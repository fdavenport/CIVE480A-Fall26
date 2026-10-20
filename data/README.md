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

## Lab 4 — Analyzing Extreme Fire Weather

Notebook: `Lab4_Extreme_Fire_Weather.ipynb`

### Fire Weather Index

Daily Canadian Forest Fire Weather Index (FWI), 1970–2025, for the foothills adjacent to Fort Collins, CO. Original dataset described in <https://www.nature.com/articles/s41597-020-0554-z>

The FWI is a unitless index of fire danger calculated from daily temperature, relative humidity, wind speed, and recent precipitation, with higher values indicating weather conditions more favorable for fires to ignite and spread.

* `fort_collins_fire_weather_index.csv`: daily FWI at a single location near Fort Collins, CO
  * 20,454 daily values from 1970-01-01 to 2025-12-31 (no missing days)
  * Columns:
    * (unnamed first column): row index
    * `date`: date in YYYY-MM-DD format
    * `fwi`: Fire Weather Index (unitless). Values range from about 0 to 145; the median is about 6 and the 75th percentile is about 38

Other files added for this lab but not currently used: `boulder_fire_weather_index.csv` and `fort_collins_weather_station_T_max.csv` (daily maximum temperature in °F).

---

## Lab 5 — Extreme Value Theory and Design Wind Speeds

Notebook: `Lab5_Extreme_Value_Theory.ipynb`

### Simulated hurricane winds for Mobile, AL

Annual maximum hurricane wind speeds (m/s) at the center of Mobile, AL, from computer simulations of hurricanes conducted by Prof. Yanlin Guo and her graduate students in the CEE Department at CSU. Each simulation was run for 20,000 years. Only years with a hurricane are included in the files (about 9,700 years in each).

Files used in the lab (block maxima):

* `hurricane_winds_2015_Mobile-AL_20yr_max.csv`: simulation of the present climate (Year 2015); 973 values
* `hurricane_winds_2100_Mobile-AL_20yr_max.csv`: simulation of the future climate in Year 2100 under the SSP2-4.5 scenario; 970 values
  * Column: `max_wind`, maximum wind speed (m/s) in each block. Each value is the maximum of 10 consecutive rows of the original files below (10 consecutive years with a hurricane, which is about 20 years of the simulation since only about half of simulated years have a hurricane). In the lab, each value is treated as a 20-year block maximum. Rows left over at the end of the original files were dropped (9 rows for 2100).

Original files (not used in the lab):

* `hurricane_winds_2015_Mobile-AL.csv` and `hurricane_winds_2100_Mobile-AL.csv`: annual maximum wind speed (m/s) in each simulated year that has a hurricane (column `max_wind`; 9,730 and 9,709 rows)


