# 🌫️ Air Pollution and Health Outcomes (WHO, 2019)

## Project Overview

This project analyzes the relationship between **air pollution exposure** and **health outcomes** across countries using open healthcare data from the **World Health Organization (WHO)**.

The analysis focuses on **PM2.5 air pollution levels** and **air-pollution-attributable death rates** at the **country level** for the year **2019**.

---

## Data Sources

The data was accessed programmatically via the **WHO Global Health Observatory (GHO) API**.

### Indicators Used

* **PM2.5 Exposure (`SDGPM25`)**
  Average national concentration of fine particulate matter (PM2.5), measured in µg/m³.

* **Air-Pollution-Attributable Death Rate (`AIR_5`)**
  Mortality rate attributable to air pollution, reported at the country level.

---

## Dataset Description

The final dataset represents a **cross-sectional snapshot for 2019** and contains **183 countries**.

Each row corresponds to **one country in one year** with the following variables:

| Column         | Description                              |
| -------------- | ---------------------------------------- |
| `country_code` | ISO country code                         |
| `year`         | Reference year (2019)                    |
| `pm25`         | Average PM2.5 exposure (µg/m³)           |
| `death_rate`   | Death rate attributable to air pollution |

---

## Data Preparation Summary

* PM2.5 data was filtered to include **national total exposure values** only.
* Death-rate data was filtered to:

  * Country-level observations
  * Both sexes combined
  * Total air-pollution causes
* The two datasets were merged using **country code** and **year**, retaining only countries with data available for both indicators.

---

## Scope and Limitations

* The analysis is **cross-sectional**, limited to the year **2019**, due to the availability of country-level mortality data.
* The dataset supports **between-country comparisons**, but not time-series trend analysis.
* Results describe **associations**, not causal relationships.

---

## Intended Use

This dataset is suitable for:

* Exploratory data analysis (EDA)
* Cross-country comparison of environmental health risks
* Visualization and policy-oriented insights
* Portfolio demonstration of real-world data ingestion and preparation

---

## One-Sentence Summary

> This project provides a country-level snapshot of PM2.5 air pollution exposure and its associated mortality impact across 183 countries in 2019.

---

## Repository Structure

```
who-air-pollution-analysis/
├── assets/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
├── README.md
```

---
## Dashboard
![dashboard](assets/dashboard.png)

## 🔑 Key Insights & Implications

### Key Insights
- 🌫️ **PM2.5 exposure varies substantially across countries**, with the highest levels concentrated in parts of the Middle East and South Asia.
- ☣️ **Air-pollution-attributable mortality does not increase proportionally with PM2.5 levels**; the observed correlation is weakly positive, indicating a complex and non-linear relationship.
- 🌍 **Countries with the highest air-pollution mortality exhibit average PM2.5 exposure nearly three times higher than the global mean** (~61 µg/m³ vs ~22 µg/m³), highlighting sustained high exposure as a critical risk factor even when it is not the highest globally.
- 🔎 **Contrasting country patterns**—such as high pollution with relatively low mortality and moderate pollution with very high mortality—underscore that exposure alone does not determine health outcomes and that vulnerability factors play a major role.

### Implications
- 🏛️ **Air quality interventions should be paired with health system strengthening**, particularly in countries where high exposure coincides with elevated vulnerability.
- 📊 **Cross-country comparisons of pollution impacts must account for demographic structure, baseline health, and healthcare capacity**, rather than relying on pollution metrics alone.
- 📈 **Reducing PM2.5 levels in high-mortality countries—even if they remain above the global average—may yield disproportionate public health benefits.**
- ⚠️ **As the analysis is cross-sectional (2019), findings reflect associations rather than causation**, reinforcing the need for longitudinal studies to assess long-term exposure effects.

### One-line takeaway
> **Reducing air pollution is essential, but minimizing its health impact depends just as critically on population vulnerability and healthcare capacity.**


---