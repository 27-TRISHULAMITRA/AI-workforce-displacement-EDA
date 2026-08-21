# Global AI Workforce Displacement Analysis (2020–2026)

An exploratory data analysis of AI adoption and workforce displacement across **80 countries, 12 regions, and 10 industry sectors from 2020–2026**, examining where automation is advancing fastest, who is being displaced, and whether new roles are keeping pace.

> **Data Note**
>
> This dataset is disclosed by its source as **research-calibrated synthetic data**, built to reflect patterns from real published research (WEF Future of Jobs 2025, McKinsey State of AI 2025, OECD Employment Outlook 2025, BLS O\*NET, Layoffs.fyi, PwC AI Jobs Barometer, IMF WEO). **It is directionally realistic but not observed real-world data** — treat findings as illustrative scenario analysis, not verified fact, when presenting externally.

---

## Executive Summary

**AI adoption and workforce displacement are rising together, and displacement is now outpacing job creation everywhere.**

Global AI adoption climbed steadily from **54% in 2020 to 82% in 2026**, and workforce displacement rose in near lockstep — from **2.7% to 9.0%** of the workforce over the same period.

Critically, **all 80 countries in the dataset show workforce displacement exceeding new-role creation**, meaning the "AI creates as many jobs as it destroys" narrative does not hold in this data at any point in the 2020–2026 window.

Risk is concentrated: **Administrative & Clerical work carries both the highest automation risk (0.79) and the highest displacement (9.2%)**, while wealthier, high-adoption countries (Singapore, Israel, the US, the Nordics) are simultaneously the furthest ahead on adoption **and** among the most exposed to the net displacement gap — suggesting the countries best-positioned to capture AI's productivity gains are also the ones facing the earliest workforce transition pressure.

---

## Business Questions → Solution

**Q1: Is AI adoption actually causing workforce displacement, or are the two unrelated?**

The data shows a **strong positive correlation (r = 0.69)** between AI adoption and workforce displacement, and **both metrics rose together every year from 2020 to 2026**. This is scenario-modeled data, so it should be read as a plausible causal pattern consistent with published research, not statistical proof of causation — but it is strong enough to justify workforce planning now.

**Q2: Which parts of the business are most exposed to displacement risk?**

**Administrative & Clerical, Manufacturing & Industry, and Retail & E-Commerce** carry the highest automation risk scores and the highest actual displacement rates, while **Healthcare & Education are the most insulated**. Leadership should prioritize reskilling investment in the first three sectors well ahead of the rest.

**Q3: Are new roles created by AI offsetting the jobs it displaces?**

**No** — in every one of the 80 countries analyzed, the percentage of workforce displaced exceeds the percentage of new roles created, producing a **negative net workforce change in every industry**. Role creation is not currently a sufficient offset anywhere in the dataset, and reskilling/redeployment programs need to close that gap directly rather than assuming the market will self-correct.

---

## Key Metrics at a Glance

| Metric | Value | What It Means |
|---|---|---|
| **Countries covered** | 80 | Broad global coverage across income levels and regions |
| **Industry sectors** | 10 | From Technology to Healthcare to Administrative & Clerical |
| **Global AI adoption, 2020 → 2026** | 54.3% → 81.7% | AI adoption nearly doubled its distance to full saturation in 6 years |
| **Global workforce displacement, 2020 → 2026** | 2.7% → 9.0% | Displacement more than tripled over the same period |
| **AI adoption ↔ displacement correlation** | r = 0.69 | Strong positive relationship — adoption and displacement move together |
| **GDP per capita ↔ AI adoption correlation** | r = 0.70 | Wealthier economies adopt AI faster |
| **Countries where displacement > new roles created** | 80 of 80 (100%) | No country in the dataset shows net-positive job creation from AI |
| **Highest-risk industry** | Administrative & Clerical (0.79 risk, 9.2% displaced) | Clear #1 priority for reskilling investment |
| **Lowest-risk industry** | Healthcare & Life Sciences (0.22 risk, 2.1% displaced) | Most insulated sector in the dataset |
| **Top AI-adopting countries** | Singapore, Israel, USA, Sweden, Denmark | Small, high-income, tech-forward economies lead adoption |
| **Highest AI skill wage premium** | High Income countries (39.4%) | AI-fluent workers command the largest pay premium in wealthy economies |

