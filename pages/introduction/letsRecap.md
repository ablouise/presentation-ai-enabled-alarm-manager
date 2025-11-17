---
class: flex justify-center items-center gap-20 px40 text-xl
---

<div text-4xl absolute :class="$clicks < 1 ? 'text-white' : 'translate-y--18 scale-40 text-white/30'" transition duration-500 ease-in-out>
  <span>The Reality</span>
</div>

<div flex flex-col items-center>
  <v-clicks>
    <div mt-20>
      <h1 flex items-center text="6xl!">
        <!-- Centered content container -->
        <div class="relative w-150 h-150 flex items-center justify-center" style="width: 600px; height: 600px;">
          <div style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);z-index:10;display:flex;flex-direction:row;align-items:center;">
            <span style="font-size:2.5rem;font-weight:700;color:white;vertical-align:middle;">Summarised</span>
          </div>
        </div>
      </h1>
    </div>

    <div text-xs mt-20>
      <span>One simple intall-to-go plugin solution combines both NPD (Node Problem Detector) and operator</span>
    </div>
  </v-clicks>
</div>

<!-- Four cards with individual v-click directives -->

<!-- Card 1: Top Left - Blue (#0099da) -->
<div
  v-click="3"
  style="position:fixed;top:20px;left:20px;z-index:50;min-width:260px;max-width:320px;"
  border="2 solid blue-800" bg="blue-800/20"
  rounded-lg overflow-hidden
  transition duration-500 ease-in-out
  :class="$clicks < 3 ? 'opacity-0 translate-y-20' : 'opacity-100 translate-y-0'"
>
  <div bg="blue-800/40" px-4 py-2 flex items-center>
    <div i-carbon:alarm text-blue-300 text-xl mr-2 />
    <span style="color:#0099da;font-weight:700;font-size:0.95rem;">Alarm Fatigue: The hidden cost</span>
  </div>
  <div px-5 py-3>
    <span style="font-size:0.8rem;color:white;">Operators are drowning in false alarms, leading to alert blindness and missed threats.</span>
  </div>
</div>

<!-- Card 2: Top Right - Cobalt (#0c62ad) -->
<div
  v-click="4"
  style="position:fixed;top:20px;right:20px;z-index:50;min-width:260px;max-width:320px;border:2px solid #d4edfc;background:rgba(212, 237, 252, 0.1);"
  rounded-lg overflow-hidden
  transition duration-500 ease-in-out
  :class="$clicks < 4 ? 'opacity-0 translate-y-20' : 'opacity-100 translate-y-0'"
>
  <div style="background:rgba(212, 237, 252, 0.2);" px-4 py-2 flex items-center>
    <div i-carbon:information style="color:#d4edfc;" text-xl mr-2 />
    <span style="color:#d4edfc;font-weight:700;font-size:0.95rem;">Context Matters. But Systems Don't Know It.</span>
  </div>
  <div px-5 py-3>
    <span style="font-size:0.8rem;">Without context, operators can't distinguish critical threats from routine events.</span>
  </div>
</div>

<!-- Card 3: Bottom Left - Green (#2caa57) -->
<div
  v-click="5"
  style="position:fixed;bottom:20px;left:20px;z-index:50;min-width:260px;max-width:320px;border:2px solid rgba(44, 170, 87, 0.4);background:rgba(44, 170, 87, 0.1);"
  rounded-lg overflow-hidden
  transition duration-500 ease-in-out
  :class="$clicks < 5 ? 'opacity-0 translate-y-20' : 'opacity-100 translate-y-0'"
>
  <div style="background:rgba(44, 170, 87, 0.2);" px-4 py-2 flex items-center>
    <div i-carbon:flow style="color:#2caa57;" text-xl mr-2 />
      <span style="color:#2caa57;font-weight:700;font-size:0.95rem;">One Alarm. Multiple Systems. Multiple UIs.</span>
  </div>
  <div px-5 py-3>
    <span style="font-size:0.8rem;">Operators chase one alarm across multiple systems, losing critical time and situational awareness.</span>
  </div>
</div>

<!-- Card 4: Bottom Right - Yellow (#ffe700) -->
<div
  v-click="6"
  style="position:fixed;bottom:20px;right:20px;z-index:50;min-width:260px;max-width:320px;border:2px solid rgba(255, 231, 0, 0.4);background:rgba(255, 231, 0, 0.1);"
  rounded-lg overflow-hidden
  transition duration-500 ease-in-out
  :class="$clicks < 6 ? 'opacity-0 translate-y-20' : 'opacity-100 translate-y-0'"
>
  <div style="background:rgba(255, 231, 0, 0.2);" px-4 py-2 flex items-center>
    <div i-carbon:settings style="color:#ffe700;" text-xl mr-2 />
    <span style="color:#ffe700;font-weight:700;font-size:0.95rem;">Every Camera. Every System. Different Setup.</span>
  </div>
  <div px-5 py-3>
    <span style="font-size:0.8rem;">Analytics capabilities exist but remain locked behind complex, time-consuming deployments.</span>
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
