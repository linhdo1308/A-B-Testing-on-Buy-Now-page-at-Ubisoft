# SkyConnect A/B Testing Project

## 1. Project Overview

**SkyConnect** is a customer loyalty program by a major airline that offers seat upgrades for frequent travelers.  
The company wanted to test whether a **new seat selection interface** on its booking page could increase seat upgrade purchases and revenue per user (ARPU).

This project is a **simulated A/B testing analysis** based on real airline customer data, conducted from **September 2023 to February 2024**, followed by a controlled experiment in **April 2024**.  
The analysis covers experiment design, power calculation, sample size estimation, and the application of **CUPED** (Covariate-Adjusted Pre-Experiment Data) to reduce variance and shorten test duration.

**Data Sources:**
- Historical Data (Sept 2023 – Feb 2024): [SkyConnect_data.csv](https://raw.githubusercontent.com/jefftwebb/data/refs/heads/main/SkyConnect_data.csv)  
- Test Data (April 2024): [SkyConnect_test_data.csv](https://raw.githubusercontent.com/jefftwebb/data/refs/heads/main/SkyConnect_test_data.csv)

**Objective:**  
Determine whether the new seat selection interface leads to a **statistically significant increase in average revenue per user (ARPU)** compared to the current interface.

---

## 2. Test Design

### a. A/B Test Details
- **Conversion Definition:** Revenue per customer (seat upgrade purchase)
- **Minimum Effect of Interest (MEI):** $0.50 increase in ARPU  
- **Unit of Analysis:** Customer  
- **Hypotheses:**
  - **H₀ (Null):** The new interface has no impact on ARPU.  
  - **H₁ (Alternative):** The new interface increases ARPU by at least $0.50.  

### b. Experimental Design
| Parameter | Value |
|------------|--------|
| Alpha | 0.05 |
| Power | 0.8 |
| Test Type | One-sided t-test |
| Required Sample Size | 10,329 users per group (20,658 total) |
| Estimated Duration | 78 days |
| Adjusted Sample Size with CUPED | 8,518 total |
| Adjusted Duration | 32 days |

**Variance Reduction Method:** CUPED (based on a 0.77 correlation in average monthly revenue between January and February 2024).

---

## 3. Results

### a. Traditional A/B Test
- **Effect:** -0.81  
- **95% CI:** [-1.44, -0.18]  
- **p-value:** 0.01  
- **Interpretation:** Statistically significant decrease in ARPU under the new interface.

### b. CUPED-Adjusted Analysis
- **Effect:** -0.17  
- **95% CI:** [-0.47, 0.13]  
- **p-value:** 0.26  
- **Interpretation:** No statistically significant difference after variance adjustment.

---

## 4. Recommendation

The A/B test indicates that the **new seat selection interface does not improve revenue**.  The observed decrease in ARPU suggests potential usability or pricing confusion among customers.  

Tony should **not recommend implementing the new interface** at this time.  
Further **UX research, customer behavior observation**, or **qualitative surveys** are advised to understand the drivers behind the decline before retesting an improved design.

---

## 5. Tools & Techniques

- **Programming:** R (`tidyverse`, `lubridate`, `stats`)
- **Methods:** Power analysis, t-test, CUPED adjustment, sequential enrollment simulation
- **Metrics:** ARPU, SDRPU, correlation, variance reduction