---

## Project Overview

| | |
|---|---|
| **Project Name** | Global AI Workforce Displacement Analysis |
| **Objective** | Quantify how AI adoption relates to workforce displacement, job creation, wages, and policy readiness across countries, regions, and industries |
| **Dataset** | AI Workforce Displacement Global 2020–2026 (20,800 records, synthetic/research-calibrated) |
| **Tools Used** | Python — Pandas, NumPy, Matplotlib, Seaborn (Jupyter) |
| **File Type** | Jupyter Notebook (`.ipynb`) + CSV |

---

## Business Problem

**Executive and workforce-planning leadership need to understand, at a global level, where AI adoption is creating the greatest workforce disruption** — by country, region, and industry — and whether job creation is keeping pace with job displacement, in order to prioritize reskilling investment and policy response before disruption peaks.

---

## Solution

This project answers that need by combining **descriptive statistics, correlation analysis, and industry/region/country-level aggregation** across a 20,800-record dataset spanning 2020–2026.

Instead of a single global adoption number, the analysis breaks displacement down by **industry, income group, gender, and geography**, and directly tests whether new-role creation offsets displacement — surfacing a clear, prioritized answer (**it does not, anywhere in the dataset**) that leadership can act on immediately rather than a vague directional trend.

---

## Dataset

Each record represents one country–industry–quarter observation, with fields including:

`country` · `region` · `income_group` · `year` · `quarter` · `industry_sector` · `sector_automation_risk_score` · `gdp_per_capita_usd` · `ai_adoption_index` · `pct_sector_workforce_displaced` · `pct_sector_workforce_new_roles_created` · `net_workforce_change_pct` · `ai_cited_layoff_announcements` · `ai_skill_wage_premium_pct` · `pct_workforce_female` · `pct_displaced_roles_female` · `reskilling_programs_count` · `govt_ai_policy_score_1_to_10` · `ai_tool_adoption_pct`

---

## Analysis Workflow

### 1. Dataset Overview

Shape, data types, summary statistics, unique values, missing values, and duplicate checks confirm **a clean 20,800-row, 23-column dataset** covering 80 countries and 10 industries.

### 2. Adoption & Displacement Benchmarking

Average AI Adoption Index, **top-10 adopting countries**, and region-level adoption averages establish who is leading and lagging globally.

### 3. Industry Risk Profiling

Average workforce displacement and automation risk score by industry sector identify **Administrative & Clerical, Manufacturing & Industry, and Retail & E-Commerce** as the highest-risk sectors.

### 4. Time Trend Analysis

Year-over-year AI adoption and displacement trends (2020–2026) confirm **both metrics rising in tandem**, with adoption nearly 82% and displacement nearing 9% by 2026.

### 5. Correlation & Relationship Testing

A full correlation matrix and heatmap, plus scatter plots (GDP vs. AI Adoption, AI Adoption vs. Displacement, Female Workforce vs. Female Displacement), **quantify the strength of each relationship**.

### 6. Displacement vs. Job Creation Gap

A merged comparison of displacement and new-role creation by country finds that **all 80 countries** show displacement exceeding new-role creation — **the single most important finding in the analysis**.

### 7. Equity & Policy Lens

Wage premium by income group, AI tool adoption by income group, and government AI policy score by region examine **whether the benefits and preparedness for AI adoption are evenly distributed**.

---

## Visualizations & Insights

### 1. AI Adoption Index Distribution

<img width="1498" height="679" alt="Screenshot 2026-08-20 165730" src="https://github.com/user-attachments/assets/282ba560-7d01-4c12-ae52-6273a69c837c" />



---

**Statistical Insight:** Left-skewed distribution (skew = -0.71, mean 0.69 < median 0.72). Most observations cluster on the high end, between roughly 0.70 and 0.90, with a smaller tail of low-adoption outliers.

**Business Insight:** The typical country-industry combination in this dataset is **already a high-adopter, not a laggard** — full-scale AI adoption is closer to "the norm" than "the frontier."

**Business Recommendation:** Treat low-adoption outliers as the priority segment for enablement support, since the majority of the market has already moved past the early-adoption phase.

