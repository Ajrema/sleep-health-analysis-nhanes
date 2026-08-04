# Sleep Duration and Health Indicators Analysis

Exploratory and statistical analysis of the relationship between sleep duration, demographic characteristics, health indicators, and lifestyle factors among U.S. adults using NHANES 2017–2018 data.

## Project snapshot

| Item | Details |
|---|---|
| Dataset | National Health and Nutrition Examination Survey (NHANES) 2017–2018 |
| Final sample | 4,103 adults aged 20–80 |
| Main language | Python |
| Analysis | Data cleaning, feature engineering, EDA, Chi-square tests, Cramer's V |
| Tools | Pandas, NumPy, Matplotlib, Seaborn, SciPy, Jupyter |

## Business question

Which demographic, health, and lifestyle factors are associated with sleep duration among U.S. adults?

The project classifies participants into short, recommended, and long sleep groups and evaluates how those groups differ across demographic characteristics, health profiles, and lifestyle patterns.

## What this project demonstrates

- Integration of multiple NHANES modules through the participant identifier `SEQN`
- Data quality checks, missing-value treatment, and validation
- Feature engineering for average sleep duration, sleep categories, BMI, alcohol consumption, physical activity, and composite profiles
- Exploratory analysis with clear statistical and visual interpretation
- Chi-square tests of independence and Cramer's V effect sizes
- Communication of findings without implying causality from cross-sectional data

## Key findings

- Most statistically significant relationships had weak or very weak effect sizes, showing that sleep is a multifactorial outcome.
- Short sleep was more prevalent among men than women.
- Sleep duration patterns varied by age, race/ethnicity, and socioeconomic position.
- Participants with recommended sleep generally showed more favorable patterns for daytime sleepiness and selected sleep-related symptoms.
- Because NHANES is cross-sectional, these findings describe associations and do not establish cause and effect.

## Repository structure

```text
sleep-health-analysis-nhanes/
├── README.md
├── notebooks/
│   ├── sleep_health_analysis_en.ipynb
│   └── analisis_sueno_salud_es.ipynb
├── reports/
│   └── research_report_es.pdf
└── requirements.txt
```

The English notebook is the primary portfolio version. The original Spanish notebook and report are included as supporting material.

## Run locally

```bash
git clone https://github.com/Ajrema/sleep-health-analysis-nhanes.git
cd sleep-health-analysis-nhanes
pip install -r requirements.txt
jupyter notebook
```

## Methodological note

The analysis uses survey data collected at one point in time. Statistical significance is interpreted together with effect size, and no causal claims are made.

## Author

**Alejandro Requena**  
Junior Data Analyst | SQL · Python · Power BI  
[LinkedIn](https://www.linkedin.com/in/alejandro-requena-/) · [GitHub](https://github.com/Ajrema)
