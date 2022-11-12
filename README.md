# NC_COVID_data

![nc_counties_covid](https://user-images.githubusercontent.com/54029190/201450287-bdf96e3a-a049-443b-b9ee-57e77fba7133.gif)
<img width="770" alt="image" src="https://user-images.githubusercontent.com/54029190/201451091-1351da5d-25ad-457a-b250-4fae3959a751.png">

This repository contains the data for and documents the process used to generate the [Tableau visualisation](https://public.tableau.com/app/profile/amanda.lim2824/viz/NCCountiesCOVIDSpread/COVID-19NCCountiesSheet?publish=yes) for the prevalence of COVID across North Carolina Counties from May - Oct 2020.

### Data Source:
- Data was taken from the [NCDHHS.gov](https://covid19.ncdhhs.gov/dashboard/data-behind-dashboards) website,
under the "County-Daily Cases and Deaths Metrics" as an excel file.
- Excel file for demographics for NC County Populations taken from [here](https://www.northcarolina-demographics.com/counties_by_population)
- Excel file for fibs codes taken from simple Google search

### Process:
Using R,
- The original daily cases were summed into groups by month and county
- The population data was added to the counties using an outer join, and the rate (cases/population) for each month calculated
- Saving the dataframe as an Excel file, Tableau was used to visualise the data

### Problems faced:
- County column insufficient on its own in Tableau, extra research from [here](https://kb.tableau.com/articles/howto/plotting-u-s-5-digit-fips-county-code) helped in adding fibs and State columns.
fibs data added to excel using outer join in R.