**Conclusion:** Global AI adoption is broadly mature within this dataset, with a shrinking minority still catching up.


---

### 2. Workforce Displacement Distribution


<img width="1471" height="717" alt="Screenshot 2026-08-20 165818" src="https://github.com/user-attachments/assets/48048eec-bf2a-4adb-82e4-b6ad2e070bd9" />


---

**Statistical Insight:** Right-skewed distribution (skew = 1.51, mean 5.6% > median 4.3%). The bulk of observations cluster under 5% displacement, with a long tail stretching toward much higher values.

**Business Insight:** Severe displacement is **not the norm** — it's a concentrated problem in a smaller number of country-industry combinations, which is actually good news for prioritization.

**Business Recommendation:** Focus reskilling and workforce transition budgets on the long-tail outliers rather than spreading resources evenly, since most segments are only mildly affected.

**Conclusion:** Displacement risk is concentrated, not universal — targeted intervention will be far more efficient than a blanket policy.

### 3. Records by Region (Bar Chart)

**Business Insight:** **Europe (5,200 records)**, Latin America and Africa (3,380 each) have the deepest data coverage, while North America, Oceania, Europe/Asia, and Central Asia are comparatively thin (520 each), and Middle East/Africa is thinnest (260).

**Business Recommendation:** Interpret North America and Oceania findings directionally rather than definitively, given their smaller sample sizes relative to Europe and Africa.

**Conclusion:** Coverage is uneven across regions, which should temper confidence in region-level comparisons involving the smaller-sample regions.


---

### 4. AI Adoption by Region 

<img width="933" height="747" alt="Screenshot 2026-08-20 170022" src="https://github.com/user-attachments/assets/862ddce2-6c35-4f26-9c39-359b644bb606" />


---

**Business Insight:** **North America leads adoption (~0.86)**, followed by East Asia (~0.85) and Oceania (~0.83). **South Asia (~0.57) and Africa (~0.54) lag furthest behind.**

**Business Recommendation:** Global AI strategy and policy investment should explicitly budget for a **multi-speed rollout** — South Asia and Africa will need materially different timelines and support than North America or East Asia.

**Conclusion:** AI adoption is regionally uneven, tracking broadly with economic development level.

---

### 5. AI Adoption Over Time 2020–2026


<img width="750" height="745" alt="Screenshot 2026-08-20 170259" src="https://github.com/user-attachments/assets/83fc1778-d84e-4e94-a1e1-6d808a71fe0d" />

---

**Statistical Insight:** Adoption rose from **54.3% (2020) to 81.7% (2026)** — a steady, consistent upward trend with no year-over-year decline.

**Business Insight:** Adoption growth shows **no sign of plateauing** within this window, meaning the window for "early mover advantage" is closing as adoption approaches saturation.

**Business Recommendation:** Organizations still below the ~80% adoption mark should treat the next 1–2 years as the **last practical window** to close the gap before AI capability becomes table stakes rather than a differentiator.

**Conclusion:** AI adoption has grown consistently and rapidly across the full 2020–2026 period.


---

### 6. Workforce Displacement Over Time 2020-2026


<img width="765" height="744" alt="Screenshot 2026-08-20 170329" src="https://github.com/user-attachments/assets/0d542040-b380-4157-a607-4e3952d39dd9" />

---

**Statistical Insight:** Displacement rose from **2.7% (2020) to 9.0% (2026)**, more than tripling and tracking the adoption curve closely (r = 0.69 between the two series).

**Business Insight:** Displacement is **accelerating in parallel with adoption, not lagging behind it** — meaning workforce impact is a current, live issue rather than a future risk to plan for later.

**Business Recommendation:** Workforce transition and reskilling programs should scale on the same timeline as AI adoption initiatives, not be treated as a downstream, delayed response.

**Conclusion:** Displacement has grown in near lockstep with adoption, confirming the two are tightly linked over time.

---

### 7. Correlation Heatmap


<img width="1086" height="757" alt="Screenshot 2026-08-20 170644" src="https://github.com/user-attachments/assets/13ff1d86-7a6d-45a1-b877-ec0dce69bac7" />

---

