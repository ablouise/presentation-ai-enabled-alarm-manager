---
layout: default
---

# Cost Calculation Assumptions

<div class="grid grid-cols-3 gap-6 mt-10">

<div class="border-2 border-blue-500 rounded-lg p-4 bg-blue-50 dark:bg-blue-900/20">
<div class="text-blue-600 dark:text-blue-400 font-bold mb-3">📊 Operations</div>
<ul class="text-sm space-y-1">
<li>⏱️ Time/alert: <strong>6 min</strong></li>
<li>💵 Wage: <strong>$45/hr</strong></li>
<li>📅 Annual hrs: <strong>2,080</strong></li>
<li>🗓️ Working days: <strong>250</strong></li>
</ul>
</div>

<div class="border-2 border-red-500 rounded-lg p-4 bg-red-50 dark:bg-red-900/20">
<div class="text-red-600 dark:text-red-400 font-bold mb-3">🎯 Alerts</div>
<ul class="text-sm space-y-1">
<li>❌ False alarms: <strong>90%</strong></li>
<li>✅ True positives: <strong>10%</strong></li>
<li>🤖 AI filtering: <strong>-80%</strong></li>
<li>📉 After AI: <strong>28%</strong></li>
</ul>
</div>

<div class="border-2 border-green-500 rounded-lg p-4 bg-green-50 dark:bg-green-900/20">
<div class="text-green-600 dark:text-green-400 font-bold mb-3">👥 24/7 Staffing</div>
<ul class="text-sm space-y-1">
<li>⚡ Productivity: <strong>70%</strong></li>
<li>🕐 Effective hrs: <strong>5.6/shift</strong></li>
<li>🔄 FTE multiplier: <strong>4.2×</strong></li>
<li>👥 <strong>Minimum 2 operators per shift</strong></li>
<li>🕒 <strong>3 shifts per day</strong></li>
</ul>
</div>

</div>

<div class="mt-8 text-center">

### Alert Volume After AI Filtering

$$
\text{Remaining Alerts} = \text{Original Volume} \times 0.28
$$

<div class="text-sm opacity-75 mt-2">
(10% true alarms + 90% × 20% remaining false alarms)
</div>

</div>
---
layout: default
---

# Cost Calculation Steps & Example

<div class="grid grid-cols-2 gap-8 mt-6">

<div>

### Calculation Steps

$$
\text{Daily Workload (hrs)} = \text{Alerts/day} \times 0.1
$$

$$
\text{Base Positions} = \frac{\text{Daily Workload}}{5.6}
$$

$$
\text{Calculated Operators} = \text{Base Positions} \times 4.2
$$

$$
\text{Operators} = \max(\text{Calculated Operators}, 6)
$$

$$
\text{Total Cost} = \text{Operators} \times 45 \times 2,080
$$



</div>

<div>

### Example: 150 alerts/day

<div class="text-sm">

| Stage              | Value/Calculation                  |
|--------------------|----------------------------------|
| Daily workload     | 150 × 0.1 = 15 hrs               |
| Base positions     | 15 ÷ 5.6 = 2.68                  |
| Calculated ops     | 2.68 × 4.2 = 11 operators       |
| Enforced minimum   | max(11, 6) = 11 operators       |
| **Cost before AI** | **11 × $45 × 2,080 = $1,029,600**|
| Alerts after AI    | 150 × 0.28 = 42 alerts/day       |

</div>

</div>

</div>


