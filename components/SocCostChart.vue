<template>
  <div>
    <canvas ref="chartCanvas"></canvas>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import ChartDataLabels from 'chartjs-plugin-datalabels'
import {
  Chart,
  BarController,
  BarElement,
  CategoryScale,
  LinearScale,
  Legend,
  Title,
  Tooltip
} from 'chart.js'

Chart.register(BarController, BarElement, CategoryScale, LinearScale, Legend, Title, Tooltip, ChartDataLabels)

const chartCanvas = ref(null)

const labels = ['Louisiana', 'Stockholm Metro', 'CERN']

// Updated calculations with minimum 6 operators total per site (2 operators × 3 shifts)
const data = {
  labels,
  datasets: [
    {
      label: 'Total Personnel Cost',
      backgroundColor: getComputedStyle(document.documentElement).getPropertyValue('--theme-accent') || '#0099da',
      data: [
        1029600, // Louisiana (11 operators before AI)
        2808000, // Stockholm (30 operators before AI)
        5054400  // CERN (54 operators before AI)
      ],
      operatorsBefore: [11, 30, 54],
      datalabels: {
        display: true,
        color: '#fff',
        font: { weight: 'bold', size: 11 },
        align: 'end',
        anchor: 'end',
        formatter: value => `$${(value / 1000000).toFixed(1)}M`
      }
    },
    {
      label: 'False Alarm Cost (90%)',
      backgroundColor: getComputedStyle(document.documentElement).getPropertyValue('--theme-error') || '#ef4444',
      data: [926640, 2527200, 4548960],
      datalabels: { display: false }
    },
    {
      label: 'Cost After AlarmX',
      backgroundColor: getComputedStyle(document.documentElement).getPropertyValue('--theme-neutral') || '#2caa57',
      data: [
        561600,  // Louisiana (min 6 operators after AI)
        748800,  // Stockholm (8 operators as calculated after AI)
        1404000  // CERN (15 operators as before, exceeds min)
      ],
      operatorsAfter: [6, 8, 15],
      reductions: ['46%', '73%', '72%'],
      reductionAmounts: [468000, 2059200, 3650400],
      datalabels: {
        display: true,
        color: '#fff',
        font: { weight: 'bold', size: 11 },
        align: 'end',
        anchor: 'end',
        formatter: value => `$${(value / 1000000).toFixed(2)}M`
      }
    }
  ]
}

const iconPlugin = {
  id: 'iconPlugin',
  afterDraw(chart) {
    const { ctx, chartArea: { top }, scales: { x }, _metasets } = chart
    const icons = [
      '/icons/problem/Louisiana_Museum_of_Modern_Art_logo.svg.png',
      '/icons/problem/stockholmmetro.svg.png',
      '/icons/problem/cern.png'
    ]
    const iconHeights = [12, 48, 48]
    const iconVerticalPaddings = [32, 24, 24]
    icons.forEach((src, index) => {
      const img = new window.Image();
      img.src = src;
      const xPos = x.getPixelForValue(index);
      const iconHeight = iconHeights[index];
      const iconVerticalPadding = iconVerticalPaddings[index];
      let barTop = top + 10;
      if (_metasets && _metasets[0] && _metasets[0].data[index]) {
        barTop = _metasets[0].data[index].y - iconHeight - iconVerticalPadding;
      }
      img.onload = () => {
        const aspect = img.width / img.height;
        const iconWidth = iconHeight * aspect;
        ctx.drawImage(img, xPos - iconWidth / 2, barTop, iconWidth, iconHeight);
      };
      if (img.complete) {
        const aspect = img.width / img.height || 1;
        const iconWidth = iconHeight * aspect;
        ctx.drawImage(img, xPos - iconWidth / 2, barTop, iconWidth, iconHeight);
      }
    });
  }
}

onMounted(() => {
  new Chart(chartCanvas.value, {
    type: 'bar',
    data,
    options: {
      responsive: true,
      plugins: {
        legend: { position: 'top' },
        tooltip: {
          callbacks: {
            label: (context) => {
              const dataset = context.dataset
              const idx = context.dataIndex
              const value = `$${context.parsed.y.toLocaleString()}`
              if (dataset.label === 'Total Personnel Cost') {
                const opsBefore = dataset.operatorsBefore?.[idx]
                return [
                  `• ${dataset.label}: ${value}`,
                  `• Operators before AI: ${opsBefore}`
                ]
              }
              if (dataset.label === 'Cost After AlarmX') {
                const opsAfter = dataset.operatorsAfter?.[idx]
                const reductionPercent = dataset.reductions?.[idx]
                const reductionAmount = `$${dataset.reductionAmounts?.[idx].toLocaleString()}`
                return [
                  `• ${dataset.label}: ${value}`,
                  `• Operators after AI: ${opsAfter}`,
                  `• Reduction: ${reductionPercent} (${reductionAmount})`
                ]
              }
              return `• ${dataset.label}: ${value}`
            }
          }
        },
        datalabels: {
          display: (context) => [
            'Total Personnel Cost',
            'Cost After AlarmX'
          ].includes(context.dataset.label)
        }
      },
      scales: {
        x: { title: { display: true, text: 'Site (24/7 Operations)' } },
        y: {
          title: { display: true, text: 'Annual Cost (USD)' },
          ticks: {
            callback: (value) => `$${(value / 1000000).toFixed(1)}M`
          }
        }
      }
    },
    plugins: [iconPlugin]
  })
})
</script>
