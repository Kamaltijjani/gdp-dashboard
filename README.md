# GDP Dashboard

A Streamlit dashboard for exploring the bundled World Bank GDP dataset by country and year (1960–2022). Values are current US dollars; this is historical data, not a live feed.

## Run locally

Requires Python 3.10 or newer.

```sh
python -m venv .venv
# Linux/macOS:
source .venv/bin/activate
# Windows PowerShell instead: .venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python -m streamlit run streamlit_app.py
```

Open the local URL printed by Streamlit. Select a year range and one or more country codes. The chart compares GDP over time; cards show the final year's GDP in billions and the final/initial GDP ratio (not a percentage).

Missing values display “No data”. A missing or zero starting value has no growth ratio. An empty country selection prompts you to select a country.

## Files

- `streamlit_app.py`: application
- `data/gdp_data.csv`: bundled historical dataset
- `requirements.txt`: Python dependencies

Some World Bank country codes represent regions or income groups. Missing observations are not treated as zero. See `LICENSE` for licensing.
