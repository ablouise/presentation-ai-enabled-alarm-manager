<template>
  <InfoCardV2
    :items="[
      {
        title: 'Management Approval',
        icon: 'carbon:checkmark',
        description: 'Decision needed to proceed with full project execution.',
        details: [
          { title: 'Details', description: 'Decision needed to proceed with full project execution.' }
        ],
        themeColor: 'success'
      },
      {
        title: 'Project Kick-off',
        icon: 'carbon:calendar',
        description: 'Schedule a kick-off meeting within 2 weeks with all core team members.',
        details: [
          { title: 'Details', description: 'Schedule a kick-off meeting within 2 weeks with all core team members.' }
        ],
        themeColor: 'accent'
      },
      {
        title: 'Pilot Customer Confirmation',
        icon: 'carbon:user-avatar',
        description: 'Secure written agreement from at least one key pilot customer.',
        details: [
          { title: 'Details', description: 'Secure written agreement from at least one key pilot customer.' }
        ],
        themeColor: 'primary'
      },
      {
        title: 'Resource Alignment',
        icon: 'carbon:group',
        description: 'Ensure identified team members can start dedicating time from Q1 2026.',
        details: [
          { title: 'Details', description: 'Ensure identified team members can start dedicating time from Q1 2026.' }
        ],
        themeColor: 'info'
      },
      {
        title: 'Communication to Wider Teams',
        icon: 'carbon:chat',
        description: 'Announce project to relevant departments.',
        details: [
          { title: 'Details', description: 'Announce project to relevant departments.' }
        ],
        themeColor: 'neutral'
      },
      {
        title: 'Status Checkpoints',
        icon: 'carbon:task',
        description: 'Set initial checkpoints for oversight (end of Q1 and Q2 2026).',
        details: [
          { title: 'Details', description: 'Set initial checkpoints for oversight (end of Q1 and Q2 2026).' }
        ],
        themeColor: 'warning'
      }
    ]"
    :useThemeColors="true"
  />
</template>
<script setup>
import InfoCardV2 from '../../cards/InfoCardV2.vue'
</script>
