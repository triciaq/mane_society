# 🧴 Mane Society — Ecommerce Analytics Case Study

> **Unpacking a $215K loss hidden behind a 3.2 ROAS.**  
> A full-stack analytics investigation into paid attribution, customer retention, and profitability for a DTC haircare brand at $920K ARR.

---

## 📌 Project Summary

Mane Society, a DTC haircare brand, was spending heavily on Meta and TikTok ads. Platform dashboards reported a healthy ROAS of 3.0–3.5. Yet the business was deeply unprofitable.

This project answers one question:

> **Why does ROAS look healthy when the business is losing money?**

The answer exposed through Python-based analysis of 1,200 orders, 84 ad campaigns, and 1,191 customer records is a 28× gap between platform-reported CAC and true acquisition cost, compounded by near-zero customer retention across all channels.

---

## 📊 Key Findings

### Finding 1 — The Attribution Gap

| Metric | Platform Reported | Reality |
|---|---|---|
| CAC (blended) | $12.89 | $361.31 |
| Gap | — | **28× underreported** |
| Months flagged | — | **24 of 24** |

Meta and TikTok claimed to acquire customers for $12.89 each. True CAC was $361.31. Every single month of the year was flagged as misleading.

### Finding 2 — Retention Crisis

```
Industry benchmark (DTC beauty):   15 – 30% repeat rate
Mane Society (best channel):        4.0%  (Influencer)
Mane Society (largest channel):     0.6%  (Meta)
Mane Society (full year average):   0.8%
```

The cohort heatmap tells the story visually — one dark column at Month 0, then near-total silence across all 12 cohorts for the rest of the year.

### Finding 3 — Profitability

```
Gross Revenue:          $79,103
Ad Spend:              $251,832   ← 329% of net revenue
Net Profit:           -$215,885
Net Margin:             -282.3%
```

Ad spend alone exceeded gross profit by $209,767. The business was spending $3.29 for every $1.00 earned.

### Finding 4 — The Path to Break Even

| Scenario | Ad Spend | Net Margin | Gap to Break Even |
|---|---|---|---|
| A — Do nothing | $251,832 | -282.3% | $392,519 |
| B — Cut 30% | $176,283 | -190.6% | $303,000 |
| C — Full fix | $176,283 | -163.6% | $249,547 |
| **D — 80% cut + retention** | **$50,366** | **-25.7%** | **$39,317** |

Scenario D — cutting paid social by 80% and investing $10,800 in email infrastructure reduces the break even gap by 90%. That remaining $39,317 gap closes with retention alone within approximately 7 months.

---

## 💡 Recommendations

**🔴 Immediate (Month 1–2)**
1. Cut Meta + TikTok spend from $21K/mo to $4.2K/mo — pause awareness and prospecting, keep retargeting only
2. Build 7-email post-purchase Klaviyo sequence targeting replenishment cycle (Day 1 → Day 270)

**🟡 Short Term (Month 2–4)**

3. Switch to value-led creative — remove discount from ad headline, A/B test vs current
4. Implement Triple Whale or Northbeam for cross-channel attribution — replace platform ROAS as primary KPI

**🟢 Medium Term (Month 4–6)**

5. Invest $10K of saved ad budget into 3–5 mid-tier influencer partnerships (highest retention channel at 4.0%)
6. Feature bundle SKUs in retargeting and welcome email — target bundle rate from 8% → 20%

---

## 🛠 Tech Stack

```python
pandas        # data manipulation and aggregation
numpy         # numerical operations
matplotlib    # all charts — no Seaborn, no Plotly
openpyxl      # reading client Excel files
```



---

## 📈 Charts

### Monthly Revenue + MoM Growth
<img width="674" height="287" alt="Image" src="https://github.com/user-attachments/assets/8158cc2e-e9e7-42c9-b1ed-048dc3dc548d" />

### Channel Mix — Revenue vs Discount Rate vs Retention
![Channel Mix](charts/chart2_channel_mix.png)

### The Attribution Gap — True CAC vs Platform CAC
![CAC Gap](charts/chart3_cac_gap.png)

### Cohort Retention Heatmap
![Cohort Heatmap](charts/chart4_cohort_heatmap.png)

### Profitability Waterfall
![Waterfall](charts/chart5_waterfall.png)

---

## 🧠 Analytical Concepts Demonstrated

- **Paid attribution analysis** — separating platform-claimed conversions from verified first-time buyers
- **True CAC calculation** — order-level customer deduplication vs marketing spend
- **Cohort retention modelling** — period-over-period customer return tracking
- **Contribution margin & break even analysis** — fixed vs variable cost structure
- **Scenario modelling** — assumption-documented projections with sensitivity
- **LTV:CAC ratio** — unit economics framing for channel efficiency
- **Demand cannibalization** — identifying promotional pull-forward in time series



