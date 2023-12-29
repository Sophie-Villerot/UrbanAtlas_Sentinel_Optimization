# UrbanAtlas_Sentinel_Optimization


## Quick summary

Optimization of the use of Sentinel-2 (potentially 1) images over Urbal Atlas Areas of Interest (AOIs)

## Problem

The 788 Functional Urban Areas (FUAs) delimited in the Urban Atlas project don't necessarily match perfectly the Sentinel-2A & B fixed paths, based on
the geometric overlap as well as the temporal revit time (around 5 days over Europe) of Sentinel data - level L2A, Bottom of Atmosphere (BOA).

### Data

- FUA delineation;
- Sentinel-2A & B paths/tiles.

### Steps

#### Pre-processing

- Extracting the FUAs delineation from https://land.copernicus.eu/en/map-viewer?dataset=70903c20fc2a4a90ad200bc95a7557d4
- Extracting path tiles for Sentinel-2 and only keeping the intersection with the FUAs.

### Going further

Could be taken into account:
- For each Sentinel image, the cloud mask (i.e. removing all cloudy images or part of them, and interpolating or replacing them with overlapping images);
- The number of pipelines available for the processing (i.e. how to break the all FUAs ensemble into smaller chunks while minimising the amount of tiles to reprocess).

Instead of L2A images, level L3 images (interpolated weekly/monthly) average could be used. 


## Bibliography

https://www.sciencedirect.com/science/article/abs/pii/S0924271622002660
