<template>
  <InfoCardV2
    :items="[
      {
        title: 'Executive Sponsor',
        icon: 'carbon:user-admin',
        description: 'Head of Product Strategy (e.g., VP Product) – championing the project at the leadership level.',
        details: [
          { title: 'Details', description: 'Head of Product Strategy (e.g., VP Product) – championing the project at the leadership level.' }
        ],
        themeColor: 'primary'
      },
      {
        title: 'Product Lead',
        icon: 'carbon:user-avatar',
        description: 'Louise Abela – Innovation Manager, overall project manager.',
        details: [
          { title: 'Details', description: 'Louise Abela – Innovation Manager, overall project manager.' }
        ],
        themeColor: 'accent'
      },
      {
        title: 'Engineering Team',
        icon: 'carbon:development',
        description: 'Tech Lead (Integration), AI Lead, developers & QA.',
        details: [
          { title: 'Details', description: 'Tech Lead (Integration), AI Lead, developers & QA.' }
        ],
        themeColor: 'success'
      },
      {
        title: 'Cross-Functional Contributors',
        icon: 'carbon:group',
        description: 'Support Lead, Product Marketing Manager, Sales Engineering Rep.',
        details: [
          { title: 'Details', description: 'Support Lead, Product Marketing Manager, Sales Engineering Rep.' }
        ],
        themeColor: 'info'
      },
      {
        title: 'Communication Plan',
        icon: 'carbon:chat',
        description: 'Bi-weekly core team meetings, monthly update meetings, post-pilot stakeholder workshop.',
        details: [
          { title: 'Details', description: 'Bi-weekly core team meetings, monthly update meetings, post-pilot stakeholder workshop.' }
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
