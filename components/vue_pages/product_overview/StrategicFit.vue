<template>
  <InfoCardV2
    :items="[
      {
        title: 'Aligns with Company Objectives',
        icon: 'carbon:plan',
        description: 'Supports Milestone\'s strategic initiative to infuse AI into our core products.',
        details: [
          { title: 'Description', description: 'Supports Milestone\'s strategic initiative to infuse AI into our core products.' }
        ],
        themeColor: 'primary'
      },
      {
        title: 'Enhances Open Platform',
        icon: 'carbon:open-panel-top',
        description: 'Adds intelligence without locking in proprietary hardware. Works with any cameras/sensors our VMS supports.',
        details: [
          { title: 'Description', description: 'Adds intelligence without locking in proprietary hardware. Works with any cameras/sensors our VMS supports.' }
        ],
        themeColor: 'accent'
      },
      {
        title: 'Customer-Driven Roadmap',
        icon: 'carbon:user-avatar',
        description: 'Addresses a pain point raised by many customers (false alarms), increasing satisfaction and loyalty.',
        details: [
          { title: 'Description', description: 'Addresses a pain point raised by many customers (false alarms), increasing satisfaction and loyalty.' }
        ],
        themeColor: 'success'
      },
      {
        title: 'Future-Proofing',
        icon: 'carbon:rocket',
        description: 'Lays groundwork for further AI features and keeps Milestone ahead of competitors.',
        details: [
          { title: 'Description', description: 'Lays groundwork for further AI features and keeps Milestone ahead of competitors.' }
        ],
        themeColor: 'info'
      }
    ]"
  :columns="1"
  :useThemeColors="true"
  />
</template>
<script setup>
import InfoCardV2 from '../../cards/InfoCardV2.vue'
</script>
