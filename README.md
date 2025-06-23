# Cost-Effectiveness Analysis of Lecanemab in South Korea

This repository contains a health economic evaluation model assessing the cost-effectiveness of **lecanemab**, an amyloid-targeting therapy, for patients with early-stage Alzheimer's disease (AD) within the **South Korean healthcare system**.

## 📌 Overview

- **Objective**: Evaluate the cost-effectiveness of lecanemab in early-stage AD  
- **Perspective**: Healthcare payer perspective / Limited societal perspective (including caregiver burden and non-medical costs)  
- **Setting**: South Korea  
- **Comparator**: Lecanemab + standard of care (SoC) vs. SoC alone  
- **Time Horizon**: Lifetime  
- **Outcome**: Incremental cost-effectiveness ratio (ICER) in KRW/QALY  

## 🧠 Model Structure

- **Type**: Markov state-transition cohort model  
- **Health States**:
  - Mild cognitive impairment due to AD
  - Mild AD
  - Moderate AD
  - Severe AD
  - Death
- **Cycle Length**: 12 months  
- **Discount Rate**: 4.5% annually for both costs and outcomes  

## 🔢 Key Inputs

### Transition Probabilities
- Derived from the **National Alzheimer’s Coordinating Center (NACC)** longitudinal data

### Costs
- **Medical & LTC Costs**: Estimated from **South Korea’s national claims database** (HIRA)
- **Drug Costs & Other Expenses**: From published literature
- **Societal Costs**: Included for limited societal perspective
  - Opportunity cost of caregiver time  
  - Out-of-pocket payments  
  - Transportation and hospital visit time costs

### Utilities
- Derived from published literature in South Korea for patients and caregivers  
- Differentiated by AD stage and care setting (community vs. institutional)

## 📊 Scenario Analyses

- **Cohort composition** (e.g., percentage of MCI vs. mild AD)
- **Age of onset**
- **Variation in drug pricing**

## ⚙️ Explanation of Excel Model – Key Sheets
- `input data/` – Includes key model inputs (e.g., costs, utilities, treatment effects) and their distributions for probabilistic analysis, tailored to the chosen perspective.
- `start page/` – Displays summary outputs for base-case and scenario analyses. Includes visualizations such as the cost-effectiveness plane and cost-effectiveness acceptability curve (CEAC).
- `cost input/` – Details cost components by perspective (payer vs. societal), care setting (community vs. institutional), and disease stage. Derived from national claims data.
- `utility input/` – Provides utility values for patients by disease stage and care setting, as well as disutility values for caregivers.
- `Tp/` – Shows transition probabilities between health states, including adjusted values that incorporate institutionalization rates.
- `no treatment/` – Presents cohort transitions per cycle for the SoC-only arm.
- `Lecanemab/` – Presents cohort transitions per cycle for the lecanemab + SoC arm.
- `no treatment_hcc/` – Shows SoC arm results with half-cycle correction applied.
- `Lecanemab_hcc/` – Shows Lecanemab + SoC arm results with half-cycle correction applied.
- `simulation/` – Contains results from the probabilistic sensitivity analysis (1,000 iterations), including distributions of cost, QALY, ICER, WTP thresholds, and the probability of being cost-effective at each threshold.
- `Mortality & Life table/` – Displays transition probabilities to death by health state based on life tables, with state-specific hazard ratios applied.
- `One-way SA/` – Summarizes results of one-way sensitivity analyses and includes a tornado diagram.

## 📈 Preliminary Results

> _The ICER of lecanemab + SoC compared to SoC alone was estimated at **198,171,820 KRW per QALY**, exceeding the conventional WTP threshold of **30 million KRW/QALY** from the healthcare payer perspective in South Korea._

---

Feel free to open an issue or contact me for questions or collaboration.
