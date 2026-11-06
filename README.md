# EDS 223: West Coast Aquaculture Analysis

## Purpose
This repository contains data and code to visualize which Exclusive Economic Zones (EEZs) on the West Coast of the US are best suited for marine aquaculture of several species of bivalves, based on suitable sea surface temperature (SST) and depth value ranges for the respective species. First, an initial workflow was established to identify suitable oyster habitats. A function was then created to create a generalizable workflow for future species analyses. The resulting `suitable_habitat_area` function takes minimum and maximum sea surface temperature, minimum and maximum depth, and species name as arguments. Its output includes a map of EEZ regions colored by amount of suitable habitat area and layered with suitable habitat locations. Mediterranean mussels (*Mytilus galloprovincialis*) were used as an example for the generalized workflow. 

## Repository Structure 
This repository is structured as follows:

```
eds223-aquaculture
├── README.md
├── west_coast_aquaculture_analysis.pdf
└── west_coast_aquaculture_analysis.qmd
|   .gitignore
    └───data
        └─── wc_regions_clean.dbf
        └─── wc_regions_clean.prj
        └─── wc_regions_clean.shp
        └─── wc_regions_clean.shx
        └─── depth.tif
        └─── average_annual_sst_2008.tif
        └─── average_annual_sst_2009.tif
        └─── average_annual_sst_2010.tif
        └─── average_annual_sst_2011.tif
        └─── average_annual_sst_2012.tif
```

## Data Access
The specific files used in this exercise can be downloaded using [this link](https://drive.google.com/file/d/1u-iwnPDbe6ZK7wSFVMI-PpCKaRQ3RVmg/view?usp=sharing). The data used in this project originated from the following sources:

1. Average annual sea surface temperature (SST) from the years 2008 to 2012 from [NOAA’s 5km Daily Global Satellite Sea Surface Temperature Anomaly v3.1](https://coralreefwatch.noaa.gov/product/5km/index_5km_ssta.php).

Data files:
* `average_annual_sst_2008.tif`
* `average_annual_sst_2009.tif`
* `average_annual_sst_2010.tif`
* `average_annual_sst_2011.tif`
* `average_annual_sst_2012.tif`

2. Ocean bathymetry data from the [General Bathymetric Chart of the Oceans (GEBCO)](https://www.gebco.net/data_and_products/gridded_bathymetry_data/#area).

Data files:
* `depth.tif`

3. Maritime boundaries using Exclusive Economic Zones off the west coast of US from [Marineregions.org](https://www.marineregions.org/eez.php).

Data files:
* `wc_regions_clean.shp`

4. Information on species depth and temperature requirements from [SeaLifeBase](https://www.sealifebase.ca/summary/Mytilus-galloprovincialis.html).

## Authors
[Courtney Lorey](https://github.com/cllorey/cll214final), Bren School of Environmental Science & Management, University of California, Santa Barbara

## References
NOAA Coral Reef Watch Version 3.1 Daily Global 5km Satellite Sea Surface Temperature Anomaly Product, 2008–2012. 2026. *NOAA Coral Reef Watch*. Retrieved: November 05, 2026, from [https://coralreefwatch.noaa.gov/product/5km/index_5km_ssta.php](https://coralreefwatch.noaa.gov/product/5km/index_5km_ssta.php).

GEBCO_2026 Grid. 2026. *GEBCO Bathymetric Compilation Group*. Retrieved: November 05, 2026, from [https://www.gebco.net/data-products/gridded-bathymetry-data#area](https://www.gebco.net/data-products/gridded-bathymetry-data#area).

Maritime Boundaries Geodatabase: Maritime Boundaries and Exclusive Economic Zones (200NM), version 12. 2023. *Flanders Marine Institute*. Retrieved: November 05, 2026, from [https://www.marineregions.org/eez.php](https://www.marineregions.org/eez.php).

Mediterranean mussel (*Mytilus galloprovincialis*). 2026. *SeaLifeBase*. Retrieved: November 05, 2026, from [https://www.sealifebase.ca/summary/Mytilus-galloprovincialis.html](https://www.sealifebase.ca/summary/Mytilus-galloprovincialis.html).
