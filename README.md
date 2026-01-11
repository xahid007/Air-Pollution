Here is a **clean, professional `README.md`** you can copy-paste directly into your GitHub repo.
It’s **concise, clear, portfolio-ready**, and written exactly the way recruiters expect.

---

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
│
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
├── README.md
```

---