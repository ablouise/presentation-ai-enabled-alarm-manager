---
class: flex items-center justify-center w-full h-full bg-black
---

<div class="video-container" style="position:relative;width:100%;height:100%;">
  <video
    id="falsealarms-video"
    src="/videos/falsealarms.mp4"
    controls
    style="width:100%;height:100%;object-fit:cover;background:black;display:block;"
  ></video>
  <div id="video-overlay" style="position:absolute;top:0;left:0;width:100%;height:100%;align-items:center;justify-content:center;display:none;background:rgba(0,0,0,0.55);color:white;font-size:2.5rem;font-weight:700;z-index:10;pointer-events:none;">
    False alarms. Real consequences.
  </div>
</div>

<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  const video = document.getElementById('falsealarms-video')
  const overlay = document.getElementById('video-overlay')
  
  if (video && overlay) {
    video.addEventListener('play', () => {
      overlay.style.display = 'none'
    })
    
    video.addEventListener('ended', () => {
      overlay.style.display = 'flex'
    })
  }
})
</script>
