CRAN Task View: Analysis of Spatial Data
----------------------------------------

                                                            
**Maintainer:** Roger Bivand                                
**Contact:**    Roger.Bivand at nhh.no                      
**Version:**    2018-06-02                                  
**URL:**        <https://CRAN.R-project.org/view=Spatial>   

Base R includes many functions that can be used for reading, visualising, and analysing spatial data.
The focus in this view is on "geographical" spatial data, where observations can be identified with geographical locations, and where additional information about these locations may be retrieved if the location is recorded with care.
Base R functions are complemented by contributed packages, some of which are on CRAN, and others are still in development.
One active location is [R-Forge](http://R-Forge.R-project.org/), which lists "Spatial Data and Statistics" projects in its [project tree](http://R-Forge.R-project.org/softwaremap/trove_list.php).
Information on R-spatial packages, especially [sp](https://cran.r-project.org/package=sp) is posted on the R-Forge rspatial project [website](http://rspatial.R-Forge.R-project.org/), including a visualisation gallery.
Active development of [sp](https://cran.r-project.org/package=sp) is continuing on [<span class="GitHub">sp</span>](https://github.com/edzer/sp/).

The contributed packages address two broad areas: moving spatial data into and out of R, and analysing spatial data in R.

The [R-SIG-Geo](https://stat.ethz.ch/mailman/listinfo/R-SIG-Geo/) mailing-list is a good place to begin for obtaining help and discussing questions about both accessing data, and analysing it.
The mailing list is a good place to search for information about relevant courses.
Further information about courses may be found under the "Events" tab of [this blog](http://r-spatial.org/).

There are a number of contributed tutorials and introductions; a recent one is [Introduction to visualising spatial data in R](https://cran.r-project.org/doc/contrib/intro-spatial-rl.pdf) by Robin Lovelace and James Cheshire.
The packages in this view can be roughly structured into the following topics.
If you think that some package is missing from the list, please let me know.

-   **Classes for spatial data** : Because many of the packages importing and using spatial data have had to include objects of storing data and functions for visualising it, an initiative is in progress to construct shared classes and plotting functions for spatial data.
The [sp](https://cran.r-project.org/package=sp) package is discussed in a note in [R News](http://CRAN.R-project.org/doc/Rnews/Rnews_2005-2.pdf).
A new package called [sf](https://cran.r-project.org/package=sf) is now on CRAN, and is being actively developed on [<span class="GitHub">sfr</span>](https://github.com/edzer/sfr/), providing Simple Features for R.
The development of the package is being supported by the R Consortium.
It provides simple features access for vector data, and as such is a modern implementation of parts of [sp](https://cran.r-project.org/package=sp).
Many other packages have become dependent on the [sp](https://cran.r-project.org/package=sp) classes, including [rgdal](https://cran.r-project.org/package=rgdal) and [maptools](https://cran.r-project.org/package=maptools).
The [rgeos](https://cran.r-project.org/package=rgeos) package provides an interface to topology functions for [sp](https://cran.r-project.org/package=sp) objects using [GEOS](http://trac.osgeo.org/geos/).
The [stplanr](https://cran.r-project.org/package=stplanr) provides a "SpatialLinesNetwork" class based on objects defined in [sp](https://cran.r-project.org/package=sp) and [igraph](https://cran.r-project.org/package=igraph) that can be used for routing analysis within R.
Another network package is [shp2graph](https://cran.r-project.org/package=shp2graph).
The [cleangeo](https://cran.r-project.org/package=cleangeo) may be used to inspect spatial objects, facilitate handling and reporting of topology errors and geometry validity issues.
It claims to provide a geometry cleaner that will fix all geometry problems, and eliminate (at least reduce) the likelihood of having issues when doing spatial data processing.
The [raster](https://cran.r-project.org/package=raster) package is a major extension of spatial data classes to virtualise access to large rasters, permitting large objects to be analysed, and extending the analytical tools available for both raster and vector data.
Used with [rasterVis](https://cran.r-project.org/package=rasterVis), it can also provide enhanced visualisation and interaction.
The [spatial.tools](https://cran.r-project.org/package=spatial.tools) package contains spatial functions meant to enhance the core functionality of the [raster](https://cran.r-project.org/package=raster) package, including a parallel processing engine for use with rasters.
The [micromap](https://cran.r-project.org/package=micromap) package provides linked micromaps using ggplot2.
The [recmap](https://cran.r-project.org/package=recmap) package provides rectangular cartograms with rectangle sizes reflecting for example population; the [statebins](https://cran.r-project.org/package=statebins) provides a simpler binning approach to US states.
The [spacetime](https://cran.r-project.org/package=spacetime) package extends the shared classes defined in [sp](https://cran.r-project.org/package=sp) for spatio-temporal data (see [Spatio-Temporal Data in R](http://www.jstatsoft.org/v51/i07)).
The [Grid2Polygons](https://cran.r-project.org/package=Grid2Polygons) converts a spatial object from class SpatialGridDataFrame to SpatialPolygonsDataFrame.

    An alternative approach to some of these issues is implemented in the [PBSmapping](https://cran.r-project.org/package=PBSmapping) package; [PBSmodelling](https://cran.r-project.org/package=PBSmodelling) provides modelling support.
In addition, [GEOmap](https://cran.r-project.org/package=GEOmap) provides mapping facilities directed to meet the needs of geologists, and uses the [geomapdata](https://cran.r-project.org/package=geomapdata) package.

-   **Handling spatial data** : A number of packages have been written using sp classes.
The [raster](https://cran.r-project.org/package=raster) package introduces many GIS methods that now permit much to be done with spatial data without having to use GIS in addition to R.
It may be complemented by [gdistance](https://cran.r-project.org/package=gdistance), which provided calculation of distances and routes on geographic grids.
[geosphere](https://cran.r-project.org/package=geosphere) permits computations of distance and area to be carried out on spatial data in geographical coordinates.
The [spsurvey](https://cran.r-project.org/package=spsurvey) package provides a range of sampling functions.
The [trip](https://cran.r-project.org/package=trip) package extends sp classes to permit the accessing and manipulating of spatial data for animal tracking.
[spcosa](https://cran.r-project.org/package=spcosa) provides spatial coverage sampling and random sampling from compact geographical strata.
The [magclass](https://cran.r-project.org/package=magclass) offers a data class for increased interoperability working with spatial-temporal data together with corresponding functions and methods (conversions, basic calculations and basic data manipulation).
The class distinguishes between spatial, temporal and other dimensions to facilitate the development and interoperability of tools build for it.
Additional features are name-based addressing of data and internal consistency checks (e.g.
checking for the right data order in calculations).

    The UScensus2000 suite of packages ([UScensus2000cdp](https://cran.r-project.org/package=UScensus2000cdp), [UScensus2000tract](https://cran.r-project.org/package=UScensus2000tract)) makes the use of data from the 2000 US Census more convenient.
An important data set, Guerry's "Moral Statistics of France", has been made available in the [Guerry](https://cran.r-project.org/package=Guerry) package, which provides data and maps and examples designed to contribute to the integration of multivariate and spatial analysis.
The [marmap](https://cran.r-project.org/package=marmap) package is designed for downloading, plotting and manipulating bathymetric and topographic data in R.
[marmap](https://cran.r-project.org/package=marmap) can query the ETOPO1 bathymetry and topography database hosted by the NOAA, use simple latitude-longitude-depth data in ascii format, and take advantage of the advanced plotting tools available in R to build publication-quality bathymetric maps (see the [PLOS](http://www.plosone.org/article/info%3Adoi%2F10.1371%2Fjournal.pone.0073051) paper).
Modern country boundaries are provided at 2 resolutions by [rworldmap](https://cran.r-project.org/package=rworldmap) along with functions to join and map tabular data referenced by country names or codes.
Chloropleth and bubble maps are supported and general functions to work on user supplied maps (see [A New R package for Mapping Global Data](http://journal.r-project.org/archive/2011-1/RJournal_2011-1_South.pdf).
Higher resolution country borders are available from the linked package [rworldxtra](https://cran.r-project.org/package=rworldxtra).
Historical country boundaries (1946-2012) can be obtained from the [cshapes](https://cran.r-project.org/package=cshapes) package along with functions for calculating distance matrices (see [Mapping and Measuring Country Shapes](http://journal.r-project.org/archive/2010-1/RJournal_2010-1_Weidmann+Skrede~Gleditsch.pdf)).

    The [landsat](https://cran.r-project.org/package=landsat) package with accompanying [JSS paper](http://www.jstatsoft.org/v43/i04) provides tools for exploring and developing correction tools for remote sensing data.
[taRifx](https://cran.r-project.org/package=taRifx) is a collection of utility and convenience functions, and some interesting spatial functions.
The [gdalUtils](https://cran.r-project.org/package=gdalUtils) package provides wrappers for the Geospatial Data Abstraction Library (GDAL) Utilities.

    An rOpenSci [blog entry](http://ropensci.org/blog/blog/2016/11/22/geospatial-suite) described a GeoJSON-centred approach to reading GeoJSON and WKT data.
GeoJSON can be written and read using [rgdal](https://cran.r-project.org/package=rgdal), and WKT by [rgeos](https://cran.r-project.org/package=rgeos).
The entry lists [geojson](https://cran.r-project.org/package=geojson), [geojsonio](https://cran.r-project.org/package=geojsonio), [geoaxe](https://cran.r-project.org/package=geoaxe) and [lawn](https://cran.r-project.org/package=lawn) among others.
The [rgbif](https://cran.r-project.org/package=rgbif) package is used to access Global Biodiversity Information Facility (GBIF) data).
The [geoaxe](https://cran.r-project.org/package=geoaxe) allows users to split 'geospatial' objects into pieces.
The [lawn](https://cran.r-project.org/package=lawn) package is a client for 'Turfjs' for 'geospatial' analysis.

-   **Reading and writing spatial data - [rgdal](https://cran.r-project.org/package=rgdal)** : Maps may be vector-based or raster-based.
The [rgdal](https://cran.r-project.org/package=rgdal) package provides bindings to [GDAL](http://www.gdal.org/) -supported raster formats and [OGR](http://www.gdal.org/ogr/) -supported vector formats.
It contains functions to write raster files in supported formats.
The package also provides [PROJ.4](http://trac.osgeo.org/proj/) projection support for vector objects ([this site](http://spatialreference.org) provides searchable online PROJ.4 representations of projections).
Affine and similarity transformations on sp objects may be made using functions in the [vec2dtransf](https://cran.r-project.org/package=vec2dtransf) package.
The Windows and Mac OSX CRAN binaries of [rgdal](https://cran.r-project.org/package=rgdal) include subsets of possible data source drivers; if others are needed, use other conversion utilities, or install from source against a version of GDAL with the required drivers.
The [rgeos](https://cran.r-project.org/package=rgeos) package provides functions for reading and writing well-known text (WKT) geometry, and the [wkb](https://cran.r-project.org/package=wkb) package provides functions for reading and writing well-known binary (WKB) geometry.

-   **Reading and writing spatial data - other packages** : There are a number of other packages for accessing vector data on CRAN: [maps](https://cran.r-project.org/package=maps) (with [mapdata](https://cran.r-project.org/package=mapdata) and [mapproj](https://cran.r-project.org/package=mapproj)) provides access to the same kinds of geographical databases as S - [RArcInfo](https://cran.r-project.org/package=RArcInfo) allows ArcInfo v.7 binary files and \*.e00 files to be read, and [maptools](https://cran.r-project.org/package=maptools) and [shapefiles](https://cran.r-project.org/package=shapefiles) read and write ArcGIS/ArcView shapefiles; for NetCDF files, [ncdf4](https://cran.r-project.org/package=ncdf4) or [RNetCDF](https://cran.r-project.org/package=RNetCDF) may be used.
The [maptools](https://cran.r-project.org/package=maptools) package also provides helper functions for writing map polygon files to be read by WinBUGS, Mondrian, and the tmap command in Stata.
It also provides interface functions between [PBSmapping](https://cran.r-project.org/package=PBSmapping) and [spatstat](https://cran.r-project.org/package=spatstat) and sp classes, in addition to [maps](https://cran.r-project.org/package=maps) databases and sp classes.
There is also an interface to GSHHS shoreline databases.
The [gmt](https://cran.r-project.org/package=gmt) package gives a simple interface between GMT map-making software and R.
[geonames](https://cran.r-project.org/package=geonames) is an interface to the [www.geonames.org](http://www.geonames.org/) service.
[OpenStreetMap](https://cran.r-project.org/package=OpenStreetMap) gives access to open street map raster images, and [osmar](https://cran.r-project.org/package=osmar) provides infrastructure to access OpenStreetMap data from different sources, to work with the data in common R manner, and to convert data into available infrastructure provided by existing R packages.

    The [rpostgis](https://cran.r-project.org/package=rpostgis) package provides additional functions to the 'RPostgreSQL' package to interface R with a 'PostGIS'-enabled database, as well as convenient wrappers to common 'PostgreSQL' queries.
The [postGIStools](https://cran.r-project.org/package=postGIStools) package provides functions to convert geometry and 'hstore' data types from 'PostgreSQL' into standard R objects, as well as to simplify the import of R data frames (including spatial data frames) into 'PostgreSQL'

    Integration with version 6.\* and of the leading open source GIS, GRASS, is provided in CRAN package [spgrass6](https://cran.r-project.org/package=spgrass6), using [rgdal](https://cran.r-project.org/package=rgdal) for exchanging data.
For GRASS 7.\*, use [rgrass7](https://cran.r-project.org/package=rgrass7).
[RPyGeo](https://cran.r-project.org/package=RPyGeo) is a wrapper for Python access to the ArcGIS GeoProcessor, and [RSAGA](https://cran.r-project.org/package=RSAGA) is a similar shell-based wrapper for SAGA commands.
The [RQGIS](https://cran.r-project.org/package=RQGIS) package establishes an interface between R and QGIS, i.e.
it allows the user to access QGIS functionalities from the R console.
It achieves this by using the QGIS Python API via the command line.
Note also [this thread](https://stat.ethz.ch/pipermail/r-sig-geo/2016-August/024817.html) on an alternative R/QGIS integration.

-   **Visualisation** : For visualization, the colour palettes provided in the [RColorBrewer](https://cran.r-project.org/package=RColorBrewer) package are very useful, and may be modified or extended using the `colorRampPalette` function provided with R.
The [classInt](https://cran.r-project.org/package=classInt) package provides functions for choosing class intervals for thematic cartography.
The [tmap](https://cran.r-project.org/package=tmap) package provides a modern basis for thematic mapping optionally using a Grammar of Graphics syntax.
Because it has a custom grid graphics platform, it obviates the need to fortify geometries to use with ggplot2.
The [mapview](https://cran.r-project.org/package=mapview) package provides methods to view spatial objects interactively, usually on a web mapping base; the [leaflet](https://cran.r-project.org/package=leaflet) is another alternative.
The [quickmapr](https://cran.r-project.org/package=quickmapr) package provides a simple method to visualize 'sp' and 'raster' objects, allows for basic zooming, panning, identifying, and labeling of spatial objects, and does not require that the data be in geographic coordinates.
The [cartography](https://cran.r-project.org/package=cartography) package allows various cartographic representations such as proportional symbols, choropleth, typology, flows or discontinuities.
The [mapmisc](https://cran.r-project.org/package=mapmisc) package is a minimal, light-weight set of tools for producing nice looking maps in R, with support for map projections.If the user wishes to place a map backdrop behind other displays, the the [RgoogleMaps](https://cran.r-project.org/package=RgoogleMaps) package for accessing Google Maps(TM) may be useful.
[ggmap](https://cran.r-project.org/package=ggmap) may be used for spatial visualisation with Google Maps and OpenStreetMap; [ggsn](https://cran.r-project.org/package=ggsn) provides North arrows and scales for such maps.
The [plotGoogleMaps](https://cran.r-project.org/package=plotGoogleMaps) package provides methods for the visualisation of spatial and spatio-temporal objects in Google Maps in a web browser.
[plotKML](https://cran.r-project.org/package=plotKML) is a package providing methods for the visualisation of spatial and spatio-temporal objects in Google Earth.
A further option is [leafletR](https://cran.r-project.org/package=leafletR), which provides basic web-mapping functionality to combine vector data files and online map tiles from different sources.

-   **Point pattern analysis** : The [spatial](https://cran.r-project.org/package=spatial) package is a recommended package shipped with base R, and contains several core functions, including an implementation of Khat by its author, Prof.
Ripley.
In addition, [spatstat](https://cran.r-project.org/package=spatstat) allows freedom in defining the region(s) of interest, and makes extensions to marked processes and spatial covariates.
Its strengths are model-fitting and simulation, and it has a useful [homepage](http://www.spatstat.org/).
It is the only package that will enable the user to fit inhomogeneous point process models with interpoint interactions.
The [spatgraphs](https://cran.r-project.org/package=spatgraphs) package provides graphs, graph visualisation and graph based summaries to be used with spatial point pattern analysis.
The [splancs](https://cran.r-project.org/package=splancs) package also allows point data to be analysed within a polygonal region of interest, and covers many methods, including 2D kernel densities.
The [smacpod](https://cran.r-project.org/package=smacpod) package provides various statistical methods for analyzing case-control point data.
The methods available closely follow those in chapter 6 of Applied Spatial Statistics for Public Health Data by Waller and Gotway (2004).

    [ecespa](https://cran.r-project.org/package=ecespa) provides wrappers, functions and data for spatial point pattern analysis, used in the book on Spatial Ecology of the ECESPA/AEET.
The functions for binning points on grids in [ash](https://cran.r-project.org/package=ash) may also be of interest.
The [ads](https://cran.r-project.org/package=ads) package perform first- and second-order multi-scale analyses derived from Ripley's K-function.
The [aspace](https://cran.r-project.org/package=aspace) package is a collection of functions for estimating centrographic statistics and computational geometries from spatial point patterns.
[DSpat](https://cran.r-project.org/package=DSpat) contains functions for spatial modelling for distance sampling data and [spatialsegregation](https://cran.r-project.org/package=spatialsegregation) provides segregation measures for multitype spatial point patterns.
[GriegSmith](https://cran.r-project.org/package=GriegSmith) uses the Grieg-Smith method on 2 dimensional spatial data.
The [dbmss](https://cran.r-project.org/package=dbmss) package allows simple computation of a full set of spatial statistic functions of distance, including classical ones (Ripley's K and others) and more recent ones used by spatial economists (Duranton and Overman's Kd, Marcon and Puech's M).
It relies on spatstat for core calculation.
[latticeDensity](https://cran.r-project.org/package=latticeDensity) contains functions that compute the lattice-based density estimator of Barry and McIntyre, which accounts for point processes in two-dimensional regions with irregular boundaries and holes.

-   **Geostatistics** : The [gstat](https://cran.r-project.org/package=gstat) package provides a wide range of functions for univariate and multivariate geostatistics, also for larger datasets, while [geoR](https://cran.r-project.org/package=geoR) and [geoRglm](https://cran.r-project.org/package=geoRglm) contain functions for model-based geostatistics.
Variogram diagnostics may be carried out with [vardiag](https://cran.r-project.org/package=vardiag).
Automated interpolation using [gstat](https://cran.r-project.org/package=gstat) is available in [automap](https://cran.r-project.org/package=automap).
This family of packages is supplemented by [intamap](https://cran.r-project.org/package=intamap) with procedures for automated interpolation.
A similar wide range of functions is to be found in the [fields](https://cran.r-project.org/package=fields) package.
The [spatial](https://cran.r-project.org/package=spatial) package is shipped with base R, and contains several core functions.
The [spBayes](https://cran.r-project.org/package=spBayes) package fits Gaussian univariate and multivariate models with MCMC.
[ramps](https://cran.r-project.org/package=ramps) is a different Bayesian geostatistical modelling package.
The [geospt](https://cran.r-project.org/package=geospt) package contains some geostatistical and radial basis functions, including prediction and cross validation.
Besides, it includes functions for the design of optimal spatial sampling networks based on geostatistical modelling.
[spsann](https://cran.r-project.org/package=spsann) is another package to offer functions to optimize sample configurations, using spatial simulated annealing.
The [geostatsp](https://cran.r-project.org/package=geostatsp) package offers geostatistical modelling facilities using Raster and SpatialPoints objects are provided.
Non-Gaussian models are fit using INLA, and Gaussian geostatistical models use Maximum Likelihood Estimation.
The [FRK](https://cran.r-project.org/package=FRK) package is a tool for spatial/spatio-temporal modelling and prediction with large datasets.
The approach, discussed in Cressie and Johannesson (2008), decomposes the field, and hence the covariance function, using a fixed set of n basis functions, where n is typically much smaller than the number of data points (or polygons) m.

    The [RandomFields](https://cran.r-project.org/package=RandomFields) package provides functions for the simulation and analysis of random fields, and variogram model descriptions can be passed between [geoR](https://cran.r-project.org/package=geoR), [gstat](https://cran.r-project.org/package=gstat) and this package.
[SpatialExtremes](https://cran.r-project.org/package=SpatialExtremes) proposes several approaches for spatial extremes modelling using [RandomFields](https://cran.r-project.org/package=RandomFields).
In addition, [CompRandFld](https://cran.r-project.org/package=CompRandFld), [constrainedKriging](https://cran.r-project.org/package=constrainedKriging) and [geospt](https://cran.r-project.org/package=geospt) provide alternative approaches to geostatistical modelling.
The [spTimer](https://cran.r-project.org/package=spTimer) package is able to fit, spatially predict and temporally forecast large amounts of space-time data using \[1\] Bayesian Gaussian Process (GP) Models, \[2\] Bayesian Auto-Regressive (AR) Models, and \[3\] Bayesian Gaussian Predictive Processes (GPP) based AR Models.
The [rtop](https://cran.r-project.org/package=rtop) package provides functions for the geostatistical interpolation of data with irregular spatial support such as runoff related data or data from administrative units.
The [georob](https://cran.r-project.org/package=georob) package provides functions for fitting linear models with spatially correlated errors by robust and Gaussian Restricted Maximum Likelihood and for computing robust and customary point and block kriging predictions, along with utility functions for cross-validation and for unbiased back-transformation of kriging predictions of log-transformed data.
The [SpatialTools](https://cran.r-project.org/package=SpatialTools) package has an emphasis on kriging, and provides functions for prediction and simulation.
It is extended by [ExceedanceTools](https://cran.r-project.org/package=ExceedanceTools), which provides tools for constructing confidence regions for exceedance regions and contour lines.
The [gear](https://cran.r-project.org/package=gear) package implements common geostatistical methods in a clean, straightforward, efficient manner, and is said to be a quasi reboot of [SpatialTools](https://cran.r-project.org/package=SpatialTools).
The [sperrorest](https://cran.r-project.org/package=sperrorest) package implements spatial error estimation and permutation-based spatial variable importance using different spatial cross-validation and spatial block bootstrap methods.
The [spm](https://cran.r-project.org/package=spm) package provides functions for hybrid geostatistical and machine learning methods for spatial predictive modelling.
It currently contains two commonly used geostatistical methods, two machine learning methods, four hybrid methods and two averaging methods.

    The [sgeostat](https://cran.r-project.org/package=sgeostat) package is also available.
Within the same general topical area are the [deldir](https://cran.r-project.org/package=deldir) and [tripack](https://cran.r-project.org/package=tripack) packages for triangulation and the [akima](https://cran.r-project.org/package=akima) package for spline interpolation; the [MBA](https://cran.r-project.org/package=MBA) package provides scattered data interpolation with multilevel B-splines.
In addition, there are the [spatialCovariance](https://cran.r-project.org/package=spatialCovariance) package, which supports the computation of spatial covariance matrices for data on rectangles, the [regress](https://cran.r-project.org/package=regress) package building in part on [spatialCovariance](https://cran.r-project.org/package=spatialCovariance), and the [tgp](https://cran.r-project.org/package=tgp) package.
The [Stem](https://cran.r-project.org/package=Stem) package provides for the estimation of the parameters of a spatio-temporal model using the EM algorithm, and the estimation of the parameter standard errors using a spatio-temporal parametric bootstrap.
[FieldSim](https://cran.r-project.org/package=FieldSim) is another random fields simulations package.
The [SSN](https://cran.r-project.org/package=SSN) is for geostatistical modeling for data on stream networks, including models based on in-stream distance.
Models are created using moving average constructions.
Spatial linear models, including covariates, can be fit with ML or REML.
Mapping and other graphical functions are included.
The [ipdw](https://cran.r-project.org/package=ipdw) provides functions o interpolate georeferenced point data via Inverse Path Distance Weighting.
Useful for coastal marine applications where barriers in the landscape preclude interpolation with Euclidean distances.
[RSurvey](https://cran.r-project.org/package=RSurvey) may be used as a processing program for spatially distributed data, and is capable of error corrections and data visualisation.

-   **Disease mapping and areal data analysis** : [DCluster](https://cran.r-project.org/package=DCluster) is a package for the detection of spatial clusters of diseases.
It extends and depends on the [spdep](https://cran.r-project.org/package=spdep) package, which provides basic functions for building neighbour lists and spatial weights, tests for spatial autocorrelation for areal data like Moran's I, and functions for fitting spatial regression models, such as SAR and CAR models.
These models assume that the spatial dependence can be described by known weights.
In [spdep](https://cran.r-project.org/package=spdep), the `ME` and `SpatialFiltering` functions provide Moran Eigenvector model fitting, as do more modern functions in the [spmoran](https://cran.r-project.org/package=spmoran) package.
The [SpatialEpi](https://cran.r-project.org/package=SpatialEpi) package provides implementations of cluster detection and disease mapping functions, including Bayesian cluster detection, and supports strata.
The [smerc](https://cran.r-project.org/package=smerc) package provides statistical methods for the analysis of data areal data, with a focus on cluster detection.
The [diseasemapping](https://cran.r-project.org/package=diseasemapping) package offers the formatting of population and case data, calculation of Standardized Incidence Ratios, and fitting the BYM model using INLA.
Regionalisation of polygon objects is provided by [AMOEBA](https://cran.r-project.org/package=AMOEBA): a function to calculate spatial clusters using the Getis-Ord local statistic.
It searches irregular clusters (ecotopes) on a map, and by `skater` in [spdep](https://cran.r-project.org/package=spdep).
The [seg](https://cran.r-project.org/package=seg) and [OasisR](https://cran.r-project.org/package=OasisR) packages provide functions for measuring spatial segregation; [OasisR](https://cran.r-project.org/package=OasisR) includes Monte Carlo simulations to test the indices.
The [spgwr](https://cran.r-project.org/package=spgwr) package contains an implementation of geographically weighted regression methods for exploring possible non-stationarity.
The [gwrr](https://cran.r-project.org/package=gwrr) package fits geographically weighted regression (GWR) models and has tools to diagnose and remediate collinearity in the GWR models.
Also fits geographically weighted ridge regression (GWRR) and geographically weighted lasso (GWL) models.
The [GWmodel](https://cran.r-project.org/package=GWmodel) package contains functions for computing geographically weighted models.
The [lctools](https://cran.r-project.org/package=lctools) package provides researchers and educators with easy-to-learn user friendly tools for calculating key spatial statistics and to apply simple as well as advanced methods of spatial analysis in real data.
These include: Local Pearson and Geographically Weighted Pearson Correlation Coefficients, Spatial Inequality Measures (Gini, Spatial Gini, LQ, Focal LQ), Spatial Autocorrelation (Global and Local Moran's I), several Geographically Weighted Regression techniques and other Spatial Analysis tools (other geographically weighted statistics).
This package also contains functions for measuring the significance of each statistic calculated, mainly based on Monte Carlo simulations.
The [sparr](https://cran.r-project.org/package=sparr) package provides another approach to relative risks.
The [CARBayes](https://cran.r-project.org/package=CARBayes) package implements Bayesian hierarchical spatial areal unit models.
In such models the spatial correlation is modelled by a set of random effects, which are assigned a conditional autoregressive (CAR) prior distribution.
Examples of the models included are the BYM model as well as a recently developed localised spatial smoothing model.
The [glmmBUGS](https://cran.r-project.org/package=glmmBUGS) package is a helpful way of passing out spatial models to WinBUGS.
The [spaMM](https://cran.r-project.org/package=spaMM) package fits spatial GLMMs, using the Matern correlation function as the basic model for spatial random effects.
The [PReMiuM](https://cran.r-project.org/package=PReMiuM) package is for profile regression, which is a Dirichlet process Bayesian clustering model; it provides a spatial CAR term that can be included in the fixed effects (which are global, ie.
non cluster specific, parameters) to account for any spatial correlation in the residuals.
The [spacom](https://cran.r-project.org/package=spacom) package provides tools to construct and exploit spatially weighted context data, and further allows combining the resulting spatially weighted context data with individual-level predictor and outcome variables, for the purposes of multilevel modelling.
The [geospacom](https://cran.r-project.org/package=geospacom) package generates distance matrices from shape files and represents spatially weighted multilevel analysis results.
Spatial survival analysis is provided by the [spatsurv](https://cran.r-project.org/package=spatsurv) - Bayesian inference for parametric proportional hazards spatial survival models - and [spBayesSurv](https://cran.r-project.org/package=spBayesSurv) - Bayesian Modeling and Analysis of Spatially Correlated Survival Data - packages.
The [spselect](https://cran.r-project.org/package=spselect) package provides modelling functions based on forward stepwise regression, incremental forward stagewise regression, least angle regression (LARS), and lasso models for selecting the spatial scale of covariates in regression models.

-   **Spatial regression** : The choice of function for spatial regression will depend on the support available.
If the data are characterised by point support and the spatial process is continuous, geostatistical methods may be used, or functions in the [nlme](https://cran.r-project.org/package=nlme) package.
If the support is areal, and the spatial process is not being treated as continuous, functions provided in the [spdep](https://cran.r-project.org/package=spdep) package may be used.
This package can also be seen as providing spatial econometrics functions, and, as noted above, provides basic functions for building neighbour lists and spatial weights, tests for spatial autocorrelation for areal data like Moran's I, and functions for fitting spatial regression models.
It provides the full range of local indicators of spatial association, such as local Moran's I and diagnostic tools for fitted linear models, including Lagrange Multiplier tests.
Spatial regression models that can be fitted using maximum likelihood include spatial lag models, spatial error models, and spatial Durbin models.
For larger data sets, sparse matrix techniques can be used for maximum likelihood fits, while spatial two stage least squares and generalised method of moments estimators are an alternative.
When using GMM, [sphet](https://cran.r-project.org/package=sphet) can be used to accommodate both autocorrelation and heteroskedasticity.
The [McSpatial](https://cran.r-project.org/package=McSpatial) provides functions for locally weighted regression, semiparametric and conditionally parametric regression, fourier and cubic spline functions, GMM and linearized spatial logit and probit, k-density functions and counterfactuals, nonparametric quantile regression and conditional density functions, Machado-Mata decomposition for quantile regressions, spatial AR model, repeat sales models, and conditionally parametric logit and probit.
The [splm](https://cran.r-project.org/package=splm) package provides methods for fitting spatial panel data by maximum likelihood and GM.
The two small packages [S2sls](https://cran.r-project.org/package=S2sls) and [spanel](https://cran.r-project.org/package=spanel) provide alternative implementations without most of the facilities of [splm](https://cran.r-project.org/package=splm).
The [HSAR](https://cran.r-project.org/package=HSAR) package provides Hierarchical Spatial Autoregressive Models (HSAR), based on a Bayesian Markov Chain Monte Carlo (MCMC) algorithm.
[spatialprobit](https://cran.r-project.org/package=spatialprobit) make possible Bayesian estimation of the spatial autoregressive probit model (SAR probit model).
The [ProbitSpatial](https://cran.r-project.org/package=ProbitSpatial) package provides methods for fitting Binomial spatial probit models to larger data sets; spatial autoregressive (SAR) and spatial error (SEM) probit models are included.
The [starma](https://cran.r-project.org/package=starma) package provides functions to identify, estimate and diagnose a Space-Time AutoRegressive Moving Average (STARMA) model.

-   **Ecological analysis** : There are many packages for analysing ecological and environmental data.
They include [ade4](https://cran.r-project.org/package=ade4) for exploratory and Euclidean methods in the environmental sciences, the adehabitat family of packages for the analysis of habitat selection by animals ([adehabitatHR](https://cran.r-project.org/package=adehabitatHR), [adehabitatHS](https://cran.r-project.org/package=adehabitatHS), [adehabitatLT](https://cran.r-project.org/package=adehabitatLT), and [adehabitatMA](https://cran.r-project.org/package=adehabitatMA)), [pastecs](https://cran.r-project.org/package=pastecs) for the regulation, decomposition and analysis of space-time series, [vegan](https://cran.r-project.org/package=vegan) for ordination methods and other useful functions for community and vegetation ecologists, and many other functions in other contributed packages.
One such is [tripEstimation](https://cran.r-project.org/package=tripEstimation), basing on the classes provided by [trip](https://cran.r-project.org/package=trip).
[ncf](https://cran.r-project.org/package=ncf) has entered CRAN recently, and provides a range of spatial nonparametric covariance functions.
The [spind](https://cran.r-project.org/package=spind) package provides functions for spatial methods based on generalized estimating equations (GEE) and wavelet-revised methods (WRM), functions for scaling by wavelet multiresolution regression (WMRR), conducting multi-model inference, and stepwise model selection.
[rangeMapper](https://cran.r-project.org/package=rangeMapper) is a package to manipulate species range (extent-of-occurrence) maps, mainly tools for easy generation of biodiversity (species richness) or life-history traits maps.
The [siplab](https://cran.r-project.org/package=siplab) package is a platform for experimenting with spatially explicit individual-based vegetation models.
[ModelMap](https://cran.r-project.org/package=ModelMap) builds on other packages to create models using underlying GIS data.
The [SpatialPosition](https://cran.r-project.org/package=SpatialPosition) computes spatial position models: Stewart potentials, Reilly catchment areas, Huff catchment areas.
The [Watersheds](https://cran.r-project.org/package=Watersheds) package provides methods for watersheds aggregation and spatial drainage network analysis.
An off-CRAN package - [Rcitrus](http://www.leg.ufpr.br/Rcitrus/) - is for the spatial analysis of plant disease incidence.
The [ngspatial](https://cran.r-project.org/package=ngspatial) package provides tools for analyzing spatial data, especially non-Gaussian areal data.
It supports the sparse spatial generalized linear mixed model of Hughes and Haran (2013) and the centered autologistic model of Caragea and Kaiser (2009).
The [Environmetrics](Environmetrics.html) Task View contains a much more complete survey of relevant functions and packages.

### CRAN packages:

-   [ade4](https://cran.r-project.org/package=ade4)
-   [adehabitatHR](https://cran.r-project.org/package=adehabitatHR)
-   [adehabitatHS](https://cran.r-project.org/package=adehabitatHS)
-   [adehabitatLT](https://cran.r-project.org/package=adehabitatLT)
-   [adehabitatMA](https://cran.r-project.org/package=adehabitatMA)
-   [ads](https://cran.r-project.org/package=ads)
-   [akima](https://cran.r-project.org/package=akima)
-   [AMOEBA](https://cran.r-project.org/package=AMOEBA)
-   [ash](https://cran.r-project.org/package=ash)
-   [aspace](https://cran.r-project.org/package=aspace)
-   [automap](https://cran.r-project.org/package=automap)
-   [CARBayes](https://cran.r-project.org/package=CARBayes)
-   [cartography](https://cran.r-project.org/package=cartography)
-   [classInt](https://cran.r-project.org/package=classInt) (core)
-   [cleangeo](https://cran.r-project.org/package=cleangeo)
-   [CompRandFld](https://cran.r-project.org/package=CompRandFld)
-   [constrainedKriging](https://cran.r-project.org/package=constrainedKriging)
-   [cshapes](https://cran.r-project.org/package=cshapes)
-   [dbmss](https://cran.r-project.org/package=dbmss)
-   [DCluster](https://cran.r-project.org/package=DCluster) (core)
-   [deldir](https://cran.r-project.org/package=deldir) (core)
-   [diseasemapping](https://cran.r-project.org/package=diseasemapping)
-   [DSpat](https://cran.r-project.org/package=DSpat)
-   [ecespa](https://cran.r-project.org/package=ecespa)
-   [ExceedanceTools](https://cran.r-project.org/package=ExceedanceTools)
-   [fields](https://cran.r-project.org/package=fields)
-   [FieldSim](https://cran.r-project.org/package=FieldSim)
-   [FRK](https://cran.r-project.org/package=FRK)
-   [gdalUtils](https://cran.r-project.org/package=gdalUtils)
-   [gdistance](https://cran.r-project.org/package=gdistance)
-   [gear](https://cran.r-project.org/package=gear)
-   [geoaxe](https://cran.r-project.org/package=geoaxe)
-   [geojson](https://cran.r-project.org/package=geojson)
-   [geojsonio](https://cran.r-project.org/package=geojsonio)
-   [GEOmap](https://cran.r-project.org/package=GEOmap)
-   [geomapdata](https://cran.r-project.org/package=geomapdata)
-   [geonames](https://cran.r-project.org/package=geonames)
-   [geoR](https://cran.r-project.org/package=geoR) (core)
-   [geoRglm](https://cran.r-project.org/package=geoRglm)
-   [georob](https://cran.r-project.org/package=georob)
-   [geospacom](https://cran.r-project.org/package=geospacom)
-   [geosphere](https://cran.r-project.org/package=geosphere)
-   [geospt](https://cran.r-project.org/package=geospt)
-   [geostatsp](https://cran.r-project.org/package=geostatsp)
-   [ggmap](https://cran.r-project.org/package=ggmap)
-   [ggsn](https://cran.r-project.org/package=ggsn)
-   [glmmBUGS](https://cran.r-project.org/package=glmmBUGS)
-   [gmt](https://cran.r-project.org/package=gmt)
-   [Grid2Polygons](https://cran.r-project.org/package=Grid2Polygons)
-   [GriegSmith](https://cran.r-project.org/package=GriegSmith)
-   [gstat](https://cran.r-project.org/package=gstat) (core)
-   [Guerry](https://cran.r-project.org/package=Guerry)
-   [GWmodel](https://cran.r-project.org/package=GWmodel)
-   [gwrr](https://cran.r-project.org/package=gwrr)
-   [HSAR](https://cran.r-project.org/package=HSAR)
-   [igraph](https://cran.r-project.org/package=igraph)
-   [intamap](https://cran.r-project.org/package=intamap)
-   [ipdw](https://cran.r-project.org/package=ipdw)
-   [landsat](https://cran.r-project.org/package=landsat)
-   [latticeDensity](https://cran.r-project.org/package=latticeDensity)
-   [lawn](https://cran.r-project.org/package=lawn)
-   [lctools](https://cran.r-project.org/package=lctools)
-   [leaflet](https://cran.r-project.org/package=leaflet)
-   [leafletR](https://cran.r-project.org/package=leafletR)
-   [magclass](https://cran.r-project.org/package=magclass)
-   [mapdata](https://cran.r-project.org/package=mapdata)
-   [mapmisc](https://cran.r-project.org/package=mapmisc)
-   [mapproj](https://cran.r-project.org/package=mapproj)
-   [maps](https://cran.r-project.org/package=maps)
-   [maptools](https://cran.r-project.org/package=maptools) (core)
-   [mapview](https://cran.r-project.org/package=mapview)
-   [marmap](https://cran.r-project.org/package=marmap)
-   [MBA](https://cran.r-project.org/package=MBA)
-   [McSpatial](https://cran.r-project.org/package=McSpatial)
-   [micromap](https://cran.r-project.org/package=micromap)
-   [ModelMap](https://cran.r-project.org/package=ModelMap)
-   [ncdf4](https://cran.r-project.org/package=ncdf4)
-   [ncf](https://cran.r-project.org/package=ncf)
-   [ngspatial](https://cran.r-project.org/package=ngspatial)
-   [nlme](https://cran.r-project.org/package=nlme)
-   [OasisR](https://cran.r-project.org/package=OasisR)
-   [OpenStreetMap](https://cran.r-project.org/package=OpenStreetMap)
-   [osmar](https://cran.r-project.org/package=osmar)
-   [pastecs](https://cran.r-project.org/package=pastecs)
-   [PBSmapping](https://cran.r-project.org/package=PBSmapping)
-   [PBSmodelling](https://cran.r-project.org/package=PBSmodelling)
-   [plotGoogleMaps](https://cran.r-project.org/package=plotGoogleMaps)
-   [plotKML](https://cran.r-project.org/package=plotKML)
-   [postGIStools](https://cran.r-project.org/package=postGIStools)
-   [PReMiuM](https://cran.r-project.org/package=PReMiuM)
-   [ProbitSpatial](https://cran.r-project.org/package=ProbitSpatial)
-   [quickmapr](https://cran.r-project.org/package=quickmapr)
-   [ramps](https://cran.r-project.org/package=ramps)
-   [RandomFields](https://cran.r-project.org/package=RandomFields) (core)
-   [rangeMapper](https://cran.r-project.org/package=rangeMapper)
-   [RArcInfo](https://cran.r-project.org/package=RArcInfo)
-   [raster](https://cran.r-project.org/package=raster) (core)
-   [rasterVis](https://cran.r-project.org/package=rasterVis)
-   [RColorBrewer](https://cran.r-project.org/package=RColorBrewer) (core)
-   [recmap](https://cran.r-project.org/package=recmap)
-   [regress](https://cran.r-project.org/package=regress)
-   [rgbif](https://cran.r-project.org/package=rgbif)
-   [rgdal](https://cran.r-project.org/package=rgdal) (core)
-   [rgeos](https://cran.r-project.org/package=rgeos) (core)
-   [RgoogleMaps](https://cran.r-project.org/package=RgoogleMaps)
-   [rgrass7](https://cran.r-project.org/package=rgrass7)
-   [RNetCDF](https://cran.r-project.org/package=RNetCDF)
-   [rpostgis](https://cran.r-project.org/package=rpostgis)
-   [RPyGeo](https://cran.r-project.org/package=RPyGeo)
-   [RQGIS](https://cran.r-project.org/package=RQGIS)
-   [RSAGA](https://cran.r-project.org/package=RSAGA)
-   [RSurvey](https://cran.r-project.org/package=RSurvey)
-   [rtop](https://cran.r-project.org/package=rtop)
-   [rworldmap](https://cran.r-project.org/package=rworldmap)
-   [rworldxtra](https://cran.r-project.org/package=rworldxtra)
-   [S2sls](https://cran.r-project.org/package=S2sls)
-   [seg](https://cran.r-project.org/package=seg)
-   [sf](https://cran.r-project.org/package=sf) (core)
-   [sgeostat](https://cran.r-project.org/package=sgeostat)
-   [shapefiles](https://cran.r-project.org/package=shapefiles)
-   [shp2graph](https://cran.r-project.org/package=shp2graph)
-   [siplab](https://cran.r-project.org/package=siplab)
-   [smacpod](https://cran.r-project.org/package=smacpod)
-   [smerc](https://cran.r-project.org/package=smerc)
-   [sp](https://cran.r-project.org/package=sp) (core)
-   [spacetime](https://cran.r-project.org/package=spacetime) (core)
-   [spacom](https://cran.r-project.org/package=spacom)
-   [spaMM](https://cran.r-project.org/package=spaMM)
-   [spanel](https://cran.r-project.org/package=spanel)
-   [sparr](https://cran.r-project.org/package=sparr)
-   [spatgraphs](https://cran.r-project.org/package=spatgraphs)
-   [spatial](https://cran.r-project.org/package=spatial)
-   [spatial.tools](https://cran.r-project.org/package=spatial.tools)
-   [spatialCovariance](https://cran.r-project.org/package=spatialCovariance)
-   [SpatialEpi](https://cran.r-project.org/package=SpatialEpi)
-   [SpatialExtremes](https://cran.r-project.org/package=SpatialExtremes)
-   [SpatialPosition](https://cran.r-project.org/package=SpatialPosition)
-   [spatialprobit](https://cran.r-project.org/package=spatialprobit)
-   [spatialsegregation](https://cran.r-project.org/package=spatialsegregation)
-   [SpatialTools](https://cran.r-project.org/package=SpatialTools)
-   [spatstat](https://cran.r-project.org/package=spatstat) (core)
-   [spatsurv](https://cran.r-project.org/package=spatsurv)
-   [spBayes](https://cran.r-project.org/package=spBayes)
-   [spBayesSurv](https://cran.r-project.org/package=spBayesSurv)
-   [spcosa](https://cran.r-project.org/package=spcosa)
-   [spdep](https://cran.r-project.org/package=spdep) (core)
-   [sperrorest](https://cran.r-project.org/package=sperrorest)
-   [spgrass6](https://cran.r-project.org/package=spgrass6)
-   [spgwr](https://cran.r-project.org/package=spgwr)
-   [sphet](https://cran.r-project.org/package=sphet)
-   [spind](https://cran.r-project.org/package=spind)
-   [splancs](https://cran.r-project.org/package=splancs) (core)
-   [splm](https://cran.r-project.org/package=splm)
-   [spm](https://cran.r-project.org/package=spm)
-   [spmoran](https://cran.r-project.org/package=spmoran)
-   [spsann](https://cran.r-project.org/package=spsann)
-   [spselect](https://cran.r-project.org/package=spselect)
-   [spsurvey](https://cran.r-project.org/package=spsurvey)
-   [spTimer](https://cran.r-project.org/package=spTimer)
-   [SSN](https://cran.r-project.org/package=SSN)
-   [starma](https://cran.r-project.org/package=starma)
-   [statebins](https://cran.r-project.org/package=statebins)
-   [Stem](https://cran.r-project.org/package=Stem)
-   [stplanr](https://cran.r-project.org/package=stplanr)
-   [taRifx](https://cran.r-project.org/package=taRifx)
-   [tgp](https://cran.r-project.org/package=tgp)
-   [tmap](https://cran.r-project.org/package=tmap)
-   [trip](https://cran.r-project.org/package=trip)
-   [tripack](https://cran.r-project.org/package=tripack)
-   [tripEstimation](https://cran.r-project.org/package=tripEstimation)
-   [UScensus2000cdp](https://cran.r-project.org/package=UScensus2000cdp)
-   [UScensus2000tract](https://cran.r-project.org/package=UScensus2000tract)
-   [vardiag](https://cran.r-project.org/package=vardiag)
-   [vec2dtransf](https://cran.r-project.org/package=vec2dtransf)
-   [vegan](https://cran.r-project.org/package=vegan)
-   [Watersheds](https://cran.r-project.org/package=Watersheds)
-   [wkb](https://cran.r-project.org/package=wkb)

### Related links:

-   CRAN Task View: [Environmetrics](Environmetrics.html)
-   [Rgeo: Spatial Statistics with R](http://geodacenter.asu.edu/projects/rsp)
-   [R-SIG-Geo mailing list](https://stat.ethz.ch/mailman/listinfo/R-SIG-Geo/)
