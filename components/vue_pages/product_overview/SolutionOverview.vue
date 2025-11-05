<template>
  <InfoCardV2
    :items="[
      {
        title: 'What it is',
        icon: 'carbon:ai',
        description: 'AI-Enabled Alarm Manager - a software module for XProtect that uses artificial intelligence to automatically verify and filter alarms in real time.',
        features: ['AI-powered', 'Real-time filtering'],
        pros: ['Reduces false alarms', 'Automates verification'],
        cons: ['Requires AI model updates'],
        details: [
          { title: 'Module', description: 'For XProtect' },
          { title: 'Description', description: 'AI-Enabled Alarm Manager - a software module for XProtect that uses artificial intelligence to automatically verify and filter alarms in real time.' }
        ],
        themeColor: 'primary'
      },
      {
        title: 'How it works',
        icon: 'carbon:video',
        description: 'When an alarm comes in, the system instantly analyzes the associated video and data, auto-dismisses or downgrades likely false alarms, and flags real events for the operator. All alarms are visualised on the map and timeline as usual, but with AI annotations.',
        features: ['Video analytics', 'Auto-dismissal'],
        pros: ['Instant analysis', 'Operator-friendly'],
        cons: ['May need tuning'],
        details: [
          { title: 'Visualization', description: 'Map and timeline with AI annotations' },
          { title: 'Description', description: 'When an alarm comes in, the system instantly analyzes the associated video and data, auto-dismisses or downgrades likely false alarms, and flags real events for the operator. All alarms are visualised on the map and timeline as usual, but with AI annotations.' }
        ],
        themeColor: 'accent'
      },
      {
        title: 'Why it’s unique',
        icon: 'carbon:star',
        description: 'Combines advanced video analytics, human feedback loop, and contextual visualisation. It’s a self-improving alarm management system that remains operator-friendly and is entirely on-premise, aligned with Milestone’s open platform.',
        features: ['Self-improving', 'Contextual visualization'],
        pros: ['Human feedback loop', 'On-premise'],
        cons: ['Initial setup required'],
        details: [
          { title: 'Platform', description: 'Milestone open platform' },
          { title: 'Description', description: 'Combines advanced video analytics, human feedback loop, and contextual visualisation. It’s a self-improving alarm management system that remains operator-friendly and is entirely on-premise, aligned with Milestone’s open platform.' }
        ],
        themeColor: 'success'
      }
    ]"
    :columns="2"
    :useThemeColors="true"
  />
</template>
<script setup>
import InfoCardV2 from '../../cards/InfoCardV2.vue'
</script>
