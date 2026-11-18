# Myuzima original-design dashboard upgrade

Three tabs: Overview & clickable community map, Socioeconomic Factors & Regression, Healthcare & Hospital Impact.

## Run

```bash
python3 -m pip install -r requirements.txt
python3 -m streamlit run app.py
```

Click a Chicago community polygon to open the detailed popup. Use the sidebar community selector to synchronize all charts and metrics.

## Data caution

Merged community-year data contains repeated static profile and historical variables; these are not independent annual measurements. Regression is exploratory Poisson with year indicators and a population offset; assess overdispersion and alternative models before external use. Poverty definitions and source years need primary-source verification. Hospital finances are hospital-wide, not gunshot-specific. Drive-time estimates are not actual EMS times.

The source data are retained in `data/`. No original GitHub files are changed by this ZIP.

Map fix: Both interactive maps use OpenStreetMap tiles instead of CartoDB Positron, removing the CARTO API KEY REQUIRED overlay. Internet access is needed for background tiles.
