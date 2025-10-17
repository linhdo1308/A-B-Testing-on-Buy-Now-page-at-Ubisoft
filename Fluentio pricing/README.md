# Fluent.io Pricing A/B Test — Pro Plan Impact on ARPU

## 1. Project Overview  
Fluent.io is an AI-powered language learning app offering adaptive lessons, pronunciation training, and AI conversation practice. Currently, the app uses a freemium subscription model with:

- **Free**: Ad-supported, limited features  
- **Plus**: $9.99/month, ad-free  

20% of paying users contribute 80% of revenue through in-app purchases.  

The goal of this project is to evaluate the impact of adding a **Pro plan** ($14.99/month) with enhanced features on **average revenue per user (ARPU)** through an A/B test.  

### a. Current Plans (Control)  
- Free: Ad-supported, limited features  
- Plus: $9.99/month, ad-free  

### b. Proposed Test Variation (Treatment)  
- Free: Ad-supported, limited features  
- Plus: $9.99/month, ad-free  
- Pro: $14.99/month, ad-free, with pronunciation training, AI simulated conversation, and advanced scheduling/reminder tools  

---

## 2. Test Design  

### a. A/B Test Details  
- **Primary Metric:** ARPU (subscription + in-app purchases)  
- **Minimum Effect of Interest (MEI):** $0.50  
- **Unit of Analysis:** Customer  
- **Hypotheses:**  
  - **Null (H₀):** ARPU difference ≤ $0.50  
  - **Alternative (H₁):** ARPU difference > $0.50  

### b. Experimental Setup  

| Parameter | Value |
|-----------|-------|
| α (Significance level) | 0.05 |
| Power (1 - β) | 0.8 |
| Sample Size (per checkpoint) | 2,820; 5,638; 8,456; 11,276 |
| Expected Sample Size under H1 | 9,814 |
| Allocation | 50% control / 50% treatment |
| Test Duration | 115 days (~3 months, 23 days) |
| Test Type | Group sequential with O’Brien-Fleming spending, 4 checkpoints |

**Assumptions:**  
- New users arrive daily and are randomly assigned to control or treatment  
- No major promotions or competitor campaigns interfere during testing  
- Previous month revenue can be used for variance reduction (CUPED)  

---

## 3. Results (Expected / Simulated)  

- **ARPU (Historical Data):** $2.82  
- **SD of Revenue per User (SDRPU):** $10.94  
- **Traditional Fixed Sample Size Needed:** 11,972 (5,956 per group)  
- **Required Duration:** ~140 days  
- **Expected Early Stopping (True Effect = $0.25):** High probability at checkpoint 2 (~42%)  

**Interpretation:** The Pro plan is expected to increase ARPU if the treatment effect is ≥ $0.50. Early stopping is possible if the effect is smaller.  

---

## 4. Possible Threats to Validity  

- **Selection Bias:** Sample may overrepresent users likely to buy Pro plan  
- **Instrumentation Effects:** Bugs in feature rollout or A/B assignment could affect data  
- **Promotions/External Factors:** Special deals or competitor campaigns could bias ARPU  
- **Seasonality:** Monthly revenue fluctuations may influence results  

---

## Tools & Techniques  

- R (tidyverse, dplyr, rpact)  
- Statistical hypothesis testing (t-test, group sequential design)  
- Sample size estimation and CUPED for variance reduction  

---

**Outcome:**  
This experiment will guide Fluent.io in deciding whether adding a Pro subscription plan effectively increases ARPU, captures value from high-engagement users, and informs pricing strategy for sustainable revenue growth.