**Statistical Insight:** The strongest relationships in the matrix are **AI Adoption ↔ GDP per Capita (r = 0.70)**, **AI Adoption ↔ Workforce Displacement (r = 0.69)**, and **Female Workforce Share ↔ Female Displacement Share (r = 0.99, near-perfect)**.

**Business Insight:** Displacement risk is **not randomly distributed** — it is structurally tied to how wealthy and how AI-adopting a country/industry already is, and displaced roles mirror the existing gender composition of the workforce almost exactly.

**Business Recommendation:** Use GDP and adoption level as **leading indicators** to forecast which markets will see rising displacement next, rather than waiting for displacement data to arrive.

**Conclusion:** The dataset's key relationships are strong and consistent, giving confidence that adoption, wealth, and displacement move together predictably.

---


### 8. GDP per Capita vs. AI Adoption Index (Scatter Plot)


<img width="1038" height="727" alt="Screenshot 2026-08-20 170725" src="https://github.com/user-attachments/assets/f8dcb957-21c3-458f-86fd-e78c4fce3f5a" />


---

**Statistical Insight:** Clear positive relationship (r = 0.70) — as GDP per capita rises from near $0 to $100,000+, AI adoption trends upward with it.

**Business Insight:** AI adoption is, at this stage, **still largely a function of national wealth** — lower-income economies face a structural adoption disadvantage, not just a preference gap.

**Business Recommendation:** International development and technology-transfer programs should treat AI enablement in lower-income countries as an **economic equity issue**, not only a technology rollout issue.

**Conclusion:** Wealthier economies adopt AI faster, reinforcing existing global economic divides rather than closing them.

---

### 9. AI Adoption vs. Workforce Displacement 

<img width="1124" height="743" alt="Screenshot 2026-08-20 170758" src="https://github.com/user-attachments/assets/f770ea2f-20ac-4df3-bfa8-952f2b83b00c" />


---

**Statistical Insight:** Positive but non-linear relationship (r = 0.69) — displacement stays modest through low-to-moderate adoption, then rises more steeply at higher adoption levels.

**Business Insight:** There appears to be a **"tipping point"** in adoption beyond which displacement accelerates, rather than a smooth, proportional increase from the start.

**Business Recommendation:** Monitor sectors/countries as they approach that higher-adoption tipping zone specifically, since that's where displacement risk compounds fastest.

**Conclusion:** Displacement risk is not just about how much AI is adopted, but where a country/industry sits on the adoption curve.

---


### 10. Workforce Displacement by Industry 


<img width="966" height="701" alt="Screenshot 2026-08-20 170823" src="https://github.com/user-attachments/assets/78e09a10-c3f9-41ca-89d9-2b61426b7029" />


---

**Business Insight:** **Administrative & Clerical shows the highest median displacement** and the widest spread of outliers (up to ~30%), followed by Manufacturing & Industry and Transportation & Logistics with similarly heavy outlier clusters.

**Business Recommendation:** Prioritize Administrative & Clerical roles first in any reskilling roadmap — both the typical case and the worst-case outcomes are worse here than in any other sector.

**Conclusion:** Displacement risk is heavily concentrated in a small number of industries, led clearly by Administrative & Clerical.


---

### 11. Automation Risk by Industry 

<img width="760" height="744" alt="Screenshot 2026-08-20 171248" src="https://github.com/user-attachments/assets/d24319af-59d6-41c3-9225-b0623e943185" />



---

**Business Insight:** **Administrative & Clerical carries the highest automation risk score (~0.79)**, followed by Manufacturing & Industry (~0.72), then Retail & E-Commerce (~0.67) and Transportation & Logistics (~0.65) close behind each other. **Healthcare & Life Sciences (~0.22) and Education & Research (~0.27) are the most insulated.**

**Business Recommendation:** Rank reskilling investment in this order — Administrative & Clerical, Manufacturing, Retail/Transportation — while treating Healthcare and Education as lower-priority for displacement mitigation (though still worth monitoring).

**Conclusion:** Automation risk closely mirrors actual displacement rates by industry, validating the risk score as a reliable early-warning metric.

---

### 12. Top 10 Countries by AI Adoption 


