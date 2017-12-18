# Awesome Sentinel [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of awesome tools, tutorials and APIs related to data from the [Copernicus Sentinel Satellites](http://www.copernicus.eu/main/sentinels).

## Data Access

### Data Hubs and National Mirrors
Official datahubs and mirrors by the Copernicus partners and [Collaborative Ground Segment members](https://sentinels.copernicus.eu/web/sentinel/missions/collaborative/national-points-of-contact).

- [**Copernicus Open Access Hub (SciHub)**](https://scihub.copernicus.eu/)
- [**Australia National Mirror**](http://www.copernicus.gov.au/)
- [**Austria National Mirror**](https://data.sentinel.zamg.ac.at/)
- [**Finland National Mirror**](https://finhub.nsdc.fmi.fi/)
- [**France National Mirror (PEPS)**](https://peps.cnes.fr/rocket/)
- [**Germany National Mirror (CODE-DE)**](https://code-de.org/)
- [**Greece National Mirror**](https://sentinels.space.noa.gr/)
- [**Italy National Mirror**](http://collaborative.mt.asi.it/)
- [**Norway National Mirror**](https://colhub.met.no/#/home)
- [**Portugal National Mirror**](https://ipsentinel.ipma.pt/dhus/#/home)
- [**Sweden National Mirror (SWEA)**](http://swea.rymdstyrelsen.se/portal/)
- [**United Kingdom National Mirror (SEDAS)**](http://sedas.satapps.org/)

### Partial Mirrors
Innitiatives to integrate specific Sentinel data into existing search and discovery platforms.

- [**Alaska Satellite Facility (Sentinel-1)**](https://www.asf.alaska.edu/sentinel/)
- [**Centre for Environmental Data Analysis - CEDA (Sentinel-1, -2)**](http://catalogue.ceda.ac.uk/search/?search_term=sentinel&return_obj=ob&search_obj=ob)
- [**Theia (Sentinel-2)**](https://theia.cnes.fr/atdistrib/rocket/#/search?collection=SENTINEL2)
  - atmospherically corrected L2A products covering several European countries and [areas proposed by scientists](http://www.cesbio.ups-tlse.fr/multitemp/?page_id=7501)
  - published less than two days after L1C is available
- [**USGS EarthExplorer (Sentinel-2)**](https://earthexplorer.usgs.gov/)
- [**EUMETSAT CODA (Sentinel-3 Marine Products)**](https://coda.eumetsat.int/#/home)
  - 14 day rolling archive of Sentinel-3 L1 and L2 marine products in near real-time (NRT), short time critical (STC) and non time critical (NTC) latency mode

### Cloud Providers
Providers that host Copernicus Sentinel data and allow you to bring your own code to process it.

- [**Amazon Web Services (Sentinel-2)**](http://sentinel-pds.s3-website.eu-central-1.amazonaws.com/)
  - public S3 bucket, Sentinel-2 only, hosted in region eu-central-1 (Frankfurt)
- [**Google (Sentinel-2)**](https://cloud.google.com/storage/docs/public-datasets/sentinel-2)
  - public [Google Cloud Storage bucket](https://console.cloud.google.com/storage/browser/gcp-public-data-sentinel-2/?pli=1), `.SAFE` format, EU region
- [**Planet**](https://www.planet.com/pulse/sentinel-2-and-landsat-8-data-now-available-on-the-planet-platform/)
  - Sentinel-2 included in commercial API

## Tools
Specific to Copernicus Sentinel data discovery, download and processing.

### Search & Download
- [**`sentinelsat`**](https://github.com/sentinelsat/sentinelsat)
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
  - deployed by Development Seed at [https://api.developmentseed.org/satellites](https://api.developmentseed.org/satellites)
- [**`awsdownload`**](https://github.com/kraftek/awsdownload)
  - downloader for Sentinel-2 products from Amazon or SciHub
- [**`sentinelhub`**](https://github.com/sinergise/sentinelhub)
  - Python library for downloading Sentinel-2 data from Amazon into ESA .SAFE format.
- [**`aws-sat-api`**](https://github.com/RemotePixel/aws-sat-api)
  - Simple Serverless API for satellite data hosted on AWS Public Dataset
- [**`sentinel_s3`**](https://github.com/beaorn/sentinel_s3)
  - Ruby gem for parsing Sentinel-2 metadata from AWS S3

### Viewers & Browsers
- [**AWS/Sinergise "Sentinel Image Browser"**](http://sentinel-pds.s3-website.eu-central-1.amazonaws.com/browser.html)
  - search Sentinel-2 data available on Amazon Webservices
- [**EOS "Land Viewer"**](https://lv.eos.com/)
  - viewer for Landsat-8/7, MODIS and Sentinel-2 data hosted by AWS
  - visualize band combinations on-the-fly
- [**jeobrowser "Rocket"**](https://mapshup.com/projects/rocket)
  - viewer for Sentinel (1,2,3), Landsat-8, SPOT and Pleiades imagery
  - based on [resto](https://github.com/jjrom/resto) search engine and used as frontend for [PEPS](https://peps.cnes.fr/rocket/)
- [**mundialis "EO-me"**](http://eome.mundialis.de/eome/client/index.html)
  - viewer for Sentinel-2 and Landsat-8 data with custom metadata filters
- [**RemotePixel "Viewer"**](https://viewer.remotepixel.ca)
  - [open source](https://github.com/RemotePixel/viewer.remotepixel.ca) viewer for Landsat-8, Sentinel-2 and CBERS-4 data hosted by AWS
  - uses [**`sentinel-tiler`**](https://github.com/mapbox/sentinel-tiler) (tiles server based on AWS Lambda)
- [**RemotePixel "Satellite Search"**](https://remotepixel.ca/projects/satellitesearch.html)
  - [open source](https://github.com/RemotePixel/satellitesearch) Browser for Landsat-8 and Sentinel-2 data hosted by AWS
  - supports on-the-fly display and calculation of band combinations
  - uses [**`remotepixel-api`**](https://github.com/RemotePixel/remotepixel-api) (based on AWS Lambda)
- [**Sinergise "Sentinel Playground"**](http://apps.sentinel-hub.com/sentinel-playground)
  - visualize AWS Sentinel-2 data in different band combinations
  - offers a [WMS/WMTS service](http://www.sentinel-hub.com/apps/wms).
- [**Sinergise "EO-browser"**](http://apps.sentinel-hub.com/eo-browser/)
  - search Sentinel-1, 2, 3 and other free satellite data
  - supports pixel based band-math operations and [simple data processing](http://www.sentinel-hub.com/blog/eo-browser-goes-public)

### Processing
- [**`SNAP` (Sentinel Application Plattform)**](http://step.esa.int/main/toolboxes/snap/)
  - (pre-)process any Sentinel data
  - also available as [docker](https://github.com/edwardpmorris/docker-snap)
- [**`Sen2Cor`**](http://step.esa.int/main/third-party-plugins-2/sen2cor/)
  - atmospheric correction of Sentinel-2 data
  - also available as [python package](https://github.com/umwilm/SEN2COR)
- [**`MAJA` (MACCS ATCOR Joint Algorithm)** ](https://logiciels.cnes.fr/en/content/maja)
  - atmospheric correction of Sentinel-2 data using time series
  - used for [Theia](https://theia.cnes.fr/atdistrib/rocket/#/search?collection=SENTINEL2) and [`Sen2-Agri`](https://github.com/Sen2Agri/Sen2Agri-System)
- [**`iCOR`**](https://blog.vito.be/remotesensing/icor_available)
  - atmospheric correction of Sentinel-2 data
  - available as `SNAP` plugin
- [**Google Earth Engine**](https://earthengine.google.com/)
  - process the global Sentinel-1 and Sentinel-2 archives directly on Google's servers
- [**`Sen2-Agri`**](https://github.com/Sen2Agri/Sen2Agri-System)
  - toolbox for processing images for agricultural purposes
  - includes modules for atmospheric correction, monthly syntheses, biophysical variables, crop mask, crop-type classification and an [orchestrator](http://www.esa-sen2agri.org/operational-system/system-description/)

 ## Products
 Products, datasets and applications generated from Copernicus Sentinel data.

- [**EOX "Sentinel-2 cloudless"**](https://s2maps.eu/)
  - cloudless, [medium brightness](https://eox.at/2017/03/sentinel-2-cloudless/), [global](https://eox.at/2017/08/sentinel-2-global-cloudless-mosaic) Sentinel-2 composite
  - also provided as [WMTS Layer](https://tiles.maps.eox.at/wmts/1.0.0/WMTSCapabilities.xml) under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
  - [original GeoTIFF tiles](https://eox.at/2017/03/sentinel-2-cloudless-original-tiles-available/) provided on AWS S3 bucket
