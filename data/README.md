# Data files

This folder holds data used by the CIVE 480A6 lab notebooks. These data come from publicly available sources, but have been formatted to simplify analysis. Original data sources are noted below.

---

## Lab 1 — Greenhouse Gases and Earth's Radiation

Notebook: `Lab1_Greenhouse_Gases_and_Radiation.ipynb`

### Atmospheric greenhouse gas concentrations (NOAA GML)

Monthly mean atmospheric concentrations from the NOAA Global Monitoring
Laboratory (GML). <https://gml.noaa.gov/ccgg/trends/>.

* `co2_mm_mlo.csv`: Carbon dioxide (CO₂) monthly mean at Mauna Loa Observatory (1958 – 2026) [find original data here](https://gml.noaa.gov/ccgg/trends/data.html)
* `ch4_mm_gl.csv`: Methane (CH₄) global monthly mean (1983 – 2026) [find original data here](https://gml.noaa.gov/ccgg/trends_ch4/)
* `n2o_mm_gl.csv`: Nitrous oxide (N₂O) global monthly mean (2001 – 2026) [find original data here](https://gml.noaa.gov/ccgg/trends_n2o/)

### National greenhouse gas emissions (Our World in Data)

* `ghg_emissions_country.csv`: total annual greenhouse gas emissions by country in tonnes of CO₂-equivalent per year, downloaded from [Our World in Data](https://ourworldindata.org/grapher/annual-co2-emissions-per-country).


### U.S. greenhouse gas emissions by state and sector (EPA)

* `ghg_emissions_state_sector.csv`: annual greenhouse gas emissions broken out by state, sector, and specific greenhouse gas. Reported as teragrams (Tg, million metric tons) of CO₂-equivalent. Downloaded from the [U.S. EPA GHG inventor](https://www.epa.gov/ghgemissions/methodology-report-inventory-us-greenhouse-gas-emissions-and-sinks-state-1990-2022
)

---

## Lab 2 — Analyzing Historical Temperature Trends

Notebook: `Lab2_Analyzing_Historical_Temperature_Trends.ipynb`

### Global gridded temperature data

Gridded (5° x 5°) annual surface temperature anomalies calculated from NOAA's Global Surface Temperature
dataset (version 6.1) <https://www.psl.noaa.gov/data/gridded/data.noaaglobaltemp.html>

* `noaa_global_temperature_annual.nc`: annual mean temperature anomaly

### Colorado gridded temperature and elevation data (PRISM)

4km resolution gridded climate data for Colorado calculated from the PRISM dataset <https://prism.oregonstate.edu/>

* `PRISM_tmean_annual_CO_1895_2025.nc`: annual mean temperature (°C), 1895–2025 within Colorado

---

## Lab 3 — Hydrologic Cycle Changes

Notebook: `Lab3_Hydrologic_Cycle_Changes.ipynb`

### SNOTEL snow water equivalent, Elk River, CO

* `Elk_River_SNOTEL_SWE.csv`: Daily snow water equivalent (SWE) measured at the Elk River SNOTEL station (site 467), north of Steamboat Springs in Routt County, CO. Values for 1978-10-01 to 2026-09-28 (water years 1979–2026). Station page: <https://wcc.sc.egov.usda.gov/nwcc/site?sitenum=467>

---

## Lab 4 — Analyzing Extreme Fire Weather

Notebook: `Lab4_Extreme_Fire_Weather.ipynb`

### Fire Weather Index

Daily Canadian Forest Fire Weather Index (FWI), 1970–2025, for the foothills adjacent to Fort Collins, CO. Original dataset described in <https://www.nature.com/articles/s41597-020-0554-z>

The FWI is a unitless index of fire danger calculated from daily temperature, relative humidity, wind speed, and recent precipitation, with higher values indicating weather conditions more favorable for fires to ignite and spread.

* `fort_collins_fire_weather_index.csv`: daily FWI at a single location near Fort Collins, CO (1970-01-01 to 2025-12-31)

---

## Lab 5 — Extreme Value Theory and Design Wind Speeds

Notebook: `Lab5_Extreme_Value_Theory.ipynb`

### Simulated hurricane winds for Mobile, AL

Annual maximum hurricane wind speeds (m/s) at the center of Mobile, AL, from computer simulations of hurricanes conducted by Prof. Yanlin Guo. Each simulation was run for 20,000 years. Values correspond to maximum windspeed within ~20-year blocks of time 

* `hurricane_winds_2015_Mobile-AL_20yr_max.csv`: simulation of the present climate (Year 2015)
* `hurricane_winds_2100_Mobile-AL_20yr_max.csv`: simulation of the future climate in Year 2100 under the SSP2-4.5 scenario


## Lab 6 — Future Climate Projections and Building Energy Use

Notebook: `Lab6_Future_Climate_Projections.ipynb`

### CMIP6 annual mean temperature projections for Chicago, IL

Annual mean temperature from CMIP6 climate model simulations for the model grid cell closest to Chicago, IL (41.25°N, 271.25°E; the models have a 2.5° resolution), for the years 2015–2099. Each file has one dimension, `year`, and one variable, `meanT`, in °C as an anomaly relative to the 1985–2014 average. Files are named `temperature_Chicago_<model>_<scenario>_<simulation>.nc`.

Files used in the lab:

* `ssp370`: `CESM2` (`r4i1p1f1`), `MIROC6` (`r1i1p1f1`), `CanESM5` (`r1i1p1f1`), and `ACCESS-ESM1-5` (`r1i1p1f1`, `r4i1p1f1`, `r5i1p1f1`)
* `ssp126`, `ssp245`, `ssp585`: `ACCESS-ESM1-5` (`r1i1p1f1`)


