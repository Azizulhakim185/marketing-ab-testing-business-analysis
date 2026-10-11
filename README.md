# Marketing A/B Testing: Conversion Analysis & Business Decisions

**An independent data analytics portfolio project by Azizul Hakim**

[LinkedIn](https://www.linkedin.com/in/azizul185) · [GitHub](https://github.com/Azizulhakim185) · [Email](mailto:azizulhakimshuvo185@gmail.com)

## Business question

Did users shown a product advertisement convert at a higher rate than users shown a public service announcement (PSA)? If so, is the evidence strong enough to justify expanding the campaign?

This project examines conversion performance, statistical uncertainty, and experiment-quality limitations before making a business recommendation.

## Dataset and tools

- **Dataset:** [Marketing A/B Testing — Kaggle](https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing)
- **Records:** 588,101 user-level observations
- **Tools:** Python, Pandas, NumPy, Statsmodels, Matplotlib, Kaggle Notebooks
- **Methods:** Data validation, conversion-rate comparison, relative lift, two-sided two-proportion z-test, and a 95% Newcombe confidence interval for the difference in conversion rates

## Key findings

| Metric | Ad group | PSA group |
|---|---:|---:|
| Users | 564,577 | 23,524 |
| Conversions | 14,423 | 420 |
| Conversion rate | 2.5547% | 1.7854% |

- **Absolute difference:** +0.7692 percentage points (Ad − PSA)
- **Observed relative conversion lift:** +43.09%
- **Z-statistic:** 7.3701
- **Two-sided p-value:** 1.7053 × 10⁻¹³
- **95% confidence interval for absolute difference:** +0.5873 to +0.9360 percentage points
- **Basic data checks:** No missing values, duplicate user IDs, or invalid values detected by the implemented checks

The Ad group had a statistically significantly higher **observed** conversion rate than the PSA group. This result does not, by itself, establish a causal effect or a profitable campaign.

## Business recommendation: Validate before scaling

The results support further investigation, **not an unconditional increase in advertising spend**. Before scaling, the business should:

1. Verify how users were assigned and whether the planned treatment/control allocation matches the observed **96% Ad / 4% PSA** split.
2. Confirm tracking, eligibility criteria, and experiment integrity.
3. Obtain media costs, revenue per conversion, and customer-value data to estimate incremental profit.
4. If those checks pass, consider a limited rollout with conversion and financial guardrail metrics.

**Limitations:** The intended allocation and randomisation procedure are not documented in the analysed data; the sample split alone cannot confirm a sample-ratio mismatch. Exposure counts are post-assignment measurements, not proof of randomisation quality. No cost or revenue fields are available to calculate return on investment.

## Repository files

| File | Purpose |
|---|---|
| `marketing_ab_testing.ipynb` | Full Kaggle analysis notebook (Blocks 1–7) |
| `conversion_comparison.png` | Ad vs PSA conversion-rate chart |
| `conversion_confidence_interval.png` | Conversion-rate difference and 95% CI |
| `ab_testing_final_metrics.csv` | Exported statistical metrics |
| `ab_testing_executive_summary.md` | Findings, caveats, and recommendations |

## Run the analysis

1. Open the [Kaggle dataset](https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing) and create a notebook with the dataset attached.
2. Upload or open `marketing_ab_testing.ipynb` in Kaggle.
3. Run all cells in order. The notebook reads `marketing_AB.csv` from the attached dataset and saves the charts and exported summaries in `/kaggle/working/`.

**Live Kaggle notebook:** Add your public Kaggle notebook URL here after publishing it.

---
*Independent educational case study using public data. Not a commissioned project for the dataset provider or any employer.*


