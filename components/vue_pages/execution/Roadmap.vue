<template>
  <InfoCardV2
    :items="[
      {
        title: 'Q4 2025 - Prototype Phase',
        icon: 'carbon:development',
        description: 'Internal PoC demo completed.',
        details: [
          { title: 'Details', description: 'Internal PoC demo completed.' }
        ],
        themeColor: 'accent'
      },
      {
        title: 'Q1 2026 - MVP Development',
        icon: 'carbon:build-tool',
        description: 'Build Minimum Viable Product with core features.',
        details: [
          { title: 'Details', description: 'Build Minimum Viable Product with core features.' }
        ],
        themeColor: 'primary'
      },
      {
        title: 'Q2 2026 - Pilot Launch',
        icon: 'carbon:launch',
        description: 'Test in real environment with friendly customers.',
        details: [
          { title: 'Details', description: 'Test in real environment with friendly customers.' }
        ],
        themeColor: 'success'
      },
      {
        title: 'Q3 2026 - Iteration & Beta',
        icon: 'carbon:iteration',
        description: 'Incorporate pilot feedback, polish features, and scale up testing.',
        details: [
          { title: 'Details', description: 'Incorporate pilot feedback, polish features, and scale up testing.' }
        ],
        themeColor: 'info'
      },
      {
        title: 'Q4 2026 - Finalise & Go-to-Market Prep',
        icon: 'carbon:task',
        description: 'Hardening and readiness for launch.',
        details: [
          { title: 'Details', description: 'Hardening and readiness for launch.' }
        ],
        themeColor: 'neutral'
      },
      {
        title: 'H1 2027 - General Availability Launch',
        icon: 'carbon:cloud-service',
        description: 'Official product release.',
        details: [
          { title: 'Details', description: 'Official product release.' }
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
