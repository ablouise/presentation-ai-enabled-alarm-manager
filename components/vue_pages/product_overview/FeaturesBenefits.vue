<template>
  <InfoCardV2
    :items="[
      {
        title: 'AI Alarm Verification',
        icon: 'carbon:checkmark',
        description: 'Uses video analytics to detect people, vehicles, etc., and automatically dismiss likely false alarms.',
        features: ['Video analytics'],
        pros: ['Detects people/vehicles', 'Dismisses false alarms'],
        cons: ['May miss edge cases'],
        details: [
          { title: 'Detection', description: 'People, vehicles, etc.' },
          { title: 'Description', description: 'Uses video analytics to detect people, vehicles, etc., and automatically dismiss likely false alarms.' }
        ],
        themeColor: 'success'
      },
      {
        title: 'Contextual Visualisation (FloorPlan2Graph)',
        icon: 'carbon:map',
        description: 'Translates facility maps and sensor layouts into an interactive graph. Alarms pop up on a map with their exact location.',
        features: ['Interactive graph'],
        pros: ['Visualizes alarms'],
        cons: ['Complex setup'],
        details: [
          { title: 'Map', description: 'Facility maps, sensor layouts' },
          { title: 'Description', description: 'Translates facility maps and sensor layouts into an interactive graph. Alarms pop up on a map with their exact location.' }
        ],
        themeColor: 'accent'
      },
      {
        title: 'Alarm Refinement Loop',
        icon: 'carbon:repeat',
        description: 'Integrated feedback mechanism for operators. The system learns from input using federated learning.',
        features: ['Feedback loop'],
        pros: ['Learns from operators'],
        cons: ['Requires operator input'],
        details: [
          { title: 'Learning', description: 'Federated learning' },
          { title: 'Description', description: 'Integrated feedback mechanism for operators. The system learns from input using federated learning.' }
        ],
        themeColor: 'info'
      },
      {
        title: 'Automated Camera Tracking (EasyTrack)',
        icon: 'carbon:video',
        description: 'Automatically queues up the next relevant camera feed in sequence, based on the floor plan graph and object detection.',
        features: ['Camera tracking'],
        pros: ['Queues relevant feeds'],
        cons: ['Depends on detection accuracy'],
        details: [
          { title: 'Sequence', description: 'Based on graph/object detection' },
          { title: 'Description', description: 'Automatically queues up the next relevant camera feed in sequence, based on the floor plan graph and object detection.' }
        ],
        themeColor: 'primary'
      },
      {
        title: 'GenAI-Ready (Future Add-on)',
        icon: 'carbon:chat',
        description: 'Infrastructure in place to integrate a conversational assistant for alarms in the future.',
        features: ['Conversational assistant'],
        pros: ['Future integration'],
        cons: ['Not yet available'],
        details: [
          { title: 'Infrastructure', description: 'Ready for GenAI add-on' },
          { title: 'Description', description: 'Infrastructure in place to integrate a conversational assistant for alarms in the future.' }
        ],
        themeColor: 'secondary'
      }
    ]"
    :columns="2"
    :useThemeColors="true"
  />
</template>
<script setup>
import InfoCardV2 from '../../cards/InfoCardV2.vue'
</script>
