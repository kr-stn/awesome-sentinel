# Awesome Sentinel [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of awesome tools, tutorials and APIs related to data from the [Copernicus Sentinel Satellites](http://www.copernicus.eu/main/sentinels).

![Copernicus logo](https://www.esa.int/var/esa/storage/images/esa_multimedia/images/2013/08/copernicus_logo/12986716-3-eng-GB/Copernicus_logo.jpg)

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
- [**Luxembourg National Mirror**](https://www.collgs.lu/)
- [**Norway National Mirror**](https://colhub.met.no/#/home)
- [**Portugal National Mirror**](https://ipsentinel.ipma.pt/dhus/#/home)
- [**Sweden National Mirror (SWEA)**](http://swea.rymdstyrelsen.se/portal/)
- [**United Kingdom National Mirror (SEDAS)**](http://sedas.satapps.org/)

### Partial Mirrors
Initiatives to integrate specific Sentinel data into existing search and discovery platforms.

- [**Alaska Satellite Facility (Sentinel-1)**](https://www.asf.alaska.edu/sentinel/)
- [**Centre for Environmental Data Analysis - CEDA (Sentinel-1, -2)**](http://catalogue.ceda.ac.uk/search/?search_term=sentinel&return_obj=ob&search_obj=ob)
- [**Theia (Sentinel-2)**](https://theia.cnes.fr/atdistrib/rocket/#/search?collection=SENTINEL2)
  - atmospherically corrected L2A products covering several European countries and [areas proposed by scientists](http://www.cesbio.ups-tlse.fr/multitemp/?page_id=7501)
  - published less than two days after L1C is available
- [**USGS EarthExplorer (Sentinel-2)**](https://earthexplorer.usgs.gov/)
- [**EUMETSAT CODA (Sentinel-3 Marine Products)**](https://coda.eumetsat.int/#/home)
  - 14 day rolling archive of Sentinel-3 L1 and L2 marine products in near real-time (NRT), short time critical (STC) and non time critical (NTC) latency mode
- [**DLR Geoservice (Sentinel-2)**](https://geoservice.dlr.de/web/)
  - [Download](https://download.geoservice.dlr.de/S2_L2A_MAJA/files/) 2 years rolling archive of MAJA-corrected Sentinel-2 scenes covering Germany
- [**NOAA CoastWatch**](https://coastwatch.noaa.gov/)
    - Sentinel-3 OLCI and Sentinel-2 over United States coasts
- [**NASA Earthdata**](https://search.earthdata.nasa.gov/)
    - search NASA mirrors for Sentinel-1, Sentinel-3, and Sentinel-5P

### Cloud Providers
Providers that host Copernicus Sentinel data and allow you to bring your own code to process it without the need to download the data.

- [**Open data on AWS**](https://registry.opendata.aws/tag/satellite-imagery/)
  - [Sentinel-2 L1C and L2A](https://registry.opendata.aws/sentinel-2/) hosted in region `eu-central-1` (Frankfurt), requester-pays S3 buckets
  - [Sentinel-2 L2A Cloud-Optimized GeoTIFFs](https://registry.opendata.aws/sentinel-2-l2a-cogs/), hosted in region `us-west-2` (Oregon), S3 buckets
    - [STAC Browser](https://sentinel.stac.cloud/?t=catalogs) for Sentinel-2 COG hosted on AWS
  - [Sentinel-1 GRD](https://registry.opendata.aws/sentinel-1/) hosted in region `eu-central-1` (Frankfurt), requester-pays S3 buckets
  - [Sentinel-1 ARD CONUS](https://registry.opendata.aws/sentinel-1-rtc-indigo/) - analysis ready dataset of Sentinel-1, tiled COGs, for contiguous United States
  - [Sentinel-3 NRT, STC, NTC, COG](https://registry.opendata.aws/sentinel-3/) - all Sentinel-3 products for near-real time, short time critical and not time critical, all products also available converted to COGs
  - [Sentinel-5P L2](https://registry.opendata.aws/sentinel5p/) -  all Level-2 products from Sentinel-5P, also available as COG converted data
- [**Google (Sentinel-2)**](https://cloud.google.com/storage/docs/public-datasets/sentinel-2)
  - public [Google Cloud Storage bucket](https://console.cloud.google.com/storage/browser/gcp-public-data-sentinel-2/?pli=1), `.SAFE` format, EU region
- [**Planet**](https://www.planet.com/pulse/sentinel-2-and-landsat-8-data-now-available-on-the-planet-platform/)
  - Sentinel-2 included in commercial API

### DIAS
[Data and Information Access Services (DIAS)](https://www.copernicus.eu/en/access-data/dias), funded by the European Commission "providing  centralised  access  to  Copernicus  data  and  information,  as  well as to processing tools"
- [**CREODIAS**](https://creodias.eu/)
  - full Sentinel archive, free visualization and download through [data discovery portal](https://finder.creodias.eu/www/) and [CREODIAS Browser](http://browser.creodias.eu/)
  - large EO [data archive](https://creodias.eu/data-offer) including Landsat, Envisat and others, next to Copernicus data
- [**MUNDI**](https://mundiwebservices.com)
  - Sentinel archive, free visualization and download through [mundi web services](https://mundiwebservices.com/geodata/)
- [**ONDA DIAS**](https://www.onda-dias.eu/cms/)
  - VM Infrastructure as a Service, with an API for access to hosted Copernicus data
- [**sobloo**](https://sobloo.eu)
  - on-demand processing of thematic products with link to other data-sets (i.e. geo-marketing)
- [**WEkEO**](https://wekeo.eu/)
  - harmonised data access with a REST API, hosted VM options

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
- [**`eodag`**](https://github.com/CS-SI/eodag)
  - command line tool and plugin-oriented Python framework for search and download from [multiple providers](https://eodag.readthedocs.io/en/latest/intro.html#available-providers) including all DIAS

### Viewers & Portals
- [**AWS/Sinergise "Sentinel Image Browser"**](http://sentinel-pds.s3-website.eu-central-1.amazonaws.com/browser.html)
  - search Sentinel-2 data available on Amazon Webservices
- [**EOS "Land Viewer"**](https://lv.eos.com/)
  - viewer for Landsat-8/7, MODIS and Sentinel-2 data hosted by AWS
  - visualize band combinations on-the-fly
- [**jeobrowser "Rocket"**](https://mapshup.com/projects/rocket)
  - viewer for Sentinel (1,2,3), Landsat-8, SPOT and Pleiades imagery
  - based on [resto](https://github.com/jjrom/resto) search engine and used as frontend for [PEPS](https://peps.cnes.fr/rocket/)
- [**mundialis "EO-me"**](https://www.mundialis.de/en/earth-observation-metadata-enhancer/)
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
- [**USGS "Sentinel2Look"**](https://landsatlook.usgs.gov/sentinel2/viewer.html)
    - variant of the [LandsatLook Viewer](https://landsatlook.usgs.gov/) to search and download Sentinel-2 data from the USGS archive
- [**ESRI Sentinel-2 Explorer**](https://sentinel2explorer.esri.com/)
    - view Sentinel-2 data rendered with a [number of indexes](https://www.arcgis.com/home/group.html?id=658741129719420f83d503a3ba743def#overview)
    - available as [ArcGIS ImageServer (REST)](https://sentinel.arcgis.com/arcgis/rest/services/Sentinel2/ImageServer)

### Processing
- [**`SNAP` (Sentinel Application Plattform)**](http://step.esa.int/main/toolboxes/snap/)
  - (pre-)process any Sentinel data
  - also available as [docker](https://github.com/edwardpmorris/docker-snap)
- [**`ARCSI` (Atmospheric and Radiometric Correction of Satellite Imagery)**](https://www.arcsi.remotesensing.info/)
  - atmospheric correction of Sentinel-2 data
- [**Google Earth Engine**](https://earthengine.google.com/)
  - process the global Sentinel archives directly on Google's servers
- [**EOS Processing**](https://processing.eos.com/)
  - workflow library for thematic processing of (Sentinel-2) satellite data
- [**`iCOR`**](https://blog.vito.be/remotesensing/icor_available)
  - atmospheric correction of Sentinel-2 data
  - available as `SNAP` plugin
- [**`MAJA` (MACCS ATCOR Joint Algorithm)** ](https://logiciels.cnes.fr/en/content/maja)
  - atmospheric correction of Sentinel-2 data using time series
  - used for [Theia](https://theia.cnes.fr/atdistrib/rocket/#/search?collection=SENTINEL2) and [`Sen2-Agri`](https://github.com/Sen2Agri/Sen2Agri-System)
- [**`Sen2-Agri`**](https://github.com/Sen2Agri/Sen2Agri-System)
  - toolbox for processing images for agricultural purposes
  - includes modules for atmospheric correction, monthly syntheses, biophysical variables, crop mask, crop-type classification and an [orchestrator](http://www.esa-sen2agri.org/operational-system/system-description/)
- [**`s2cloudless`**](https://github.com/sentinel-hub/sentinel2-cloud-detector)
  - single scene, pixel-based cloud detection algorithm used at [Sentinel-Hub](https://www.sentinel-hub.com/)
  - [accompanying write-up](https://medium.com/sentinel-hub/improving-cloud-detection-with-machine-learning-c09dc5d7cf13) with performance comparison to other cloud detection algorithms
- [**`Sen2Cor`**](http://step.esa.int/main/third-party-plugins-2/sen2cor/)
  - atmospheric correction of Sentinel-2 data
  - basis for [L2A](https://sentinel.esa.int/web/sentinel/technical-guides/sentinel-2-msi/level-2a/algorithm) data published on Copernicus Open Access Hub
- [**`sen2r`**](https://github.com/ranghetti/sen2r)
  - R toolbox to search, download and pre-process Sentinel-2 data
- [**`ACOLITE`**](https://github.com/acolite/acolite)
  - atmospheric correction algorithms for aquatic applications of Landsat and Sentinel-2
- [**`C2RCC`**](https://github.com/bcdev/s3tbx-c2rcc)
  - atmospheric correction of Sentinel-3 and -2 for coast colour applications
  - included in the `SNAP` toolbox for Sentinel-3
- [**`i.sentinel.mask`**](https://grass.osgeo.org/grass7/manuals/addons/i.sentinel.mask.html)
  - GRASS GIS addon for atmospheric correction of Sentinel-2 including cloud and shadow detection
- [**`sat-stac-sentinel`**](https://github.com/sat-utils/sat-stac-sentinel)
  - convert original Sentinel-1 and -2 metadata into [STAC](https://stacspec.org/) items
- [**`xsar`**](https://github.com/oarcher/xsar)
  -  Sentinel-1 Level 1 python reader for efficient xarray/dask based processor
  -  Denoising and calibration luts applied
 
## Products
Products, datasets and applications generated from Copernicus Sentinel data.

- [**EOX "Sentinel-2 cloudless"**](https://s2maps.eu/)
  - cloudless, [medium brightness](https://eox.at/2017/03/sentinel-2-cloudless/), [global](https://eox.at/2017/08/sentinel-2-global-cloudless-mosaic) Sentinel-2 composite
  - also provided as [WMTS Layer](https://tiles.maps.eox.at/wmts/1.0.0/WMTSCapabilities.xml) under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
  - [original GeoTIFF tiles](https://eox.at/2017/03/sentinel-2-cloudless-original-tiles-available/) provided on AWS S3 bucket
- [**S2GLC Land Cover Map of Europe 2017**](http://s2glc.cbk.waw.pl/extension)
  - tiles in MGRS (Sentinel-2) available at [CREODIAS Finder](https://finder.creodias.eu/) (collection: S2GLC)
