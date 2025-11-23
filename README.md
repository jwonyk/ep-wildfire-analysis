# Landsat False Color Analysis of Fire Impact of Palisades-Eaton Region

## About This Repository

This repository contains the work for homework 4, tasks 2. The repository focuses on analyzing wildfire impacts using Landsat 8 satellite imagery and a fire perimeter dataset. The project explores the following:

-   Explore and wrangle geospatial fire perimeter data
-   Import and explore NetCDF-based Landsat raster data
-   Restore CRS information for raster dataset
-   Create a true and false-color image
-   Visualize fire perimeters
-   Document the workflow

## Final Map Output

This map summarizes the main output of homework 4, showing false-color Landsat Imagery and the Eaton and Palisades Fire Perimeters.

<img width="990" height="553" alt="output" src="https://github.com/user-attachments/assets/e20ae91e-b1bc-46e6-b1d3-4dee75a123d3" />

## Repository Structure

``` bash
eds220-hwk4
├── hwk4-task2-false-color-kim.ipynb
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
│   └── landsat8-2025-02-23-palisades-eaton.nc
```

The dataset for this repository:

#### Fire Perimeter Dataset

The fire perimeter dataset contains dissolved burn boundaries for the Eaton and Palisades fires. The original data comes from NIFC FIRIS (Fire Integrated Real-time Intelligence System). The data provide daily fire growth during a wildfire. The dataset is available through the Los Angeles GeoHub and the NIFC FIRIS public ArcGIS service.

#### Landsat NetCDF Dataset

The Landsat used in this analysis is a Landsat 8 Collection Level-2 Surface Reflectance product accessed through the Microsoft Planetary Computer Data Catalogue. The dataset includes multiple spectral bands stored in a NetCDF structure, CRS information, coordinate dimensions, and metadata. The spectral bands will assist in creating true and false-color composite images for post-fire assessment.

## Authorship

This project is part of the assignment from EDS 220 - Working with Environmental Datasets.

-   The project author: **Jay Kim**
-   Instructor: **Carmen Galaz García**
-   Co-Instructor: **Annie Adams**

## References

Data Citation:

\[1\] EPSG.io. (n.d.). *EPSG:32611 – WGS 84 / UTM Zone 11N*. Available: https://epsg.io/32611#google_vignette. \[Accessed: Nov. 15, 2025\]

\[2\] Los Angeles GeoHub / NIFC FIRIS. (2025). *Palisades–Eaton dissolved fire perimeters* \[data file\]. Available: https://geohub.lacity.org/maps/ad51845ea5fb4eb483bc2a7c38b2370c/about. \[Accessed: Nov. 15, 2025\]

\[3\] U.S. Geological Survey. *Landsat Collection 2 Level-2 Surface Reflectance (Microsoft Planetary Computer version)* \[data file\]. Available: https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2. \[Accessed: Nov. 15, 2025\]

\[4\] NASA Earth Observatory. (2014, Mar. 4). *Why is that forest red and that cloud blue? How to interpret a false-color satellite image*. Available: https://earthobservatory.nasa.gov/features/FalseColor. \[Accessed: Nov. 15, 2025\]

\[5\] U.S. Geological Survey. (n.d.). *What are the band designations for the Landsat satellites?* Available: https://www.usgs.gov/faqs/what-are-band-designations-landsat-satellites. \[Accessed: Nov. 15, 2025\]

\[6\] U.S. Geological Survey. (2021, Nov. 12). *Common Landsat band combinations*. Available: https://www.usgs.gov/media/images/common-landsat-band-combinations. \[Accessed: Nov. 15, 2025\]
