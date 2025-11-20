---
class: py-10
glowSeed: 250
---

# Metrics in summary

<span>The measurable benefits of Datasets</span>

<div mt-4 />

<div
  grid grid-cols-3 gap-4
  transition duration-500 ease-in-out h-90
  :class="$clicks < 1 ? 'opacity-0 scale-90' : 'opacity-100 scale-100'"
>
  <v-clicks>
  <div
    border="2 solid lime-800" bg="lime-800/20"
    rounded-lg p-5 flex flex-col items-center
    transition-all duration-500 h-full
  >
    <div mb-4 flex-1 flex items-center justify-center>
      <div i-carbon:lightning text-yellow-500 text="[100px]" />
    </div>
    <div font-bold text-xl>Setup time cost</div>
    <div
      text-lime-300 text-2xl font-bold mt-2
      flex items-center gap-1
    >
      <span>5-10x</span>
      <div i-carbon:arrow-up text-green-400 />
    </div>
    <div text-sm opacity-70 mt-1>With shared environments</div>
    <div text-xs mt-3 bg="lime-900/30" rounded-lg px-3 py-1>
      From hours to minutes
    </div>
  </div>

  <div
    border="2 solid cyan-800" bg="cyan-800/20"
    rounded-lg p-5 flex flex-col items-center
    transition-all duration-500 h-full
  >
    <div mb-4 flex-1 flex items-center justify-center>
      <div i-carbon:vmdk-disk text-indigo-500 text="[100px]" />
    </div>
    <div font-bold text-xl>Save storage</div>
    <div
      text-cyan-300 text-2xl font-bold mt-2
      flex items-center gap-1
    >
      <span>90%</span>
      <div i-carbon:arrow-down text-green-400 />
    </div>
    <div text-sm opacity-70 mt-1>Using JuiceFS dedup</div>
    <div text-xs mt-3 bg="cyan-900/30" rounded-lg px-3 py-1>
      10GB → 1GB typical savings
    </div>
  </div>

  <div
    border="2 solid purple-800" bg="purple-800/20"
    rounded-lg p-5 flex flex-col items-center
    transition-all duration-500 h-full
  >
    <div mb-4 flex-1 flex items-center justify-center>
      <div i-carbon:badge text-violet-500 text="[100px]" />
    </div>
    <div font-bold text-xl>Time cost</div>
    <div
      text-purple-300 text-2xl font-bold mt-2
      flex items-center gap-1
    >
      <span>75%</span>
      <div i-carbon:arrow-down text-green-400 />
    </div>
    <div text-sm opacity-70 mt-1>No more environment setup</div>
    <div text-xs mt-3 bg="purple-900/30" rounded-lg px-3 py-1>
      Instant environment activation
    </div>
  </div>
  </v-clicks>
</div>