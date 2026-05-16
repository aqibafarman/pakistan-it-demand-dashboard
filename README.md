# Pakistan IT Sector — Demand Forecasting Dashboard

A data analytics project forecasting Pakistan's IT export demand through 2030,
built with Python and Power BI using real public data sources.

## Dashboard Pages
| Page | Content |
|------|---------|
| 1 | IT Export Growth Story (FY2006–FY2025) |
| 2 | Macro & Market Context |
| 3 | 5-Year Demand Forecast (2026–2030) |
| 4 | PKR/FX Impact on Export Competitiveness |

## Tech Stack
- **Python**: pandas, Prophet (Meta AI), statsmodels, requests, BeautifulSoup
- **Power BI**: DAX measures, Power Query, star schema data model
- **Forecast model**: Facebook Prophet with GDP as external regressor
- **Model accuracy**: MAPE 11.6% (Good fit), trained on 20 annual observations

## Data Sources
| Source | Data | Method |
|--------|------|--------|
| State Bank of Pakistan | IT exports FY2006–FY2025 | Official bulletin |
| World Bank Open Data API | GDP, internet users, ICT indicators | Live API fetch |
| Payoneer / PAFLA-ADB | Freelancing index, workforce data | Published reports |
| SBP interbank rates | PKR/USD 2015–2024 | Published averages |

## Key Findings
- Pakistan IT exports grew **17x** from $227M (FY2006) to $3.8Bn (FY2025)
- 19-year CAGR of **~15%** — one of Asia's most consistent tech growth stories
- Forecast: **$5.95Bn by FY2030** (90% CI: $4.8Bn – $7.2Bn)
- Internet penetration and IT export growth show strong structural correlation
- PKR depreciation of 173% since 2015 acts as a competitiveness tailwind

## Project Structure
├── 01_raw_data/
├── 02_clean_data/        ← processed CSVs
├── 03_forecasts/         ← Prophet output
├── 04_notebooks/         ← Jupyter pipeline
├── 05_powerbi/           ← .pbix file
└── 06_exports/           ← PDF + screenshots

## How to Run
1. Install requirements: `pip install pandas prophet statsmodels requests beautifulsoup4 plotly`
2. Run `04_notebooks/01_data_pipeline.ipynb` top to bottom
3. Open `05_powerbi/systems_limited_dashboard.pbix` in Power BI Desktop

---
*Built as part of a Reporting Specialist portfolio project | May 2026*
