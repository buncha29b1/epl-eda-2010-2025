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

---

## 🛠 Methodology
1. **Data Preprocessing**
   - Load seasons 2010–11 → 2024–25 and concatenate to one table.
   - Clean types; standardize season labels and team names.
   - Derive features:
     - `total_goals = FTHG + FTAG`
     - `result ∈ {H, D, A}` from final score
     - (Optional) join standings to tag **top-5** and **bottom-5** per season.

2. **Analysis Formulation**
   - **Goals per match by season**: line plot vs. long-run mean.
   - **Distribution** of total goals: histogram / bar chart.
   - **Result shares** (H/D/A): stacked or side-by-side by season.
   - **Home vs. away scoring**: two lines + **difference** series.
   - **Top-5 vs. bottom-5**: compare result shares and scoring.

3. **Validation & QC**
   - Sanity checks (≈380 fixtures per season).
   - Inspect outliers and season breakpoints (e.g., pandemic).
   - Cross-check with known long-run EPL baselines.

---

## 🔁 Reproducibility
1) **Create a virtual environment & install** (repo root):
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

2) **Run the notebook**:
- In Jupyter: open `EPL_DA.ipynb`-> Run All
- Or execute and export to HTML:
```bash
python -m jupyter nbconvert --execute --to html "EPL_DA.ipynb"
```
This regenerates `EPL_DA.html` with fresh outputs, using the frozen environment.

---

📈 Key Findings (high level)

- Home advantage persists, though it narrowed during pandemic-affected seasons before rebounding.
- Scoring increased in the early 2020s, with a jump around 2023–24 and some reversion afterward.
- Home teams outscore away teams on average; the gap varies by season.
- Team quality matters: top-5 clubs show stronger home and away performance than bottom-5 clubs.

*(See the notebook and PDF for figures and details.)*

---

## 📚 References

*(See the References section in the PDF report for full lists of references and data sources.)*

---

## 📬 Contact
- Khoi Van: van_k1@denison.edu
