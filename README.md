# Eaton & Palisades Wildfire Analysis

### Landsat False-Color Imagery + Environmental Justice Index Community Vulnerability Assessment

## About This Repository

This repository contains the analysis and supporting materials for the wildfire-impact project examining the *2025 Eaton and Palisades Fires* in Los Angeles County. The project integrates:

-   *Landsat 8 satellite imagery* (true-color and false-color composites)
-   *Fire perimeter data* from NIFC FIRIS
-   *2024 Environmental Justice Index* census-tract–level social vulnerability indicators

The goal is to understand both the physical burn impacts and the social dimensions of the communities affected by each fire.

## Final Map Output

This map summarizes the main output of homework 4, showing false-color Landsat Imagery and the Eaton and Palisades Fire Perimeters.

**VERY IMPORTANT!!! REPLACE THIS WITH PICTURE!!!**

## Repository Structure

``` bash
ep-wildfire-analysis
├── landsat-false-color.ipynb
├── eji-social-vulnerability.ipynb
├── LICENSE
├── .gitignore
└── README.md
```

## Data Access

This project uses publicly available spatial and remote sensing datasets stored locally in the repository's `data/` directory. Following is the local `data/` directory structure:

``` bash
├── data
│   ├── fire_perimeters
│   │   ├── Eaton_Perimeter_20250121.csv
│   │   ├── Eaton_Perimeter_20250121.geojson
│   │   ├── Eaton_Perimeter_20250121.kml
│   │   ├── Palisades_Perimeter_20250121.csv
│   │   ├── Palisades_Perimeter_20250121.geojson
│   │   └── Palisades_Perimeter_20250121.kml
│   ├── EJI_2024_California
│   │   ├── EJI_2024_California.gdb
│   └── landsat8-2025-02-23-palisades-eaton.nc
```

The dataset for this repository:

#### Fire Perimeter Dataset

The fire perimeter dataset contains dissolved burn boundaries for the Eaton and Palisades fires. The original data comes from NIFC FIRIS (Fire Integrated Real-time Intelligence System). The data provide daily fire growth during a wildfire. The dataset is available through the Los Angeles GeoHub and the NIFC FIRIS public ArcGIS service.

#### Landsat NetCDF Dataset

The Landsat used in this analysis is a Landsat 8 Collection Level-2 Surface Reflectance product accessed through the [Microsoft Planetary Computer Data Catalogue](https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2). The dataset includes multiple spectral bands stored in a NetCDF structure, CRS information, coordinate dimensions, and metadata. The spectral bands will assist in creating true and false-color composite images for post-fire assessment.

#### Environmental Justice Index Community Vulnerability Analysis

This analysis uses the 2024 [Environmental Justice Index](https://www.atsdr.cdc.gov/place-health/php/eji/eji-explorer.html) (EJI) to identify and compare census tracts affected by the Eaton and Palisades fires, using spatial joins and clipping to the fire boundaries. After aligning datasets to a shared CRS, the intersecting tracts are examined using four key vulnerability indicators, such as age, vehicle access, poverty, and overall EJI score, to highlight differences in social and demographic vulnerability between the two burn areas.

## Authorship

This repository was created for the course EDS 220 – Working with Environmental Datasets, UC Santa Barbara.

-   The project author: **Jay Kim**
-   Instructor: **Carmen Galaz García**
-   Co-Instructor: **Annie Adams**

## References

Data Citation:

\[1\] Los Angeles GeoHub / NIFC FIRIS. (2025). *Palisades–Eaton dissolved fire perimeters* \[data file\]. Available: https://geohub.lacity.org/maps/ad51845ea5fb4eb483bc2a7c38b2370c/about. \[Accessed: Nov. 15, 2025\]

\[2\] U.S. Geological Survey. *Landsat Collection 2 Level-2 Surface Reflectance (Microsoft Planetary Computer version)* \[data file\]. Available: https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2. \[Accessed: Nov. 15, 2025\]

\[3\] U.S. Department of Health and Human Services. (2024). *Environmental Justice Index (EJI), 2024 – California Census Tract Data* \[data file\]. Available: https://www.atsdr.cdc.gov/place-health/php/eji/eji-data-download.html. \[Accessed: Nov. 21, 2025\]