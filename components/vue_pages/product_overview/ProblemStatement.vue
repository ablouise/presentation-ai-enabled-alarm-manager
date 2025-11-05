<template>
    <InfoCardV2
      :items="[
        {
          title: 'Alarm Overload',
          icon: 'carbon:warning',
          description: 'Security teams are inundated with alarms - often hundreds per day, of which roughly 90%+ are false positives. Operators struggle to distinguish real threats from routine noise.',
          features: ['Scalable', 'Real-time'],
          pros: ['Reduces false alarms', 'Improves efficiency'],
          cons: ['Requires initial setup'],
          details: [
            { title: 'Stat', description: '90%+ are false positives' },
            { title: 'Description', description: 'Security teams are inundated with alarms - often hundreds per day, of which roughly 90%+ are false positives. Operators struggle to distinguish real threats from routine noise.' }
          ],
          themeColor: 'warning'
        },
        {
          title: 'Alarm Fatigue',
          icon: 'carbon:face-dissatisfied',
          description: 'Constant false alerts lead to desensitisation. Critical alarms can be ignored or missed because staff grow accustomed to assuming alarms aren\'t genuine. This poses serious safety risks.',
          features: ['Operator health'],
          pros: ['Highlights critical alarms'],
          cons: ['Risk of missed incidents'],
          details: [
            { title: 'Safety Risk', description: 'Critical alarms can be ignored' },
            { title: 'Description', description: 'Constant false alerts lead to desensitisation. Critical alarms can be ignored or missed because staff grow accustomed to assuming alarms aren\'t genuine. This poses serious safety risks.' }
          ],
          themeColor: 'error'
        },
        {
          title: 'Resource Drain',
          icon: 'carbon:time',
          description: 'Handling every alarm (even false ones) consumes significant staff time and attention. It also triggers unnecessary responses (e.g., dispatching guards or engineers for false calls), which is costly and erodes confidence in the system.',
          features: ['Cost impact'],
          pros: ['Reduces unnecessary dispatches'],
          cons: ['Staff time wasted'],
          details: [
            { title: 'Cost', description: 'Unnecessary responses are costly' },
            { title: 'Description', description: 'Handling every alarm (even false ones) consumes significant staff time and attention. It also triggers unnecessary responses (e.g., dispatching guards or engineers for false calls), which is costly and erodes confidence in the system.' }
          ],
          themeColor: 'neutral'
        },
        {
          title: 'Impact',
          icon: 'carbon:chart-area',
          description: 'The net effect is reduced efficiency and increased risk - real security incidents might slip through, while personnel are stretched thin managing mostly irrelevant alerts.',
          features: ['Efficiency'],
          pros: ['Improves focus on real threats'],
          cons: ['Personnel stretched thin'],
          details: [
            { title: 'Risk', description: 'Real incidents might slip through' },
            { title: 'Description', description: 'The net effect is reduced efficiency and increased risk - real security incidents might slip through, while personnel are stretched thin managing mostly irrelevant alerts.' }
          ],
          themeColor: 'secondary'
        }
      ]"
      :columns="2"
      :useThemeColors="true"
    />
</template>
<script setup>
import InfoCardV2 from '../../cards/InfoCardV2.vue'
</script>
