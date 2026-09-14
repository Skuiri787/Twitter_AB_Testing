# 🐦 Twitter A/B Testing — Advertising Product Analysis
## Data-Driven Evaluation of Click-Based vs Impression-Based Billing

---

## 🎯 Project Objective

Twitter conducted an A/B experiment to evaluate a new **impression-based advertising billing model** designed to reduce advertiser overspending caused by delays in click reporting.

This project analyzes the experiment data to:

- Measure overspending across control and treatment groups
- Evaluate the effectiveness of the new billing model
- Analyze treatment impact across company sizes
- Investigate differences in advertiser budget-setting behavior
- Identify statistically significant performance differences
- Highlight data limitations and recommend next steps

---

## 📊 Dataset Overview

- **15,474 advertising campaigns**
- **Control:** Traditional click-based billing
- **Treatment:** Impression-based billing
- **4 available variables:**
  - Treatment group
  - Company size
  - Campaign budget
  - Campaign spend
- No missing values or duplicate records

The analysis focuses primarily on **overspend percentage, budget utilization, campaign spend, and company size**.

---

## 🛠 Tools & Techniques

- **Python** – Data cleaning, EDA & statistical analysis
- **Pandas & NumPy** – Data manipulation and feature engineering
- **Matplotlib & Seaborn** – Data visualization
- **SciPy & Statsmodels** – Hypothesis testing & regression
- **A/B Testing** – Control vs treatment comparison
- **Statistical Testing** – Proportion tests, Mann-Whitney U, Welch's t-test, Kruskal-Wallis, Levene's test
- **Logistic Regression** – Treatment × company-size interaction analysis

---

## 🔎 Key Findings

### 📉 Lower Overspending
Treatment campaigns had a lower overspending rate:

**73.9% → 66.9%**

A reduction of approximately **7.0 percentage points**, statistically significant at  
**p = 1.43 × 10⁻²¹**.

### 👥 Segment-Level Impact
The treatment effect varied by company size.

- **Small:** ~8.0 pp reduction
- **Large:** ~7.9 pp reduction
- **Medium:** ~1.7 pp reduction and not significant in the simple subgroup test

The treatment × medium-company interaction was statistically significant, indicating genuine heterogeneity in treatment effectiveness.

### 💰 Budget Differences
Treatment advertisers had a substantially lower **median campaign budget**:

**$65.38 → $38.60**

The difference was statistically significant, although the dataset cannot establish whether advertiser caution or "wariness" caused this behavior.

### 📊 Lower Budget Utilization
Average percentage of budget spent was lower under treatment:

**125.3% → 117.6%**

This indicates that treatment campaigns still exceeded budget on average, but by less than control campaigns.

### ⚖ Company Size Matters
Company size was significantly associated with overspending in both groups.

Small companies consistently showed the highest overspending levels, followed by large and medium companies.

---

## 🚫 Data Limitations

Several requested metrics could not be calculated because the supplied dataset does not contain the required fields:

| Analysis | Missing Data |
|----------|--------------|
| CTR Comparison | Click & impression counts |
| Industry Analysis | Industry / vertical |
| Engagement Analysis | Likes, retweets & replies |

Rather than estimating or fabricating these metrics, they were explicitly documented as **data gaps**.

---

## 💡 Strategic Recommendations

| Focus Area | Direction |
|------------|-----------|
| Product Rollout | Proceed with a phased rollout |
| Small & Large Advertisers | Prioritize segments showing strong treatment gains |
| Medium Advertisers | Conduct targeted follow-up / sub-experiment |
| Budget Behavior | Validate advertiser caution through surveys or interviews |
| Monitoring | Track median overspend alongside mean |
| Segmentation | Use per-segment KPIs instead of one blended target |
| Data Collection | Add CTR, engagement and industry-level data |
| Spend Variance | Re-test after investigating extreme-value accounts |

---

## 📈 Core Insight

**The impression-based billing model meaningfully reduces advertiser overspending, but its impact is not uniform across all advertiser segments.**

The strongest strategy is therefore a **phased, segment-aware rollout backed by continued experimentation and better behavioral data**.

---

## 📁 Repository Contents

- `Twitter_AB_Testing.ipynb` — Complete Python analysis & statistical testing
- `Twitter_AB_Testing_Report.docx` — Detailed project report
- `Twitter_AB_Test_ppt.pptx` — Executive presentation
- `Twitter_A_B_testing.csv` — Experiment dataset
- `README.md` — Project documentation

---

## 🧪 Experiment Summary

| Metric | Control | Treatment |
|--------|---------|-----------|
| Campaigns | 7,733 | 7,741 |
| Overspend >1% | 73.9% | 66.9% |
| Mean Overspend % | 25.3% | 17.6% |
| Median Overspend % | 6.5% | 4.6% |
| Mean Budget Spent % | 125.3% | 117.6% |
| Median Budget | $65.38 | $38.60 |

---

## 🏁 Final Decision

### **Proceed with a phased, segment-aware rollout of the impression-based billing product.**

Prioritize **small and large advertisers**, investigate the weaker medium-company response, validate the budget-setting hypothesis, and continue collecting the missing engagement, CTR, and industry data.

---

![Project Preview](twitter_ab_testing.png)
