# Locations for Potential Aquaculture 
## EDS 223 Assignment 3 
Determining which exclusive economic zones (EEZ) on the West Coast are best suited to develop marine aquaculture


![Source: AGRITECTURE](https://www.agritecture.com/hubfs/Imported_Blog_Media/cishqO8wnTSbHWYxctUsYC1XxIpnYWQ5drcoh_22VWw-Sep-11-2023-11-25-21-8230-AM.jpg)

## Background

Aquaculture sits at the nexus of food secuity and marine conservation. On a global scale, aquaculture supplies more than 50% of all aquatic animals consumed by people. This practice also allows wild stocks of threatened or endangered species to be replenished by removing pressure off of overfished natural populations. The United States holds the second largest Exclusive Economic Zone (EEZ) in the globe. In the west coast alone, EEZ regions covers about 830,000 square kilometers of sea floor. Specifically, it extends 200 nautical miles offshore fron Washington, Oregon, and California. This gives the United States the soverign rights to the natural resources in this area.

Due to these reasons, and many more, expansion of aquaculture is an notable avenue of exploration. However, not all of the area that the EEZ spans is not necessarily suitable for all commercial marine species. Conditions for optimal temperatures and depth levels must be met to consider a species for aquaculture in the west coast. 


## Purpose
This repository creates a function, `suitable_locations_aquaculture()`, that determines and maps the suitable area in each EEZ region in the West Coast for a given species. 

The function has five arguments: 

    - species (species name, as a string) 
    - sst_min (lowest suitable temperature, Celsius ) 
    - sst_max (highest suitable temperature, Celsius) 
    - depth_min (greatest depth, meters below sea level) 
    - depth_max (lowest depth, meters below sea level, default is set to 0) 

A location is deemed suitable for the species if both temperature and depth conditions are met. The area is then visualized and produces a table specifying suitable area in squared kilometers for each region.



## Repository organization
```
potential-aquaculture
└─── README.md
└─── qmd/Rmd/Proj files
└─── potential-aquaculture-analysis.qmd 
|   .gitignore
    └───data
        └─── wc_regions_clean.shp
        └─── depth.tif
        └─── average_annual_sst_2008.tif
        └─── average_annual_sst_2009.tif
        └─── average_annual_sst_2010.tif
        └─── average_annual_sst_2011.tif
        └─── average_annual_sst_2012.tif
```
Data was placed in the `.gitignore` folder due to large size.


## Data access

Sea surface temperature (SST) data from 2008-2012 were originally generated from NOAA’s [5km Daily Global Satellite Sea Surface Temperature Anomaly](https://coralreefwatch.noaa.gov/product/5km/index_5km_ssta.php).

Gridded bathymetric data to measure depth in this analysis was obtained from [General Bathymetric Chart of the Oceans (GEBCO)](https://www.gebco.net/data-products/gridded-bathymetry-data#area).

Boundaries for the Exclusive Economic Zones in the west coast were obtained from [Marineregions.org](https://www.marineregions.org/eez.php)


More concisely, all data was downloaded from a provided [folder](https://drive.google.com/file/d/1u-iwnPDbe6ZK7wSFVMI-PpCKaRQ3RVmg/view?usp=sharing).



## Contributors

Assignment given by Annie Adams for EDS223 Fall 2026.





## References

AGRITECTURE. "A Dive into Aquaculture: The Future of Sustainable Seafood." https://www.agritecture.com/blog/2023/5/16/a-dive-into-aquaculture-the-future-of-sustainable-seafood. Accessed 7 Nov. 2026.

European Commission. "1. What Are the Main Benefits of Aquaculture?" https://aquaculture.ec.europa.eu/faq/1-what-are-main-benefits-aquaculture. Accessed 7 Nov. 2026.

GLORIA Bathymetry of the U.S. West Coast Exclusive Economic Zone | Data Basin. https://databasin.org/datasets/6d14f92effae4ff083a95a78d87e4b1e/. Accessed 7 Nov. 2026.

NOAA Fisheries. “Aquaculture” NOAA, 24 Sept. 2026, National, https://www.fisheries.noaa.gov/topic/aquaculture.

NOAA Ocean Exploration. “What Is the ‘EEZ’?”, https://oceanexplorer.noaa.gov/ocean-fact/useez/. Accessed 7 Nov. 2026.
