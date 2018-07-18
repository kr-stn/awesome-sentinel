# Awesome Sentinel [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of awesome tools, tutorials and APIs related to data from the [Copernicus Sentinel Satellites](http://www.copernicus.eu/main/sentinels).

![Copernicus logo](http://emergency.copernicus.eu/mapping/sites/all/themes/gmes960/images/Copernicus_fb.png)

## Data Access

### Data Hubs and National Mirrors
Official datahubs and mirrors by the Copernicus partners and [Collaborative Ground Segment members](https://sentinels.copernicus.eu/web/sentinel/missions/collaborative/national-points-of-contact).

- [**Copernicus Open Access Hub (SciHub)**](https://scihub.copernicus.eu/)
- [**Australia National Mirror**](https://copernicus.nci.org.au/)
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
Providers that host Copernicus Sentinel data and allow you to bring your own code to process it without the need to download the data.

- [**Amazon Web Services**](http://sentinel-pds.s3-website.eu-central-1.amazonaws.com/)
  - Sentinel-2 L1C and L2A, Sentinel-1, hosted in region eu-central-1 (Frankfurt), requester-pays S3 buckets
- [**CREODIAS**](https://creodias.eu/)
  - full Sentinel archive, free visualization and download through [data discovery portal](https://finder.creodias.eu/www/) and [CREODIAS Browser](http://browser.creodias.eu/) 
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
- [**`sentinelhub-py`**](https://github.com/sentinel-hub/sentinelhub-py)
  - Python library for downloading Sentinel-2 data from Amazon into ESA .SAFE format and interface [Sentinel Hub OGC services](https://www.sentinel-hub.com/develop/capabilities/wms)
- [**`aws-sat-api`**](https://github.com/RemotePixel/aws-sat-api)
  - Simple Serverless API for satellite data hosted on AWS Public Dataset
- [**`sentinel2-search-api`**](https://github.com/beaorn/sentinel2-search-api)
  - query Sentinel-2 data hosted on AWS by MGRS tile
  - API deployed at [https://sentinel2.satgateway.com](https://sentinel2.satgateway.com), tile preview front-end deployed at [https://s2viewer.satgateway.com](https://s2viewer.satgateway.com)
- [**`sentinel2_aws`**](https://github.com/beaorn/sentinel2_aws)
  - Ruby gem for parsing Sentinel-2 metadata from AWS

### Viewers & Portals
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
  - satellite tiles enriched with additional metadata (e.g. terrain statistics, NDVI at overpass, climatic parameters, population count)
- [**OceanDataLab**](https://www.oceandatalab.com)
  - portals focussing on Ocean Remote Sensing data, including Sentinel-1 and 3
- [**RemotePixel "Viewer"**](https://viewer.remotepixel.ca)
  - [open source](https://github.com/RemotePixel/viewer.remotepixel.ca) viewer for Landsat-8, Sentinel-2 and CBERS-4 data hosted by AWS
  - uses [**`sentinel-tiler`**](https://github.com/mapbox/sentinel-tiler) (tiles server based on AWS Lambda)
- [**RemotePixel "Satellite Search"**](https://remotepixel.ca/projects/satellitesearch.html)
  - [open source](https://github.com/RemotePixel/satellitesearch) Browser for Landsat-8 and Sentinel-2 data hosted by AWS
  - supports on-the-fly display and calculation of band combinations
  - uses [**`remotepixel-api`**](https://github.com/RemotePixel/remotepixel-api) (based on AWS Lambda)
- [**Research and User Support (RUS)**](https://rus-copernicus.eu/)
  - service portal to promote the uptake of Copernicus data and scaling of R&D activities
  - provides [training](https://rus-copernicus.eu/portal/the-rus-offer/training/) and [computing environments](https://rus-copernicus.eu/portal/the-rus-offer/ict-offer/)
- [**Sinergise "Sentinel Playground"**](http://apps.sentinel-hub.com/sentinel-playground)
  - visualize AWS Sentinel-2 data in different band combinations
  - offers a [WMS/WMTS service](http://www.sentinel-hub.com/apps/wms).
- [**Sinergise "Sentinel-Hub"**](https://www.sentinel-hub.com/)
  - search Sentinel-1, 2, 3 and other free satellite data
  - supports pixel based band-math operations and [simple data processing](http://www.sentinel-hub.com/blog/eo-browser-goes-public)
- [**SnapPlanet**](https://snapplanet.io/)
  - [Android](https://play.google.com/store/apps/details?id=io.snapplanet.app) / [iOS](https://itunes.apple.com/WebObjects/MZStore.woa/wa/viewSoftware?id=1175935057) App to to view Sentinel-2 images, compare changes and share
- [**Spectator**](https://spectator.earth/)
  - real-time tracking of EO satellites, set-up custom channels to track ROI overpass and preview images
- [**Thematic Exploitation Platforms "TEPs"**](https://tep.eo.esa.int/)
  - platforms for finding and processing (Sentinel) data relating to a thematic topic
  - available platforms: [Coastal](https://coastal-tep.eo.esa.int/portal), [Forestry](https://forestry-tep.eo.esa.int/), [Geohazards](https://geohazards-tep.eo.esa.int/), [Hydrology](https://hydrology-tep.eo.esa.int/), [Polar](https://polar-tep.eo.esa.int/), [Urban](https://urban-tep.eo.esa.int/#!), [Food Security](https://foodsecurity-tep.eo.esa.int/)

### Processing
- [**`SNAP` (Sentinel Application Plattform)**](http://step.esa.int/main/toolboxes/snap/)
  - (pre-)process any Sentinel data
  - also available as [docker](https://github.com/edwardpmorris/docker-snap)
- [**`ARCSI` (Atmospheric and Radiometric Correction of Satellite Imagery)**](https://www.arcsi.remotesensing.info/)
  - atmospheric correction of Sentinel-2 data
- [**Google Earth Engine**](https://earthengine.google.com/)
  - process the global Sentinel archives directly on Google's servers
- [**`iCOR`**](https://blog.vito.be/remotesensing/icor_available)
  - atmospheric correction of Sentinel-2 data
  - available as `SNAP` plugin
- [**`MAJA` (MACCS ATCOR Joint Algorithm)** ](https://logiciels.cnes.fr/en/content/maja)
  - atmospheric correction of Sentinel-2 data using time series
  - used for [Theia](https://theia.cnes.fr/atdistrib/rocket/#/search?collection=SENTINEL2) and [`Sen2-Agri`](https://github.com/Sen2Agri/Sen2Agri-System)
- [**`Sen2-Agri`**](https://github.com/Sen2Agri/Sen2Agri-System)
  - toolbox for processing images for agricultural purposes
  - includes modules for atmospheric correction, monthly syntheses, biophysical variables, crop mask, crop-type classification and an [orchestrator](http://www.esa-sen2agri.org/operational-system/system-description/)
- [**`sentinel2-cloud-detector`**](https://github.com/sentinel-hub/sentinel2-cloud-detector)
  - single scene, pixel-based cloud detection algorithm used at [Sentinel-Hub](https://www.sentinel-hub.com/)
  - [accompanying write-up](https://medium.com/sentinel-hub/improving-cloud-detection-with-machine-learning-c09dc5d7cf13) with performance comparison to other cloud detection algorithms
- [**`Sen2Cor`**](http://step.esa.int/main/third-party-plugins-2/sen2cor/)
  - atmospheric correction of Sentinel-2 data
  - basis for [L2A](https://sentinel.esa.int/web/sentinel/technical-guides/sentinel-2-msi/level-2a/algorithm) data published on Copernicus Open Access Hub


## Products
Products, datasets and applications generated from Copernicus Sentinel data.

- [**EOX "Sentinel-2 cloudless"**](https://s2maps.eu/)
  - cloudless, [medium brightness](https://eox.at/2017/03/sentinel-2-cloudless/), [global](https://eox.at/2017/08/sentinel-2-global-cloudless-mosaic) Sentinel-2 composite
  - also provided as [WMTS Layer](https://tiles.maps.eox.at/wmts/1.0.0/WMTSCapabilities.xml) under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
  - [original GeoTIFF tiles](https://eox.at/2017/03/sentinel-2-cloudless-original-tiles-available/) provided on AWS S3 bucket
