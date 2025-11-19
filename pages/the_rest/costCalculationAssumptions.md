
## Cost Calculation Assumptions

- **Alerts per day per operator:** 250
- **False alarm rate:** 90%
- **AI filtering removes:** 80% of false alarms
- **Time per alert:** 6 min (0.1 hr)
- **Hourly wage:** $45
- **Working days per year:** 250
- **SOC sizes:** 1, 5, 15, 30 operators

---

## Cost Calculation Formula

$$
	ext{Total Personnel Cost} =
(\text{Alerts/day} \times \text{Time per alert (hrs)} \times \text{Hourly wage} \times \text{Days/year} \times \text{Operators})
$$

$$
	ext{False Alarm Cost} =
	ext{Total Personnel Cost} \times \text{False alarm rate}
$$

$$
	ext{Cost After AI} =
	ext{False Alarm Cost} \times (1 - \text{Reduction rate})
$$

**Example:**
$$
	ext{Total Cost} = 250 \times 0.1 \times 45 \times 250 \times 10 = \$2{,}812{,}500
$$

$$
	ext{False Alarm Cost} = \$2{,}812{,}500 \times 0.90 = \$2{,}531{,}250
$$

$$
	ext{Cost After AI} = \$2{,}531{,}250 \times (1 - 0.80) = \$506{,}250
$$
