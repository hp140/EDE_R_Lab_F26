# EPA Air Quality Datasets

## Summary
This dataset was prepared for Environmental Data Exploration (ENV 700) at Duke University, Fall 2026

The dataset contains data from air quality monitoring of PM2.5 and ozone in North Carolina.

## PM2.5 and O3 data

Data were collected using the Doanload Daily Data tool (https://www.epa.gov/outdoor-air-quality-data/download-daily-data).
The following selections were made: 
* PM2.5 and Ozone (Pollurant)
* 2018 and 2019 (Year)
* North Carolina (Geographic Area)
* Download CSV (spreadsheet)


csv files were saved as 
`EPAair_O3_NC2024_raw.csv`, `EPAair_O3_NC2025_raw.csv`, 
`EPAair_PM25_NC2024_raw.csv`, and `EPAair_PM25_NC2025_raw.csv`. 

## EPA Air Time Series Data

For the multiple Ozone series, we used API to download the separate data files. 
The code developed downloads daily AQS Ozone data for a given year into a CSV file, 
repeating for a span of years. 

Returns data summarized at the daily level. All daily summaries are calculated on 
midnight to midnight basis in local time. Variables returned include date, mean value, 
maximum value, etc. Data is at the monitor level and may include more than one entry per monitor. 
There may be multiple entries for different (1) sample durations, (2) pollutant standards. 
This code screens for data at the "`Ozone 8-hour 2015`" pollutant standard level for 
site `371190041` (Garinger School, near Charlotte, NC.)

* API Documentation: <https://aqs.epa.gov/aqsweb/documents/data_api.html#daily>
* Site ID = '371190041'


Data were accessed June 12 2026  
For more information contact John Fay (`john.fay@duke.edu`)

## Data Content Information
Information gathered from: https://www.epa.gov/outdoor-air-quality-data/air-data-basic-information and https://aqs.epa.gov/aqsweb/documents/AQS_Format.html

Column names without descriptors are self-explanatory.

Date: month/day/year
Source: AQS (Air Quality System) or AirNow
Site ID: A unique number within the county identifying the site.
POC: “Parameter Occurrence Code” used to distinguish different instruments that measure the same parameter at the same site.
Daily Mean PM2.5 Concentration: numeric value
Daily Max 8-hour Ozone Concentration: numeric value
Units: units for concentration

Daily_AQI_VALUE: Air quality index (range 0-500). Levels: 
0-50: Good (green)
51-100: Moderate (yellow)
101-150: Unhealthy for sensitive groups (orange)
151-200: Unhealthy (red)
201-300: Very unhealthy (purple)
301-500: Hazardous (maroon)

Site Name
DAILY_OBS_COUNT: number of observations per day
PERCENT_COMPLETE
AQS_PARAMETER_CODE
AQS_PARAMETER_DESC
CBSA_CODE
CBSA_NAME
STATE_CODE
STATE
COUNTY_CODE
COUNTY
SITE_LATITUDE
SITE_LONGITUDE

## Naming conventions and file formats
Files are named according to the following naming convention: `databasename_datatype_details_stage.format`, where: 

**databasename** refers to the database from where the data originated

**datatype** is a description of data 

**details** are additional descriptive details, particularly important for processed data 

**stage**refers to the stage in data management pipelines (e.g., raw, cleaned, or processed)

**format** is a non-proprietary file format (e.g., .csv, .txt)
