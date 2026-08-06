# Sleep Duration and Health Indicators Analysis

Exploratory and statistical analysis of the relationship between sleep duration, demographic characteristics, health indicators, and lifestyle factors among U.S. adults using NHANES 2017–2018 data.

## Project overview

| Item | Details |
|---|---|
| Data source | National Health and Nutrition Examination Survey (NHANES) 2017–2018 |
| Final analytical sample | 4,103 adults aged 20–80 |
| Study design | Cross-sectional, descriptive and inferential analysis |
| Methods | Data cleaning, feature engineering, EDA, chi-square tests, Cramer's V |
| Tools | Python, Pandas, NumPy, SciPy, Matplotlib, Seaborn, Jupyter |

## Research question

Which demographic, health, and lifestyle factors are associated with sleep duration among U.S. adults?

Average sleep duration was calculated as a weighted weekly average of workday and weekend sleep. Participants were classified into short sleep (<7 hours), recommended sleep (7–9 hours), and long sleep (>9 hours).

## What this project demonstrates

- Integration of nine NHANES modules using the participant identifier `SEQN`
- Data-quality checks, missing-value treatment, and validation
- Feature engineering for sleep duration, BMI, physical activity, alcohol consumption, and composite health and lifestyle profiles
- Exploratory analysis supported by statistical and visual interpretation
- Chi-square tests of independence and Cramer's V effect sizes
- Clear distinction between association and causation in cross-sectional data
- Reproducible file loading with portable project-relative paths

## Key findings

- **60.0%** of participants were within the recommended 7–9-hour sleep range; **24.7%** had short sleep and **14.1%** had long sleep.
- Women slept approximately **0.31 hours more** than men on average (7.90 vs. 7.60 hours).
- Gender was associated with sleep-duration category: **χ²(2) = 36.49, p < 0.001, Cramer's V = 0.095**.
- Recommended sleep increased from **53.7%** in the lowest socioeconomic group to **68.1%** in the highest, while long sleep decreased from **20.7%** to **7.8%**.
- Lifestyle profile was associated with sleep duration (**χ²(4) = 20.92, p < 0.001, V = 0.051**), although the effect was weak.
- All statistically significant associations had weak effect sizes (**V < 0.10**), reinforcing that sleep duration is multifactorial.
- Because NHANES is cross-sectional, these results describe associations and do not establish causality.

## Repository contents

- [English notebook — primary portfolio version](notebooks/sleep_health_analysis_en.ipynb)
- [Spanish notebook — original complete analysis](notebooks/analisis_sueno_salud_es.ipynb)
- [Spanish research report](reports/research_report_es.pdf)
- [Spanish presentation](presentation/sleep_health_analysis_presentation_es.pdf)
- [Data documentation](data/README.md)

## Repository structure

```text
sleep-health-analysis-nhanes/
├── data/
│   ├── README.md
│   ├── DEMO_J.xpt
│   ├── SLQ_J.xpt
│   ├── BMX_J.xpt
│   ├── GHB_J.xpt
│   ├── BPX_J.xpt
│   ├── HDL_J.xpt
│   ├── PAQ_J.xpt
│   ├── SMQ_J.xpt
│   └── ALQ_J.xpt
├── notebooks/
│   ├── sleep_health_analysis_en.ipynb
│   └── analisis_sueno_salud_es.ipynb
├── presentation/
│   └── sleep_health_analysis_presentation_es.pdf
├── reports/
│   └── research_report_es.pdf
├── .gitignore
├── README.md
└── requirements.txt
```

The English notebook is the primary portfolio version. The Spanish notebook, report, and presentation preserve the original project and its full academic context.

## Run locally

```bash
git clone https://github.com/Ajrema/sleep-health-analysis-nhanes.git
cd sleep-health-analysis-nhanes
pip install -r requirements.txt
jupyter notebook
```

Open either notebook from the `notebooks/` directory. The loading logic detects whether Jupyter was launched from the repository root or from `notebooks/`, so the files in `data/` can be found without editing private computer paths.

## Data source and methodology

The raw SAS Transport files come from the public [CDC/NCHS NHANES 2017–2018 documentation](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?BeginYear=2017). See [data/README.md](data/README.md) for the module descriptions.

The analysis uses survey data collected at one point in time. Statistical significance is interpreted alongside effect size, and no causal claims are made.

## Author

**Alejandro Requena**  
Junior Data Analyst | SQL · Python · Power BI  
[LinkedIn](https://www.linkedin.com/in/alejandro-requena-/) · [GitHub](https://github.com/Ajrema)