<img width="828" height="660" alt="Screenshot 2026-08-20 171019" src="https://github.com/user-attachments/assets/989651ff-9935-47e9-b0ef-ab72eefa4703" />



---

**Business Insight:** **Singapore (90.5%), Israel (88.6%), and the United States (88.5%) lead global adoption**, with Sweden, Denmark, Switzerland, South Korea, Finland, China, and Norway rounding out the top 10 — all high-income or upper-middle-income economies.

**Business Recommendation:** Benchmark national AI policy and enterprise strategy against these top-10 markets, since they represent the practical "ceiling" of current adoption rather than a theoretical maximum.

**Conclusion:** AI adoption leadership is concentrated among a small group of wealthy, technology-forward nations.

---


### 13. AI Skill Wage Premium by Income Group 

<img width="1136" height="628" alt="Screenshot 2026-08-20 171113" src="https://github.com/user-attachments/assets/f33b4102-2ffa-487e-95a4-fe8988452ef5" />



---

**Business Insight:** **High-income countries capture the largest share of the AI wage premium** (28.3% of the combined total, averaging 39.4% wage uplift), while Low Income countries capture the smallest share (22.3%, averaging 31.0% uplift).

**Business Recommendation:** Expect AI-skills training to **widen wage inequality** between income groups unless paired with deliberate investment in AI-skills access for lower-income economies.

**Conclusion:** The financial upside of AI fluency is not distributed evenly — wealthier economies benefit disproportionately.

---

### 14. Female Workforce Share vs. Female Displacement Share 

<img width="1098" height="711" alt="Screenshot 2026-08-20 171144" src="https://github.com/user-attachments/assets/354c7d9c-cf29-4aad-930e-5628137535f8" />



---

**Statistical Insight:** Near-perfect positive correlation (**r = 0.99**) — as the female share of a sector's workforce rises, the female share of displaced roles rises proportionally with it.

**Business Insight:** Displacement is **not disproportionately targeting women** beyond their existing workforce representation — the pattern is proportional, not discriminatory, based on this data.

**Business Recommendation:** Frame workforce transition support in gender-neutral, sector-based terms rather than gender-targeted terms, since the driver appears to be sector composition, not gender itself.

**Conclusion:** Female displacement mirrors female workforce share almost exactly, indicating sector mix — not gender bias — is the primary driver in this dataset.

---

### 15. AI Tool Adoption by Income Group 

<img width="904" height="623" alt="Screenshot 2026-08-20 171202" src="https://github.com/user-attachments/assets/97cec029-9990-426b-bdec-067e5e62343c" />

---

**Business Insight:** **High-income countries hold the largest share of AI tool adoption** (32.2% of the combined total, averaging 44.3% tool adoption), while Low Income countries hold the smallest share (19.2%, averaging 26.4%).

**Business Recommendation:** Prioritize affordable AI tooling access programs for Lower-Middle and Low Income economies to prevent the adoption gap from widening further as AI tools become more central to competitiveness.

**Conclusion:** Practical, day-to-day AI tool usage — not just strategic adoption — is also concentrated in wealthier economies, reinforcing the same equity gap seen throughout the dataset.

---

## Skills Demonstrated

- **Large-scale exploratory data analysis** (20,800 rows, 23 columns) using Pandas and NumPy.
- **Multi-dimensional `groupby` aggregation** across country, region, industry, and income group.
- **Correlation analysis and heatmap visualization** to quantify relationships between adoption, displacement, and GDP.
- **Distribution analysis** (histograms, boxplots) to characterize skew in adoption and displacement.
- **Multi-table merge logic to directly test displacement vs. job-creation gaps at the country level.
-**Translating statistical findings into an executive-ready summary, business Q&A, and prioritized recommendations.




## Repository Contents  

-README.md

-ai_workforce_displacement_global_2020_2026.ipynb

-ai_workforce_displacement_global_2020_2026.csv


## How to Use

-Clone/download this repository.

-Open ai_workforce_displacement_global_2020_2026.ipynb in Jupyter Notebook, JupyterLab, or Google Colab.

-Ensure the CSV path in the notebook points to your local copy of ai_workforce_displacement_global_2020_2026.csv.

-Run all cells sequentially — each analysis question includes inline statistical commentary.
