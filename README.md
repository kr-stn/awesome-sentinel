# awesome Sentinel [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of awesome tools, tutorials and APIs related to data from the [Copernicus Sentinel Satellites](http://www.copernicus.eu/main/sentinels).

## Data Access

### Data Hubs and National Mirrors
Official datahubs and mirrors by the Copernicus partners and [Collaborative Ground Segment members](https://sentinels.copernicus.eu/web/sentinel/missions/collaborative/national-points-of-contact).
- [**Copernicus Sentinels Scientific Datahub (SciHub)**](https://scihub.copernicus.eu/)
- [**Australia National Mirror**](http://www.copernicus.gov.au/)
- [**Austria National Mirror**](https://data.sentinel.zamg.ac.at/)
- [**French National Mirror (PEPS)**](https://peps.cnes.fr/rocket/)
- [**German National Mirror (CODE-DE)**](https://code-de.org/)
- [**Greek National Mirror**](https://sentinels.space.noa.gr/)
- [**Italian National Mirror**](http://collaborative.mt.asi.it/)

### Partial Mirrors
Innitiatives to integrate specific Sentinel data into existing search and discovery platforms.
- [**USGS EarthExplorer (Sentinel-2)**](https://earthexplorer.usgs.gov/)
- [**Alaska Satellite Facility (Sentinel-1)**](https://www.asf.alaska.edu/sentinel/)

### Cloud providers
Providers that host Copernicus Sentinel data and allow you to bring your own code to process it.
- [**Amazon Web Services (Sentinel-2)**](http://sentinel-pds.s3-website.eu-central-1.amazonaws.com/)
  - public S3 bucket, Sentinel-2 only, hosted in region eu-central-1 (Frankfurt)
- [**Google (Sentinel-2)**](https://console.cloud.google.com/storage/browser/gcp-public-data-sentinel-2/?pli=1)
  - public Google Storage bucket, `.SAFE` format, EU region
  
## Tools
Specific to Copernicus Sentinel data discovery, download and processing.

### search & download
- [**`sentinelsat`**](https://github.com/ibamacsr/sentinelsat)
  - search and download from any Datahub. Comes with an intuitive command line and a flexible Python API.
- [**`Sentinel-download`**](https://github.com/olivierhagolle/Sentinel-download)
  - download Sentinel-2 data from Copernicus SciHub. Supports download of sub-tiles in the old product format (PDS <14).
- [**`peps_download`**](https://github.com/olivierhagolle/peps_download)
  -  download data from the French National Mirror (PEPS).
- [**`Sentinel2ProductIngestor`**](https://github.com/sinergise/Sentinel2ProductIngestor)
  - ingest Sentinel-2 data from SciHub into S3. Used by [Sinergise](https://github.com/sinergise) to populate the [AWS Sentinel-2 mirror](http://sentinel-pds.s3-website.eu-central-1.amazonaws.com/)
- [**`sat-download`**](https://github.com/sat-utils/sat-download)
  - download Sentinel-2 data from AWS
- [**`sat-api`**](https://github.com/sat-utils/sat-api)
  - query Sentinel-2 data on AWS using APIGateWay


### processing
- [**`SNAP` (Sentinel Application Plattform)**](http://step.esa.int/main/toolboxes/snap/)
  - (pre-)process any Sentinel data
- [**Google Earth Engine**](https://earthengine.google.com/)
  - process the global Sentinel-1 and Sentinel-2 archives directly on Googles servers



