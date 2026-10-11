
# Marketing A/B Testing:
# Conversion Analysis & Business Decision-Making

**Analyst:** Azizul Hakim

**Project Type:** Independent Data Analytics Project

**Tools:** Python, Pandas, Statsmodels, Matplotlib

**Dataset:** Marketing A/B Testing - Kaggle

---

## 1. Business Problem

This project evaluates whether users shown a product
advertisement achieved higher conversion rates than
users shown a Public Service Announcement (PSA).

The objective is to support evidence-based decisions
about advertising performance and future investment.

## 2. Dataset Overview

| Metric | Value |
|---|---:|
| Total Users | 588,101 |
| Ad Group Users | 564,577 |
| PSA Group Users | 23,524 |
| Ad Conversions | 14,423 |
| PSA Conversions | 420 |
| Missing Values | 0 |
| Duplicate User IDs | 0 |

## 3. Conversion Performance

| Metric | Result |
|---|---:|
| Ad Conversion Rate | 2.5547% |
| PSA Conversion Rate | 1.7854% |
| Absolute Difference | +0.7692 pp |
| Relative Conversion Lift | +43.09% |

### Key Finding

The Ad group demonstrated a higher observed
conversion rate than the PSA group.

The relative conversion lift was
**+43.09%**.

This is an observed association, not independently
verified causal uplift.

## 4. Statistical Analysis

**Null Hypothesis (H0):**
The two groups have equal conversion rates.

**Alternative Hypothesis (H1):**
The conversion rates differ.

| Statistical Metric | Result |
|---|---:|
| Z-statistic | 7.3701 |
| P-value | 1.7053e-13 |
| Significance Level | 0.05 |
| 95% CI Lower | +0.5873 pp |
| 95% CI Upper | +0.9360 pp |

**Statistical Finding:**
Statistically significant positive difference.

The two-sided test finds a statistically significant
difference when the p-value is below 0.05.

The confidence interval describes uncertainty
in the estimated conversion-rate difference,
subject to the statistical model assumptions.

## 5. Experiment Quality Assessment

### Group Allocation

- Ad allocation: 96.00%
- PSA allocation: 4.00%

The observed allocation is unequal.

However, the intended allocation ratio is unknown.
Therefore, Sample Ratio Mismatch (SRM) cannot
be confirmed from these counts alone.

### Advertisement Exposure

- Ad average exposure:
  24.82

- PSA average exposure:
  24.76

- Ad median exposure:
  13.00

- PSA median exposure:
  12.00

Exposure is recorded after assignment and does
not independently confirm randomisation quality.

### Data Reliability

- No missing values detected.
- No duplicate user IDs detected.
- Basic dataset validation passed.
- Original randomisation cannot be verified.
- Planned group allocation is unavailable.
- Advertising costs and revenue are unavailable.

## 6. Business Recommendation

### Decision: VALIDATE BEFORE SCALING

The Ad group achieved a significantly higher observed conversion rate. However, the company should verify experimental randomisation, planned allocation and campaign economics before expanding advertising investment.

### Recommended Next Actions

1. Verify the planned experiment allocation
   and random assignment process.

2. Confirm experiment tracking and eligibility
   rules before interpreting causal effects.

3. Obtain advertising costs, revenue per
   conversion and customer value information.

4. Calculate incremental profit and return
   on advertising investment where possible.

5. If experiment validity and financial
   performance are confirmed, consider
   a limited monitored rollout.

6. Track conversion rate, acquisition cost
   and profitability during the rollout.

## 7. Limitations

- Randomisation procedures are not documented.
- Group allocation is highly unequal.
- The intended allocation ratio is unknown.
- Campaign financial data are unavailable.
- Profitability cannot be calculated.
- Statistical significance alone does not
  establish causality or financial success.

## 8. Final Conclusion

The Ad group achieved a conversion rate of
**2.5547%**, compared with
**1.7854%** for the PSA group.

The relative observed conversion lift was
**+43.09%**, with a statistically
significant difference (p = 1.7053e-13).

These findings support further evaluation
of the advertising strategy.

However, experimental design validation and
campaign profitability analysis are required
before recommending full-scale investment.

**Final Business Decision: VALIDATE BEFORE SCALING**

---

*Independent portfolio analysis using a
publicly available Kaggle dataset.*
