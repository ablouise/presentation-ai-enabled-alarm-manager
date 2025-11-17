---
class: flex justify-center items-center gap-20 px40 text-xl
---

<div text-4xl absolute :class="$clicks < 1 ? 'text-white' : 'translate-y--18 scale-40 text-white/30'" transition duration-500 ease-in-out>
  <span>Let's dive in...</span>
</div>


<div flex flex-col items-center>

<v-clicks>

<div mt-20>

<h1 flex items-center text="6xl!">
<div class="relative w-150 h-150 flex items-center justify-center" style="width: 600px; height: 600px;">
  <div class="logo-grid" style="position:absolute;width:100%;height:100%;top:0;left:0;">
    <!-- 5 logos spaced evenly around a circle, not touching the edge -->
    <div class="logo-card" style="position:absolute;top:15%;left:50%;transform:translateX(-50%);">
      <div class="logo-placeholder" :class="$clicks > 1 ? 'logo-highlight' : ''">Logo 1</div>
    </div>
    <div class="logo-card" style="position:absolute;top:35%;right:13%;">
      <div class="logo-placeholder">Logo 2</div>
    </div>
    <div class="logo-card" style="position:absolute;bottom:20%;right:23%;">
      <div class="logo-placeholder">Logo 3</div>
    </div>
    <div class="logo-card" style="position:absolute;bottom:20%;left:23%;">
      <div class="logo-placeholder">Logo 4</div>
    </div>
    <div class="logo-card" style="position:absolute;top:35%;left:13%;">
      <div class="logo-placeholder">Logo 5</div>
    </div>
  </div>
    <!-- Centered Kcover and icon -->
      <div style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);z-index:10;display:flex;flex-direction:row;align-items:center;">
        <span style="font-size:2.5rem;font-weight:700;color:white;vertical-align:middle;">to the reality</span>
      </div>
</div>

<style>
  .logo-placeholder {
    width: 70px;
    height: 70px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 10px;
    font-weight: 550;
    color: white;
    background-color: rgba(255,255,255,0.15);
    border-radius: 50%;
    backdrop-filter: blur(10px);
    filter: grayscale(1);
    transition: filter 0.5s cubic-bezier(0.16, 1, 0.3, 1);
  }
  .logo-highlight {
    filter: none;
    background-color: rgba(255,255,255,0.35);
    color: #2d8a7a;
    box-shadow: 0 0 12px 2px rgba(45, 166, 178, 0.25);
  }
  @media (max-width: 768px) {
    .logo-placeholder {
      width: 50px;
      height: 50px;
      font-size: 8px;
    }
  }
</style>
  
  
</h1>

</div>

<div text-xs mt-20>
  <span>One simple intall-to-go plugin solution combines both NPD (Node Problem Detector) and operator</span>
</div>

</v-clicks>

</div>
