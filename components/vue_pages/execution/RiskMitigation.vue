<template>
  <InfoCardV2
    :items="[
      {
        title: 'Accuracy Risk',
        icon: 'carbon:warning',
        description: 'AI might misclassify alarms. Mitigation: Human in the loop, robust testing, continuous learning.',
        details: [
          { title: 'Details', description: 'AI might misclassify alarms. Mitigation: Human in the loop, robust testing, continuous learning.' }
        ],
        themeColor: 'warning'
      },
      {
        title: 'User Adoption Risk',
        icon: 'carbon:user-avatar',
        description: 'Operators might distrust or resist the new system. Mitigation: Designed to augment, not replace, humans; operator involvement in design/testing.',
        details: [
          { title: 'Details', description: 'Operators might distrust or resist the new system. Mitigation: Designed to augment, not replace, humans; operator involvement in design/testing.' }
        ],
        themeColor: 'primary'
      },
      {
        title: 'Integration/Performance Risk',
        icon: 'carbon:settings',
        description: 'Module could introduce performance issues. Mitigation: Supported SDKs, stress-testing, fail-safe module disable.',
        details: [
          { title: 'Details', description: 'Module could introduce performance issues. Mitigation: Supported SDKs, stress-testing, fail-safe module disable.' }
        ],
        themeColor: 'accent'
      },
      {
        title: '3rd Party Dependency',
        icon: 'carbon:partly-cloudy',
        description: 'Reliance on BriefCam analytics. Mitigation: Long-term partnership, modular AI layer.',
        details: [
          { title: 'Details', description: 'Reliance on BriefCam analytics. Mitigation: Long-term partnership, modular AI layer.' }
        ],
        themeColor: 'info'
      },
      {
        title: 'Data Privacy Concerns',
        icon: 'carbon:locked',
        description: 'Customers may worry about AI analyzing video. Mitigation: All analysis on-premises, anonymised model data, no new privacy issues.',
        details: [
          { title: 'Details', description: 'Customers may worry about AI analyzing video. Mitigation: All analysis on-premises, anonymised model data, no new privacy issues.' }
        ],
        themeColor: 'neutral'
      }
    ]"
  :useThemeColors="true"
  />
</template>
<script setup>
import InfoCardV2 from '../../cards/InfoCardV2.vue'
</script>
