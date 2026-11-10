<h1>
  <a href="README.md"><img align="right" src="https://raw.githubusercontent.com/levg00/levg00/main/assets/lang-en-active-clean.svg" alt="EN"></a>
  <a href="README.ru.md"><img align="right" src="https://raw.githubusercontent.com/levg00/levg00/main/assets/lang-ru-inactive-clean.svg" alt="RU"></a>
  MobiCar — product funnel analysis
</h1>

[↩ Applied projects](https://github.com/levg00/levg00/blob/main/portfolio/applied.en.md)

Analysis of the customer journey from app installation to the first ride, identifying a conversion bottleneck and hypotheses for recovering conversion.

Case study completed as part of the selection process for an internship at **T-Bank**.

#### 📓 [Code and calculations](notebooks/funnel-analysis.ipynb) · 📄 [Solution](materials/report.ru.pdf)

## 🎯 Task

Use eight weeks of data to identify the funnel stage where conversion fell, show the problem in a single chart, and propose further checks.

**Case context:** car search changed, while installations increased. The share of registered users returning to the app a week later remained unchanged; reviews did not worsen.

📋 [Full case brief](materials/task.ru.md)

## ⚡ What I did and tools used

- **Python / pandas:** calculated conversion for five transitions and the full funnel, then compared weekly trends.
- **Matplotlib:** built a chart and highlighted the problematic stage in color.
- **Product analysis:** formulated hypotheses about the causes of the decline and proposed a plan to test them.

## 📉 Analysis result

**Registration-to-search conversion dropped by 21.60 percentage points between weeks six and seven.** This stage should be investigated first.

[![Conversion trends over eight weeks: a drop between registration and search](assets/funnel.ru.png)](notebooks/funnel-analysis.ipynb)

| Metric | Week 6 | Week 7 | Change |
| :--- | :--- | :--- | :--- |
| Registration → Search | 70.95% | 49.35% | −21.60 pp |
| Installation → First ride | 27.48% | 18.54% | −8.94 pp |

The largest drop occurs between weeks six and seven. Let’s formulate hypotheses to explain this change.

## 💡 Hypotheses and investigation plan

| Hypothesis | What to check |
| :--- | :--- |
| The search interface became less intuitive | Actions after registration, the path to search, and user feedback |
| Search performance deteriorated | Errors and technical failures |
| Additional barriers appeared | The path to search and differences across cities, devices, and app versions |

Additionally, an **A/B test** to evaluate the impact of the search changes.

<details>
<summary><b>⚙️ How conversion was calculated</b></summary>

**Daily conversion = users reaching the next stage / users at the previous stage × 100%.**

For the chart, I averaged daily rates within each week.

**Additional check:** recalculating rates using total weekly user counts also showed a drop at the search transition. The [notebook](notebooks/funnel-analysis.ipynb) compares the two methods.

</details>

<details>
<summary><b>📁 Data used</b></summary>

- **56 days, eight weeks:** installations, registrations, searches, car views, bookings, and first rides.
- **CSV and Excel:** identical data restored from a saved block of numbers. The calculations matched the original notebook. [Data details](data/README.md).

</details>

## 📂 Materials

- [Code, calculations, and chart — Jupyter Notebook](notebooks/funnel-analysis.ipynb).
- [Chart and findings on one page — PDF](materials/report.ru.pdf).
- [Case brief](materials/task.ru.md).
- [CSV data](data/funnel-daily.csv) · [Excel data](data/funnel-data.xlsx).

<details>
<summary><b>Files</b></summary>

```text
README.md                        — description in English
README.ru.md                     — description in Russian
notebooks/funnel-analysis.ipynb   — code and calculations
data/funnel-daily.csv             — daily data
data/funnel-data.xlsx             — the same data in Excel
data/README.md                    — data provenance
assets/funnel.ru.png              — conversion chart
materials/task.ru.md              — case brief
materials/report.ru.pdf           — original chart and findings
materials/original-analysis.ipynb — original notebook
requirements.txt                 — dependencies
```

</details>
