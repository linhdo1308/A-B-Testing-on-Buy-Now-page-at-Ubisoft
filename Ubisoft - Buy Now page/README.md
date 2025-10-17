# Ubisoft A/B Test — For Honor Buy Now Page Optimization

## 1. Project Overview

**Ubisoft Entertainment** is a French video game publisher headquartered in Paris, France, known for major franchises such as *Assassin’s Creed*, *Just Dance*, *Far Cry*, and *For Honor*.

This is a **simulated A/B testing project** based on a real Ubisoft experiment that increased lead generation rates by **12%**.  
The goal is to **optimize the “Buy Now” page** for *For Honor* by simplifying the purchase flow — reducing scrolling and clicks — to improve customer conversions.

---

### a. Original “Buy Now” Page (Before Testing)

<p align="center">
  <img width="500" height="500" alt="For Honor Buy Now page - original" src="https://github.com/user-attachments/assets/0569e536-4095-4984-8a9e-8bc3c4b51429" />
</p>

**User Journey:**
1. The user selects the preferred version of the game from five displayed editions.
2. The user scrolls down to choose their platform (e.g., PlayStation, Xbox, PC).
3. Finally, they click **“Place Your Order”** to proceed to checkout on the Ubisoft store.

This multi-step process required **excessive scrolling** and **extra clicks**, which likely reduced conversion rates.

---

### b. New Test Variation (Redesigned Layout)

<p align="center">
  <img width="500" height="750" alt="For Honor Buy Now page - redesigned test" src="https://github.com/user-attachments/assets/98a2f95f-218a-4b9e-a6e6-16f77c9ae4d4" />
</p>

**Key Improvements:**
- Combined edition, console, and “Order Now” options at the **top left** for easier access.  
- Added an **edition comparison section** for quicker decision-making.  
- Eliminated the need to scroll, improving **interaction speed** and **user experience**.

---

## 2. Test Design

### 🧪 a. A/B Test Details
- **Conversion Definition:** A completed purchase  
- **Minimum Effect of Interest (MEI):** +1 percentage point in conversion rate (absolute)  
- **Unit of Conversion:** User  

**Hypotheses:**
- *Null (H₀):* The new design has no impact on conversion rate  
- *Alternative (H₁):* The new design increases conversion rate by at least 1%  

---

### b. Experimental Setup
| Parameter | Value |
|------------|--------|
| α (Significance level) | 0.05 |
| Power (1 - β) | 0.8 |
| Sample Size | 6,263 users per group |
| Allocation | 50% control / 50% treatment |
| Test Duration | 24 days |

**Assumptions:**
- No seasonal or promotional effects during testing  
- Random assignment ensures unbiased comparisons  

---

## 3. Results

After running the simulated A/B test:

- **Conversion Rate Increase:** +1.4% (treatment vs. control)  
- **Statistical Test:** z-test  
- **Result:** Difference is *statistically significant*

The redesigned layout **significantly improved conversion rates**.  
**Next Step:** Present findings to stakeholders and make a *ship/no-ship* decision.

---

### Tools & Techniques
- Python (Pandas, NumPy, SciPy, Matplotlib)
- Statistical hypothesis testing (z-test)
- A/B test simulation and sample size estimation

---

**📈 Outcome:**  
Improved user conversion by simplifying the buying experience and reducing friction in the user journey.

---
