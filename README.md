# Exploring Environmental Justice Patterns in Los Angeles and an Exploration with Bird Biodiversity

![Redlined Map from 1939. Source: scalar.usc.edu](https://scalar.usc.edu/hc/jewish-histories-boyle-heights/media/losangelesholc-med.jpg)


## Purpose
With the United State's long history of racial inequality and injustice, many aspects of this still remains in every day life despite movements and improvements. Under the jurisdiction of President Franklin D. Roosevelt in the 1930's, the New Deal allowed for the Home Owners’ Loan Corporation (HOLC) to grade neighborhoods based on their reliability of repayment and investment. Their grading system was from A-D, with D being neighborhoods at greatest risk for real estate investment, and grades could be used to as a reason to deny loans for home ownership. Also known as redlining, these neighborhoods have not been graded or treated fairly, and result in poorer living conditions.

This repository showcases an exploration in map making by displaying redlined neighborhoods in Los Angeles and creating figures of different environmental justice conditions (percent low income, PM2.5 and low life expectancy) by each HOLC grade. To measure differences in environmental impact, bird biodiversity was also explored by neighborhood.

## Repository Structure

```
│   README.md
│   redlined_biodiversity.qmd
│   .gitignore
└───data
     └───ejscreen
     └───gbif-birds-LA
     └───mapping-inequality
```

## Data Access

EJScreen Data is available from the United States Environmental Protection Agency’s EJScreen: [Environmental Justice Screening and Mapping Tool.](https://www.epa.gov/ejscreen/download-ejscreen-data). Data was then filtered to LA county, along with the surrounding counties to provide geographical context. Data was read in using `st_read`. 

HOLC Redlining data was sourced from the [Digital Scholarship Lab at the University of Richmond.](https://dsl.richmond.edu/panorama/redlining/data). Data was used to map onto EJSCREEN data, and was later used to subset with EJSCREEN data for figure calculations. Data was read in using `st_read`. 

Biodiversity data is sourced from the [Global Biodiversity Information Facility.](https://www.gbif.org/) Data was filtered to year 2022, and was subsetted to HOLC data to examine changes in biodiversity within neighborhoods through a figure and plot. Data was read in using `st_read`. 

All data was placed in the data folder and was read in using R. 

## References/acknowledgements
 Mapping Inequality: Redlining in New Deal America, Nelson, Robert K., LaDale Winling, et al. (2023). Mapping Inequality: Redlining in New Deal America. American Panorama: An Atlas of United States History. Retrieved: 10/16/24 from https://dsl.richmond.edu/panorama/redlining,[Redlining Data](https://dsl.richmond.edu/panorama/redlining/data)
   
  EJScreen: Environmental Justice Screening and Mapping Tool, United States Environmental Protection Agency. 2024 version. EJScreen. Retrieved: 10/4/24 from www.epa.gov/ejscreen, [EJScreen Data](https://www.epa.gov/ejscreen/download-ejscreen-data)
  
  Biodiversity Observations, Data from  Global Biodiversity Information Facility, [Biodiversity Data](https://www.gbif.org/)

