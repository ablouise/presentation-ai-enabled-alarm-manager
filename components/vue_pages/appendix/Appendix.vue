<template>
  <InfoCardV2
    :items="[
      {
        title: 'Customer Feedback Example',
        icon: 'carbon:user-avatar',
        description: '78% of major clients indicated reducing false alarms would significantly improve their operations.',
        details: [
          { title: 'Description', description: '78% of major clients indicated reducing false alarms would significantly improve their operations.' }
        ],
        themeColor: 'primary'
      },
      {
        title: 'Industry Insight',
        icon: 'carbon:analytics',
        description: '47% of organisations plan to implement AI for event/alarm filtering, 75% express concern about alarm overload.',
        details: [
          { title: 'Description', description: '47% of organisations plan to implement AI for event/alarm filtering, 75% express concern about alarm overload.' }
        ],
        themeColor: 'accent'
      },
      {
        title: 'Technical Feasibility',
        icon: 'carbon:checkmark',
        description: 'BriefCam analytics correctly identified and filtered ~92% of test false alarms in a controlled environment.',
        details: [
          { title: 'Description', description: 'BriefCam analytics correctly identified and filtered ~92% of test false alarms in a controlled environment.' }
        ],
        themeColor: 'success'
      },
      {
        title: 'Related Documentation',
        icon: 'carbon:document',
        description: 'See AI-Enabled Alarm Manager - Concept & Design Spec and Pilot Program Outline for more detail.',
        details: [
          { title: 'Description', description: 'See AI-Enabled Alarm Manager - Concept & Design Spec and Pilot Program Outline for more detail.' }
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
