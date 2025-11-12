---
layout: center
class: text-center
---

<style>
.particle-1, .particle-2, .particle-3 {
  position: absolute;
  border-radius: 9999px;
  filter: blur(48px);
  z-index: 0;
  pointer-events: none;
}
.particle-1 {
  width: 300px; height: 300px; background: var(--theme-primary); left: -10%; top: 20%; animation: float 20s infinite ease-in-out;
  opacity: 0.28;
}
.particle-2 {
  width: 200px; height: 200px; background: var(--theme-primary); right: -5%; top: 60%; animation: float 20s infinite ease-in-out 5s;
  opacity: 0.28;
}
.particle-3 {
  width: 400px; height: 400px; background: var(--theme-accent); left: 50%; bottom: -10%; animation: float 20s infinite ease-in-out 10s;
  opacity: 0.22;
}
@keyframes float {
  0%, 100% { transform: translate(0, 0) scale(1); }
  33% { transform: translate(50px, -50px) scale(1.1); }
  66% { transform: translate(-30px, 30px) scale(0.9); }
}
.stat-card {
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
  transition: box-shadow 0.3s, transform 0.3s;
  padding: 1.5rem 1rem;
  min-width: 0;
  margin: 0 1rem;
  background: rgba(30, 41, 59, 0.35);
  color: var(--theme-info);
  border-radius: 1.25rem;
  border: 1.5px solid rgba(255,255,255,0.18);
  backdrop-filter: blur(18px) saturate(180%);
  -webkit-backdrop-filter: blur(18px) saturate(180%);
}
.stat-card:hover {
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
  transform: translateY(-8px);
}
.stat-card:nth-child(1) {
  border-color: var(--theme-warning);
}
.stat-card:nth-child(2) {
  border-color: var(--theme-primary);
}
.stat-card:nth-child(3) {
  border-color: var(--theme-error);
}
.result-card {
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
  max-width: 600px;
  padding: 1.2rem 1rem;
  margin: 0 auto;
  background: rgba(15, 23, 42, 0.45);
  color: var(--theme-info);
  border-color: var(--theme-primary);
  border-radius: 1.25rem;
  border: 1.5px solid rgba(255,255,255,0.18);
  backdrop-filter: blur(18px) saturate(180%);
  -webkit-backdrop-filter: blur(18px) saturate(180%);
}
.stats-headline h1 {
  font-size: 2.2rem;
  margin-bottom: 1.2rem;
  line-height: 1.1;
  color: var(--theme-primary);
}
.stats-headline .highlight {
  color: var(--theme-neutral);
  font-weight: 700;
  letter-spacing: 1px;
}
.grid-cols-3 {
  max-width: 1100px;
  margin: 0 auto 2rem auto;
  padding-left: 2rem !important;
  padding-right: 2rem !important;
}
.text-6xl {
  font-size: 2.1rem;
}
.text-lg {
  font-size: 1rem;
}
.result-card h2 {
  font-size: 1.3rem;
  margin-bottom: 0.7rem;
  color: var(--theme-primary);
}
.result-card p {
  font-size: 1rem;
}
.result-section {
  margin-top: 1.5rem !important;
}
.divider-line {
  height: 1px;
  background: linear-gradient(90deg, transparent, var(--theme-primary) 60%, transparent);
  opacity: 0.7;
  width: 80%;
  margin: 1.5rem auto 1.5rem auto;
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
}
.stat-card .stat-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
}
.stat-card:nth-child(1) .stat-icon {
  color: var(--theme-warning);
  filter: drop-shadow(0 0 12px #ffe700cc);
}
.stat-card:nth-child(2) .stat-icon {
  color: var(--theme-primary);
  filter: drop-shadow(0 0 12px #0099dacc);
}
.stat-card:nth-child(3) .stat-icon {
  color: var(--theme-error);
  filter: drop-shadow(0 0 12px #ef4444cc);
}
@media (max-width: 900px) {
  .grid-cols-3 {
    grid-template-columns: 1fr;
    gap: 1.2rem;
    padding-left: 0.5rem !important;
    padding-right: 0.5rem !important;
    margin-bottom: 1.5rem;
  }
  .stats-headline h1 {
    font-size: 1.1rem;
    margin-bottom: 0.7rem;
  }
  .result-card {
    max-width: 98vw;
    padding: 1rem 0.5rem;
  }
  .result-card h2 {
    font-size: 1rem;
    margin-bottom: 0.5rem;
  }
  .result-card p {
    font-size: 0.9rem;
  }
  .result-section {
    margin-top: 1rem !important;
  }
  .divider-line {
    margin: 1rem auto 1rem auto;
  }
}
</style>

<div class="stats-headline mt-10 mb-6">
  <h1 class="font-bold leading-tight text-center">When everything is urgent,<br><span class="highlight">nothing is</span></h1>
</div>

<div class="grid grid-cols-3 gap-8 px-8 justify-center items-center" style="margin-bottom: 2rem;">
  <div v-click class="stat-card rounded-2xl text-center border border-theme-warning" style="border-top: 4px solid var(--theme-warning);">
    <div class="stat-icon">&#9888;</div>
    <div class="text-6xl font-bold mb-3">95%</div>
    <div class="text-lg text-white/80 font-medium tracking-wide">false alarms</div>
  </div>
  <div v-click="2" class="stat-card rounded-2xl text-center border border-theme-primary" style="border-top: 4px solid var(--theme-primary);">
    <div class="stat-icon">&#128100;</div>
    <div class="text-6xl font-bold mb-3">200+/day</div>
    <div class="text-lg text-white/80 font-medium tracking-wide">per operator</div>
  </div>
  <div v-click="3" class="stat-card rounded-2xl text-center border border-theme-error" style="border-top: 4px solid var(--theme-error);">
    <div class="stat-icon">&#128176;</div>
    <div class="text-6xl font-bold mb-3">$50K+</div>
    <div class="text-lg text-white/80 font-medium tracking-wide">annual cost</div>
  </div>
</div>

<div class="divider-line"></div>

<div v-click="4" class="result-section mx-auto flex justify-center items-center">
  <div class="w-full max-w-4xl">
    <div class="result-card rounded-2xl text-center border mx-auto">
      <h2 class="font-semibold mb-3">Result:</h2>
      <p class="text-white/90 leading-relaxed">
        Operators ignore <span class="font-semibold" style="color: var(--theme-error);">60% of alerts</span>, missing real threats
      </p>
    </div>
  </div>
</div>
