# alaska_substinence_economics_analysis
Data and statistical analysis of substinence activities across Alaska

## Datasets
The `data/` directory contains all data and datasets. Some had to be scraped, cleaned up and aggregated before being merged into the `master.csv` - the dataset containing all relevant data.

This has exclusively been done through python code available in the `src/notebooks/` directory in the form of jupyter-notebooks to allow interpretation and explaination of choices made.

All custom and aggregated data can be found in the `data/custom_data/` directory, to keep the original folders - organized by source - clean of manipulation.

The `data/custom_data/master.csv` dataset contains all relevant data, then further selected to form the `data/custom_data/analysis.csv` file, to be used for statistical analysis.

## Variable explaination and sources:

| Column Name                       | Description                               | Source                             | Link |
|-----------------------------------|-------------------------------------------|------------------------------------|------|
| year                              | Data year of harvest and use              | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| commname                          | Community or CDP name                     | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| region                            | Region of Alaska for the community        | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| top_lbs_wildfood_use_percapita    | 100th percentile wild food use per capita | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| adj_households_in_community       | Eligible households in the community      | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| IncorporationType                 | Community incorporation status            | DCRA                               | [Link](https://dcra-cdo-dcced.opendata.arcgis.com/datasets/d748e3b58c654b64825f974c25b3c697_0/explore) |
| BoroughCensusArea                 | Borough or census area of the community   | DCRA                               | [Link](https://dcra-cdo-dcced.opendata.arcgis.com/datasets/d748e3b58c654b64825f974c25b3c697_0/explore) |
| NativeRegionalHealthCarePro       | Native regional healthcare provider       | DCRA                               | [Link](https://dcra-cdo-dcced.opendata.arcgis.com/datasets/d748e3b58c654b64825f974c25b3c697_0/explore) |
| SchoolDistrict                    | School district overseeing the community  | DCRA                               | [Link](https://dcra-cdo-dcced.opendata.arcgis.com/datasets/d748e3b58c654b64825f974c25b3c697_0/explore) |
| ClimateRegion                     | Climate region classification             | DCRA                               | [Link](https://dcra-cdo-dcced.opendata.arcgis.com/datasets/d748e3b58c654b64825f974c25b3c697_0/explore) |
| EnergyRegion                      | Energy region classification              | DCRA                               | [Link](https://dcra-cdo-dcced.opendata.arcgis.com/datasets/d748e3b58c654b64825f974c25b3c697_0/explore) |
| EconomicRegion                    | Economic region classification            | DCRA                               | [Link](https://dcra-cdo-dcced.opendata.arcgis.com/datasets/d748e3b58c654b64825f974c25b3c697_0/explore) |
| subreg                            | Sub-region of Alaska                      | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| resource                          | Resource species or category              | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| using                             | % households using the resource           | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| trying                            | % households attempting harvest           | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| harvesting                        | % households successfully harvesting      | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| giving                            | % households giving the resource          | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| receving                          | % households receiving the resource       | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| units_harvested                   | Total units harvested                     | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| pounds_harvested                  | Total pounds harvested                    | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| harv_mes_units                    | Measurement units for harvest             | ADF&G                              | [Link](https://adfg-ak-subsistence.shinyapps.io/CSIS-Data-Downloader/) |
| labor_force                       | Total labor force participation           | Alaska Laborstats                  | [Link](https://live.laborstats.alaska.gov/labforce/csv/AKlaborforce.csv) |
| employed                          | Total employed population                 | Alaska Laborstats                  | [Link](https://live.laborstats.alaska.gov/labforce/csv/AKlaborforce.csv) |
| unemployed                        | Total unemployed population               | Alaska Laborstats                  | [Link](https://live.laborstats.alaska.gov/labforce/csv/AKlaborforce.csv) |
| unemployment_rate                 | Unemployment rate percentage              | Alaska Laborstats                  | [Link](https://live.laborstats.alaska.gov/labforce/csv/AKlaborforce.csv) |
| median_family_income              | Median family income                      | Family Income and Benefits         | [Link](https://dcra-cdo-dcced.opendata.arcgis.com/datasets/5b535254c9f649f9b7ffe52a476052c4_3/explore) |
| p_people_below_poverty            | % of people below poverty                 | Computed (Income & Poverty)        | [Link](https://dcra-cdo-dcced.opendata.arcgis.com/datasets/f4b63e8b2c3042a98130505df1422730_9/explore) |
| p_population_native               | % indigenous population                   | Computed (Race)                    | [Link](https://dcra-cdo-dcced.opendata.arcgis.com/datasets/30ab75bf594f48349c4ff536957869f8_1/explore) |
| ratio_male_over_female            | Ratio of males to females                 | Computed (Sex)                     | [Link](https://dcra-cdo-dcced.opendata.arcgis.com/datasets/fa3ad93528b24f7c9ba298a68c04920d_0/explore) |
| local_tax_burden                  | Aggregated Local Tax Burden (weighted)    | IRS SOI                          | [Link](https://www.irs.gov/downloads/irs-soi?page=17) |
| federal_tax_burden                | Aggregated Federal Tax Burden (weighted)  | IRS SOI                          | [Link](https://www.irs.gov/downloads/irs-soi?page=17) |
| Gini                              | Aggregated Gini Coefficient (weighted)    | IRS SOI                          | [Link](https://www.irs.gov/downloads/irs-soi?page=17) |
