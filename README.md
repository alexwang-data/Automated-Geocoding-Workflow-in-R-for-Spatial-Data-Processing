# Automated-Geocoding-Workflow-in-R-for-Spatial-Data-Processing

## 🕵️ Overview

A small R script for batch-geocoding addresses from a CSV using OpenStreetMap's Nominatim service, with output as CSV or GeoJSON for mapping.

## ❓ Why R instead of ArcGIS?

In ArcGIS Pro, geocoding is a lot of clicking. This script takes a CSV in, returns a CSV and GeoJSON out with address validation and requires mimnial manual intervention. 

## Notes

OSM/Nominatim has a usage policy of one request per second and isn't internded for heavy bulk use. For larger US-only batches, switch 
```r 
method = "osm"
```
to
```r
method = "census"
```
in the script to use the US Census geocoder. <br><br>

ArcGIS Pro does not take a GeoJSON file directly. Use a JSON to feature geoprocessing tool. 
