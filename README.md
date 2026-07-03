# 📊 Website Traffic Analysis

Analysis of a 4-week Google Analytics 4 (GA4) export to understand where website traffic comes from, how engaged visitors are, and when they show up — with a reproducible Python/Jupyter workflow and a formula-driven Excel dashboard.

## Overview

This project explores hourly website traffic data (Apr 6 – May 3, 2024) across traffic-source channels (Direct, Organic Search, Organic Social, Referral, Organic Video, Email). It answers:

- Which channels drive the most users and sessions?
- How does engagement (rate, time on site, events/session) differ by channel?
- What daily, hourly, and day-of-week patterns exist in traffic?
- Which channels are high-performing vs. low-performing, on volume *and* quality?

## Dataset

- **Source:** GA4 export, `website_data.csv`
- **Grain:** one row per channel per hour
- **Fields:** `Channel`, `Date + hour`, `Users`, `Sessions`, `Engaged sessions`, `Avg engagement time per session`, `Engaged sessions per user`, `Events per session`, `Engagement rate`, `Event count`

## Repo Contents

| File | Description |
|---|---|
| `Website_Traffic_Analysis.ipynb` | Full analysis notebook (pandas, matplotlib, seaborn) — cleans the data, builds channel/time breakdowns, and renders a one-page summary dashboard |
| `website_data.csv` | Raw GA4 export used by the notebook |
| `website_traffic_analysis.xlsx` | Excel version — Raw Data, Channel Summary, Daily Trend, Hourly Pattern, and Day of Week sheets, all driven by formulas, plus a chart-based Dashboard tab |

## How to Run

```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Website_Traffic_Analysis.ipynb
```

Run all cells top to bottom. Swap in a newer `website_data.csv` (same column layout) and re-run to refresh the analysis.

## Key Findings

- **Organic Social** is the top traffic source (~37% of sessions) but converts that volume into engagement at a below-average rate.
- **Referral** traffic is much smaller in volume but has the best engagement rate and longest average session time of the major channels — likely high-intent visitors.
- **Organic Video**, despite tiny volume, has the single highest engagement rate — a potential growth channel worth testing further.
- Traffic is unevenly distributed across hours and days of the week, useful for timing campaigns or releases.

## Tech Stack

`Python` · `pandas` · `matplotlib` · `seaborn` · `Jupyter` · `Excel` (`openpyxl`)
---
*Inspired by [The iScale's Website Data Analysis Project](https://github.com/TheiScale/YouTube-Video-Notes/tree/main/Website%20Data%20Analysis%20Project).*
