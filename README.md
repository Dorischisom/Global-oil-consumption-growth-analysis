# Global-oil-consumption-growth-analysis

# 🌍 Which Countries Have the Fastest Growth in Oil Consumption (2015–2024)?

## 📌 Business Problem

Global oil demand continues to evolve due to industrialization, urbanization, population growth, and economic expansion. While some countries dominate oil consumption in absolute terms, others may be experiencing faster growth rates.

**This analysis answers the question:**

**Which countries recorded the fastest growth in oil consumption between 2015 and 2024?**

**I examined both:**

- 📈 Growth speed (CAGR – Compound Annual Growth Rate)
- 📊 Growth size (Absolute increase in TWh)

## 📂 Data Source

**Oil consumption data (TWh) was obtained from:**

- **Our World in Data (OWID) Energy Dataset**

**Time period analyzed:**
- 2015–2024

**Data structure:**
- Country
- Year
- Oil consumption (TWh)

## Tools Used
- Python (Pandas, NumPy)
- Matplotlib / Seaborn
- Jupyter Notebook

## 🧹 Data Cleaning & Preparation (Python)

#### The following steps were performed:

- Removed aggregate regions (World, Africa, Europe, etc.)
- Kept only valid 3-letter country ISO codes
- Filtered years to 2015–2024
- Reshaped data from long to wide format
- Calculated growth metrics:
  - Absolute change (TWh)
  - Percentage change (%)
  - CAGR (%)


##### Growth Formula Used

```wide["abs_change_twh"] = wide[2024] - wide[2015]```
```wide["pct_change_%"] = (wide[2024] / wide[2015] - 1) * 100```
```wide["cagr_%"] = ((wide[2024] / wide[2015]) ** (1/9) - 1) * 100```

CAGR was calculated over a 9-year period (2015–2024).

## 📊 Analysis & Visualizations

#### 1️⃣ Fastest Growing Countries (CAGR %)

This visualization ranks countries by Compound Annual Growth Rate (CAGR).

**📌 What this measures:**

Growth speed relative to starting consumption levels.


#### Key Insight

- Emerging and developing economies dominate the top positions.
- Countries such as Bangladesh, Uzbekistan, and Vietnam recorded the fastest percentage growth.
- High growth rates often reflect:
- Rapid industrialization
- Expanding transportation demand
Urban population growth

⚠️ However, fast growth does not necessarily mean large total consumption.

#### 2️⃣ Countries with the Largest Absolute Increase (TWh)

This visualization ranks countries by total increase in oil consumption volume.

**📌 What this measures:**

Total additional oil demand added to the global system.

#### Key Insight
- China and India dominate absolute increases.
- Even moderate percentage growth in large economies results in significant global impact.
- Scale matters more than speed when assessing global oil demand influence.


#### 3️⃣ Oil Consumption Trend (Top 5 Fastest Growers)

A time-series visualization shows year-by-year changes for the top-growing countries.

#### Key Insight
- Growth is generally steady rather than volatile.
- Most countries experienced a dip around 2020 (COVID-19 shock).
- Post-2021 recovery suggests structural demand growth rather than short-term spikes.

### Overall Findings
- Fastest-growing countries are mostly emerging economies.
- Largest contributors to global demand remain large economies.
- Growth speed and growth size tell different stories.
- Oil demand growth remains resilient despite pandemic disruptions.
- Structural demand expansion is evident in developing regions.

### ⚠️ Limitations

The analysis focuses solely on oil consumption (TWh), not total energy mix.

No adjustment was made for:
- Population growth
- GDP growth
- Energy efficiency improvements

- CAGR assumes smooth growth, which may hide year-to-year volatility.

- 2024 data may be provisional or partially reported.

- This analysis does not account for policy shifts toward renewable energy.


## Conclusion
Between 2015 and 2024, oil consumption growth patterns reveal a dual dynamic:

- Smaller emerging economies are growing fastest in percentage terms.

- Large economies continue to drive the majority of absolute demand growth.

Understanding both dimensions — growth speed and growth size — is critical for:

- Energy market forecasting
- Investment strategy
- Infrastructure planning
- Climate and transition risk assessment

Oil demand remains structurally embedded in developing economies, even as global energy transition efforts accelerate.

