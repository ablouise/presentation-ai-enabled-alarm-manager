<template>
  <InfoCardV2
    :items="[
      {
        title: 'High Industry Demand',
        icon: 'carbon:analytics',
        description: '47% of security organisations plan to use AI to automatically filter events.',
        details: [
          { title: 'Description', description: '47% of security organisations plan to use AI to automatically filter events.' }
        ],
        themeColor: 'accent'
      },
      {
        title: 'Existing Customer Pain = Immediate Market',
        icon: 'carbon:warning',
        description: 'Many enterprise customers have explicitly complained about false alarms.',
        details: [
          { title: 'Description', description: 'Many enterprise customers have explicitly complained about false alarms.' }
        ],
        themeColor: 'warning'
      },
      {
        title: 'Competitive Landscape',
        icon: 'carbon:compare',
        description: 'Competitors have piecemeal offerings, but none integrate seamlessly with a VMS like our approach.',
        details: [
          { title: 'Description', description: 'Competitors have piecemeal offerings, but none integrate seamlessly with a VMS like our approach.' }
        ],
        themeColor: 'secondary'
      },
      {
        title: 'Revenue & Growth Potential',
        icon: 'carbon:money',
        description: 'Opens a new recurring revenue stream as an add-on module.',
        details: [
          { title: 'Description', description: 'Opens a new recurring revenue stream as an add-on module.' }
        ],
        themeColor: 'success'
      },
      {
        title: 'Broader Impact',
        icon: 'carbon:star',
        description: 'Successfully solving the false alarm problem strengthens Milestone’s value proposition overall.',
        details: [
          { title: 'Description', description: 'Successfully solving the false alarm problem strengthens Milestone’s value proposition overall.' }
        ],
        themeColor: 'primary'
      }
    ]"
    :columns="5"
    :useThemeColors="true"
  />
</template>
<script setup>
import InfoCardV2 from '../../cards/InfoCardV2.vue'
</script>
