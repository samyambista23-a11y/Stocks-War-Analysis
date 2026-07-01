# 📈 War & Markets: How Global Conflict Shapes Stock Performance

**DATA 332 Applied Business Analytics — 4 Page Showcase**
**Author:** Samyam Bista | Augustana College

---

## 📌 Project Overview

This project investigates how major geopolitical conflict events between 2025 and 2026 impacted stock prices across four key industries: **Defense**, **Energy**, **Airlines**, and **Consumer Retail**. Using R and the `tidyquant` package, live historical stock data is pulled directly from Yahoo Finance — no external CSV download required.

The analysis answers three core questions:
- Which industries consistently gain during war and which consistently lose?
- How quickly does each industry react after a conflict event?
- How long does it take each stock to recover back to its pre-war price?

---

## 🗂️ Repository Contents

| File | Description |
|---|---|
| `Samyam_Showcase_War_Stocks.qmd` | Full R/Quarto source code for the analysis |
| `Samyam_Showcase_War_Stocks.html` | Rendered HTML output with all charts and results |
| `README.md` | Project documentation |

---

## 📊 Stocks Analyzed

| Industry | Ticker | Company |
|---|---|---|
| Defense | LMT | Lockheed Martin |
| Defense | RTX | Raytheon Technologies |
| Defense | NOC | Northrop Grumman |
| Energy | XOM | ExxonMobil |
| Energy | CVX | Chevron |
| Airlines | DAL | Delta Air Lines |
| Airlines | UAL | United Airlines |
| Consumer Retail | AMZN | Amazon |
| Consumer Retail | WMT | Walmart |

---

## 🌍 Conflict Events Tracked

| Event | Date | Description |
|---|---|---|
| Israel-Iran 12-Day War | Jun 13, 2025 | Israel launches strikes on Iranian nuclear and military sites |
| US Joins Iran Conflict | Jun 22, 2025 | US strikes Iranian nuclear facilities |
| Operation Southern Spear | Nov 14, 2025 | USS Gerald R. Ford deployed to Caribbean |
| Maduro Captured | Jan 3, 2026 | US bombs Caracas — Operation Absolute Resolve |
| Full US-Iran War | Feb 28, 2026 | US-Israel escalation, Strait of Hormuz closed |

---

## 🔍 Analysis Structure

### Page 1 — Project Definition
Introduction, stock and event selection, data source description, and a summary statistics table covering price ranges and volatility for all 9 stocks.

### Page 2 — Methodology & Visualizations
- **Chart 1:** Cumulative returns by industry with vertical event markers showing exact market reaction at each conflict escalation
- **Chart 2:** 30-day rolling volatility confirming market uncertainty spikes at each conflict event

### Page 3 — Modeling & Results
- **Model 1:** 30-day return heatmap showing which industry won or lost after each conflict — green for gains, red for losses
- **Model 2:** Recovery time chart measuring how many trading days each stock took to return to its pre-war baseline price
- **Recovery Summary Table:** Average recovery days, stocks recovered, and average initial drop by industry

### Page 4 — Outcomes & Conclusions
Key findings, conclusions, and lessons learned using R — connecting the data results back to real-world investment insights.

---

## 💡 Key Findings

**1. Defense wins across every conflict.**
LMT, RTX, and NOC posted positive 30-day returns after all four conflict events and recovered the fastest — typically within 5 to 15 trading days.

**2. Not all wars hit Energy the same way.**
The Venezuela conflict barely moved Energy stocks. The US-Iran War caused a sharp spike because the Strait of Hormuz closure threatened 20% of global oil supply. Geography of conflict matters more than conflict size alone.

**3. Airlines suffer the longest.**
DAL and UAL dropped after every event and took 40 to 80+ trading days to recover. After the US-Iran War, some airline stocks never recovered within the 180-day measurement window.

---

## 🛠️ Tools & Packages

| Package | Purpose |
|---|---|
| `tidyquant` | Fetch live stock data from Yahoo Finance |
| `tidyverse` | Data manipulation and transformation |
| `ggplot2` | Charts and visualizations |
| `zoo` | Rolling volatility calculations |
| `purrr` | Functional programming for recovery time model |
| `scales` | Dollar and percent formatting |
| `knitr` | Clean table output |

---

## 🚀 How to Run

1. Clone this repository
```bash
git clone https://github.com/yourusername/stocks-war-analysis.git
```

2. Open `Samyam_Showcase_War_Stocks.qmd` in RStudio

3. Install required packages by running this once in your Console:
```r
install.packages(c("tidyquant", "tidyverse", "ggplot2", 
                   "dplyr", "lubridate", "scales", "zoo", "purrr"))
```

4. Click **Render** — the file fetches live data from Yahoo Finance automatically and produces the full HTML report

> **Note:** An internet connection is required at render time for `tq_get()` to fetch stock data.

---

## 📚 References

- [R for Data Science — Hadley Wickham](https://r4ds.hadley.nz/)
- [tidyquant Documentation](https://business-science.github.io/tidyquant/)
- [tidyquant JOSS Paper](https://joss.theoj.org/papers/10.21105/joss.01509)
- Data Source: Yahoo Finance via `tidyquant::tq_get()`

---

*Built as part of DATA 332 Applied Business Analytics at Augustana College*
