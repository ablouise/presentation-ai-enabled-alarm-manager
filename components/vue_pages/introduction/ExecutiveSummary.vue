<template>
  <InfoCardV2
    :items="[
      {
        title: 'Overview',
        icon: 'carbon:summary',
        description: 'An AI-driven module that dramatically reduces false alarms and improves security response efficiency, fully integrated with Milestone’s platform.',
        features: ['AI-driven', 'Integrated'],
        pros: ['Reduces false alarms', 'Improves efficiency'],
        cons: ['Requires integration'],
        details: [
          { title: 'Integration', description: 'With Milestone platform' }
        ],
        themeColor: 'primary'
      },
      {
        title: 'Value',
        icon: 'carbon:value-chain',
        description: 'Frees operators from alert overload, ensures real threats get immediate attention, and continuously learns to get smarter over time.',
        features: ['Continuous learning'],
        pros: ['Immediate attention to threats', 'Learns over time'],
        cons: ['Learning curve'],
        details: [
          { title: 'Operator', description: 'Frees from alert overload' }
        ],
        themeColor: 'success'
      },
      {
        title: 'Strategic Fit',
        icon: 'carbon:plan',
        description: 'Aligns with our company’s AI innovation goals and reinforces Milestone’s open-platform leadership by adding intelligent workflow capabilities to XProtect.',
        features: ['AI innovation', 'Open-platform'],
        pros: ['Reinforces leadership'],
        cons: ['Requires workflow changes'],
        details: [
          { title: 'Workflow', description: 'Intelligent workflow capabilities' }
        ],
        themeColor: 'accent'
      }
    ]"
  :useThemeColors="true"
  />
</template>
<script setup>
import InfoCardV2 from '../../cards/InfoCardV2.vue'
</script>
