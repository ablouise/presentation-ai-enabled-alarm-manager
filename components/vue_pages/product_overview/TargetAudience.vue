<template>
  <InfoCardV2
    :items="[
      {
        title: 'SOC Operators',
        icon: 'carbon:user-avatar',
        description: 'Front-line surveillance staff who monitor alarms. They currently face alert overload and would benefit from a system that pre-screens false alarms.',
        details: [
          { title: 'Description', description: 'Front-line surveillance staff who monitor alarms. They currently face alert overload and would benefit from a system that pre-screens false alarms.' }
        ],
        themeColor: 'primary'
      },
      {
        title: 'Security Managers',
        icon: 'carbon:security',
        description: 'Leaders managing security operations. Their concerns are missed incidents and team efficiency. This solution helps ensure their team responds to true threats promptly and can handle more with the same resources.',
        details: [
          { title: 'Description', description: 'Leaders managing security operations. Their concerns are missed incidents and team efficiency. This solution helps ensure their team responds to true threats promptly and can handle more with the same resources.' }
        ],
        themeColor: 'accent'
      },
      {
        title: 'Monitoring Centres',
        icon: 'carbon:building',
        description: 'Organisations that manage alarms for multiple clients. For them, cutting false alarms means each operator can cover more clients/sites effectively, improving service quality and profitability.',
        details: [
          { title: 'Description', description: 'Organisations that manage alarms for multiple clients. For them, cutting false alarms means each operator can cover more clients/sites effectively, improving service quality and profitability.' }
        ],
        themeColor: 'success'
      },
      {
        title: 'Internal Stakeholders',
        icon: 'carbon:group',
        description: 'Product and R&D teams, Support engineers, and Sales will also be involved – ensuring we build the right solution and can support and sell it. End-users remain the security teams above.',
        details: [
          { title: 'Description', description: 'Product and R&D teams, Support engineers, and Sales will also be involved – ensuring we build the right solution and can support and sell it. End-users remain the security teams above.' }
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
