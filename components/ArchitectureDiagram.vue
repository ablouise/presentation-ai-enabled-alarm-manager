<template>
  <div class="architecture-container">
    <div class="mermaid-diagram" ref="mermaidDiv"></div>
    <div class="logos-row">
      <div class="logo-item">
        <img src="/icons/problem/bosch.png" alt="Bosch" />
        <p>Bosch</p>
      </div>
      <div class="logo-item">
        <img src="/icons/problem/cern.png" alt="CERN" />
        <p>CERN</p>
      </div>
      <div class="logo-item">
        <img src="/icons/problem/tivoli.png" alt="Tivoli" />
        <p>Tivoli</p>
      </div>
      <!-- More logos -->
    </div>
  </div>
</template>

<script setup>
import mermaid from 'mermaid'
import { onMounted, ref } from 'vue'

const mermaidDiv = ref(null)

const diagramCode = `
flowchart TB
  vms[VMS\\nGenetec\\nMilestone]
  vsaas[VSaaS\\nArcules]
  access[Access Control\\nCental\\nAxxe]
  harmony[Harmony]
  verification[Alarm Verification]
  refinement[Alarm Refinement]
  user[User Interface\\nAlarmX]

  vms --> harmony
  vsaas --> harmony
  access --> harmony
  harmony --> verification
  verification --> refinement
  refinement --> user
`

onMounted(() => {
  mermaid.initialize({ startOnLoad: false })
  mermaidDiv.value.innerHTML = ''
  mermaid.render('mermaidGraph', diagramCode, (svgCode) => {
    mermaidDiv.value.innerHTML = svgCode
  })
})
</script>

<style scoped>
.architecture-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 24px;
}

.mermaid-diagram {
  max-width: 800px;
  width: 100%;
}

.logos-row {
  display: flex;
  gap: 30px;
  justify-content: center;
}

.logo-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100px;
}

.logo-item img {
  max-width: 80px;
  margin-bottom: 8px;
}
</style>
