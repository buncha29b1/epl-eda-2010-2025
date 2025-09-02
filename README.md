# ⚽ English Premier League — Exploratory Data Analysis (2010–2025)

**Author:** Khoi Van

**Project Type:** Independent Data Analysis (Python / Jupyter)

---

## 🔍 Overview
With 15+ seasons of English Premier League data, this project explores **scoring trends** and **match results** over time. We analyze:
- Goals per match by season
- Distribution of total match goals
- Result shares (Home, Draw, Away)
- Home vs. away scoring and the **home-advantage gap**
- (Optional) Differences for **top-5 vs. bottom-5** clubs

The goal is a clear, reproducible EDA that answers specific questions about league-wide patterns.

---

## 🗂 Project & Structure

```
├── data/             # per-season CSVs, along with CSVs for all match fixtures and standings over the seasons.
(Note: the CSVs only have team standings from 1993-1994 to 2023-2024. For season 2024-2025, you can find it here: https://www.premierleague.com/en/tables?competition=8&season=2024&round=L_1&matchweek=-1&ha=-1)
├── .gitignore
├── EPL_DA.ipynb      # Main analysis notebook (Python/Jupyter)
├── EPL_DA.html       # Rendered notebook (open in browser)
├── Final_Report.pdf  # Narrative write-up with figures
├── README.md         # This file
└── requirements.txt  # Frozen Python environment
```
