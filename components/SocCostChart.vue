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

// Labels for number of operators
const labels = ['1', '8', '16']

// Data based on your calculations
const data = {
  labels,
  datasets: [
    {
      label: 'Total Personnel Cost',
      backgroundColor: '#0099da',
      data: [337500, 7000000, 22000000], // Louisiana scenario updated
      datalabels: {
        display: true,
        color: '#fff',
        font: { weight: 'bold' },
        align: 'end',
        anchor: 'end',
        formatter: (value) => `$${value.toLocaleString()}`
      }
    },
    {
      label: 'False Alarm Cost (90%)',
      backgroundColor: '#ef4444',
      data: [303750, 6300000, 19800000]
    },
    {
      label: 'Cost After (-80%)',
      backgroundColor: '#2caa57',
      data: [60750, 1260000, 3960000],
      datalabels: {
        display: true,
        color: '#fff',
        font: { weight: 'bold' },
        align: 'end',
        anchor: 'end',
        formatter: (value) => `$${value.toLocaleString()}`
      }
    }
  ]
}

// Custom plugin to always show icons under the chart, resized proportionally
const iconPlugin = {
  id: 'iconPlugin',
  afterDraw(chart) {
    const { ctx, chartArea: { top }, scales: { x }, _metasets } = chart
    const icons = [
      '/icons/problem/Louisiana_Museum_of_Modern_Art_logo.svg.png',
      '/icons/problem/stockholmmetro.svg.png',
      '/icons/problem/cern.png'
    ]
    const iconHeights = [12, 48, 48]; // Louisiana even smaller
    const iconVerticalPaddings = [32, 24, 24]; // Move Louisiana logo a tiny bit higher
    icons.forEach((src, index) => {
      const img = new window.Image();
      img.src = src;
      const xPos = x.getPixelForValue(index);
      const iconHeight = iconHeights[index];
      const iconVerticalPadding = iconVerticalPaddings[index];
      // Find the top of the bar for this index
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
        title: {
        },
        legend: {
          position: 'top'
        },
        tooltip: {
          callbacks: {
            label: (context) => `$${context.parsed.y.toLocaleString()}`
          }
        },
        datalabels: {
          display: (context) => [
            'Total Personnel Cost',
            'Cost After AI Filtering (-80%)'
          ].includes(context.dataset.label)
        }
      },
      scales: {
        x: {
          title: { display: true, text: 'Number of Operators' }
        },
        y: {
          title: { display: true, text: 'Cost (USD)' },
          ticks: {
            callback: (value) => `$${value.toLocaleString()}`
          }
        }
      }
    },
    plugins: [iconPlugin]
  })
})
</script>