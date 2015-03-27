CRAN Task View: Mapping tools and services
------------------------------------------

  ----------------- ------------------------------------------------------------------------------------------
  **Maintainer:**   Jeff Hollister, Scott Chamberlain, Karthik Ram, Hadley Wickham, Ben Marwick, Cory Nissen
  **Contact:**      hollister.jeff at epa.gov
  **Version:**      2015-02-27
  ----------------- ------------------------------------------------------------------------------------------

This task view contains information about mapping and visualizing
spatial data in R. The base version of R does not ship with many tools
for mapping spatial data. Thankfully, there are an increasingly large
number of tools, both in R and those utilizing javascript libraries, for
doing so. A list of available packages and functions is presented below,
grouped by the type of activity. If you have any comments or suggestions
for additions or improvements for this taskview, go to Github and
[submit an issue](https://github.com/ropensci/maptools/issues), or [make
some changes](https://github.com/ropensci/maptools/CONTRIBUTING.md) and
[submit a pull request](https://github.com/ropensci/maptools/pulls). If
you can't contribute on Github, [send Jeff an
email](mailto:hollister.jeff@epa.gov). If you have an issue with one of
the packages discussed below, please contact the maintainer of that
package. This task view is focused on mapping spatial data. For more on
working with and analyzing spatial data in R, see the [Spatial Task
View](Spatial%20Task%20View.html).

Mapping tools in R
------------------

### Visualization

-   [cartodb](https://github.com/Vizzuality/cartodb-r): CartoDB R
    client. Not on CRAN, and hasn't been active for a while. [Source on
    Github](https://github.com/Vizzuality/cartodb-r)
-   [cartographer](https://github.com/lmullen/cartographer): Interactive
    maps in R using
    [d3-carto-map](https://github.com/emeeks/d3-carto-map). [Source on
    Github](https://github.com/lmullen/cartographer)
-   [ggmap](http://cran.r-project.org/web/packages/ggmap/index.html):
    Visualization of spatial data and models on top of Google Maps,
    OpenStreetMaps, Stamen Maps, or CloudMade Maps using ggplot2.
    [Source on Github](https://github.com/dkahle/ggmap)
-   [leafletR](http://cran.r-project.org/web/packages/leafletR/index.html):
    Client for the JavaScript library Leaflet.js. Basic mapping
    functionality to combine vector data and online map tiles from
    different sources. [Source on
    Github](https://github.com/chgrl/leafletR)
-   [micromap](http://cran.r-project.org/web/packages/micromap/index.html):
    This group of functions simplifies the creation of linked micromap
    plots, and uses ggplot2 plotting framework. [Source on
    Github.](https://github.com/USEPA/R-micromap-package-development)
-   [OpenStreetMap](http://cran.r-project.org/web/packages/OpenStreetMap/index.html):
    An R client for the Open Stree Maps API. [Source on
    Github](https://github.com/)
-   [plotGoogleMaps](http://cran.r-project.org/web/packages/plotGoogleMaps/index.html):
    This package provides a interactive plot device for handling the
    geographic data for web browsers. It is designed for the automatic
    creation of web maps as a combination of users' data and Google Maps
    layers.
-   [quickmpar](https://github.com/jhollist/quickmapr): Quick
    visualization of
    [sp](http://cran.r-project.org/web/packages/sp/index.html) and
    [raster](http://cran.r-project.org/web/packages/raster/index.html)
    objects. Provides basic interactivity including zooming and panning
    as well as identifying features. [Source on
    Github](https://github.com/jhollist/quickmapr)
-   [rasterVis](http://cran.r-project.org/web/packages/rasterVis/index.html):
    Package for enchanced visualization of raster data. [Source on
    Github](https://github.com/oscarperpinan/rastervis/)
-   [Rgooglemaps](http://cran.r-project.org/web/packages/Rgooglemaps/index.html):
    Query Google static maps, and use the map as a background image to
    overlay plots within R. [Source on
    Github](https://github.com/markusloecher/RgoogleMaps)
-   [rMaps](https://github.com/ramnathv/rMaps): A general purpose
    wrapper around main Javascript mapping libraries, including
    [Leaflet](http://leafletjs.com/),
    [Datamaps](http://datamaps.github.io/), and
    [Crosslet](http://sztanko.github.io/crosslet/). [Source on
    Github](https://github.com/ramnathv/rMaps)
-   [sp](http://cran.r-project.org/web/packages/sp/index.html): Core
    package in R for doing spatial data manipulation and analysis.
    Plotting capabilities in
    [sp](http://cran.r-project.org/web/packages/sp/index.html) are
    provdied through some default plot methods. More advanced plotting
    based on
    [lattice](http://cran.r-project.org/web/packages/lattice/index.html).
    [Source on
    R-Forge](https://r-forge.r-project.org/projects/rspatial/)

### Projecting Data

Coordinates for spatial data can come in many different flavors with
different units, datums, projections, and more. Many of the tools will
visualize your data regardless of the native coordinate reference
system; however, most (all?) of the javascript libraries assume some
flavor of lattitude-longitude, thus if your data are projected they need
to be transformed back to geographic coordinates prior to mapping. For
most mapping and visulaization efforts unprojected data (often displayed
in Web Mercator/EPSG::3857) is fine; however, if accuarate area, length,
or distance measurements are required through interacting with the map,
then projections need to be considered. A discussion of projections and
coordinate systems is beyond the scope of this task view. To learn more
a good starting place is [NCEAS' Overview of Coordinate Reference
Systems in
R](https://www.nceas.ucsb.edu/\~frazier/RSpatialGuides/OverviewCoordinateReferenceSystems.pdf)

Once you know that you need to transform you data there are several
options:

-   [sp](http://cran.r-project.org/web/packages/sp/index.html): The
    function `spTransform` (and methods in
    [rgdal](http://cran.r-project.org/web/packages/rgdal/index.html)) is
    the workhorse function for spatial transformations of vector data
    and it uses [PROJ.4](http://trac.osgeo.org/proj/) arguments to
    specify the transformations. Accepted inputs are provided by the
    spTransform methods in
    [rgdal](http://cran.r-project.org/web/packages/rgdal/index.html).
    [Source for `sp` on
    R-Forge](https://r-forge.r-project.org/projects/rspatial/). [Source
    for `rgdal` on
    R-Forge](https://r-forge.r-project.org/projects/rgdal/).
-   [mapproj](http://cran.r-project.org/web/packages/mapproj/index.html):
    This package provides a fucntion to convert two vectors representing
    longitude (x) and lattitude (y) to projected coordinates.
-   [PBSmapping](http://cran.r-project.org/web/packages/PBSmapping/index.html):
    The function `convUL` will transform coordinates between Universal
    Transverse Mercator (UTM) and longitude-latitude. A data frame with
    a `projection` attribute is required input. [Source on Google
    Code](http://code.google.com/p/pbs-software/)

### Geocoding

Geocoding is the process of converting address or place name information
into geographic coordinates.

-   [geocodeHERE](http://cran.r-project.org/web/packages/geocodeHERE/index.html):
    Client for Nokia's [HERE geocoding
    API](https://developer.here.com/geocoder). [Source on
    GitHub](https://github.com/corynissen/geocodeHERE/)
-   [ggmap](http://cran.r-project.org/web/packages/ggmap/index.html):
    The function `geocode` in
    [ggmap](http://cran.r-project.org/web/packages/ggmap/index.html)
    uses the [Google Geocoding
    API](https://developers.google.com/maps/documentation/geocoding/?csw=1).
    [Source on Github](https://github.com/dkahle/ggmap)
-   [rydn](https://github.com/trestletech/rydn): Client for the Yahoo!
    Developers Network [BOSS PlaceFinder
    API](https://developer.yahoo.com/boss/). [Source on
    Github](https://github.com/trestletech/rydn)

### Sources of Map Data

There are \*many\* possible sources of data to use as base layers, so
this list will most certainly be incomplete. If you have any suggest
additions, please use the [Github
Issues](https://github.com/ropensci/maptools/issues).

-   [maps](http://cran.r-project.org/web/packages/maps/index.html):
    Collection of coarse scaled for the US, some European countries, and
    a world map. Stored as \`map\` objects and various other geographic
    datasets. Location information in decimal degrees. Needs coversion
    to work with visualization from
    [sp](http://cran.r-project.org/web/packages/sp/index.html),
    [ggmap](http://cran.r-project.org/web/packages/ggmap/index.html),
    etc. Code for projections and additional maps in packages
    [mapproj](http://cran.r-project.org/web/packages/mapproj/index.html)
    [mapdata](http://cran.r-project.org/web/packages/mapdata/index.html).
-   [rworldmap](http://cran.r-project.org/web/packages/rworldmap/index.html):
    Set of functions to create country based world maps. Allows for
    joining of user specified data and can display chloropleth, gridded,
    bubble plot, bar charts, or pie charts. Data stored as \`sp\`
    objects. [Source on Google
    Code.](https://code.google.com/p/rworld/downloads/list)
-   [osmar](http://cran.r-project.org/web/packages/osmar/index.html):
    Package for interacting with the Open Street Map API in R. Functions
    for converting an open street map object into
    [sp](http://cran.r-project.org/web/packages/sp/index.html) or
    [igraph](http://cran.r-project.org/web/packages/igraph/index.html)
    objects. [Source on
    R-Forge.](https://r-forge.r-project.org/projects/osmar/)
-   [UScensus2010](http://cran.r-project.org/web/packages/UScensus2010/index.html):
-   [geomapdata](http://cran.r-project.org/web/packages/geomapdata/index.html):
-   [geonames](http://cran.r-project.org/web/packages/geonames/index.html):
    functions for working with [geonames](http://www.geonames.org/), a
    geographical database that covers all countries and contains over
    eight million placenames
-   [USAboundaries](http://cran.r-project.org/web/packages/USAboundaries/index.html):
    provides spatial objects with the boundaries of states or counties
    in the United States of America from 1629 to 2000. It provides data
    from the Atlas of Historical County Boundaries.

### Map Data I/O

-   shapefiles:
    [maptools](http://cran.r-project.org/web/packages/maptools/index.html),
    [rgdal](http://cran.r-project.org/web/packages/rgdal/index.html)
-   topo- and geo- json:
    [rgdal](http://cran.r-project.org/web/packages/rgdal/index.html),
    geojsonio
-   kml
-   raster:
    [raster](http://cran.r-project.org/web/packages/raster/index.html)

### CRAN packages:

-   [geocodeHERE](http://cran.r-project.org/web/packages/geocodeHERE/index.html)
-   [geomapdata](http://cran.r-project.org/web/packages/geomapdata/index.html)
-   [geonames](http://cran.r-project.org/web/packages/geonames/index.html)
-   [ggmap](http://cran.r-project.org/web/packages/ggmap/index.html)
-   [igraph](http://cran.r-project.org/web/packages/igraph/index.html)
-   [lattice](http://cran.r-project.org/web/packages/lattice/index.html)
-   [leafletR](http://cran.r-project.org/web/packages/leafletR/index.html)
-   [mapdata](http://cran.r-project.org/web/packages/mapdata/index.html)
-   [mapproj](http://cran.r-project.org/web/packages/mapproj/index.html)
-   [maps](http://cran.r-project.org/web/packages/maps/index.html)
-   [maptools](http://cran.r-project.org/web/packages/maptools/index.html)
-   [micromap](http://cran.r-project.org/web/packages/micromap/index.html)
-   [OpenStreetMap](http://cran.r-project.org/web/packages/OpenStreetMap/index.html)
-   [osmar](http://cran.r-project.org/web/packages/osmar/index.html)
-   [PBSmapping](http://cran.r-project.org/web/packages/PBSmapping/index.html)
-   [plotGoogleMaps](http://cran.r-project.org/web/packages/plotGoogleMaps/index.html)
-   [raster](http://cran.r-project.org/web/packages/raster/index.html)
-   [rasterVis](http://cran.r-project.org/web/packages/rasterVis/index.html)
-   [rgdal](http://cran.r-project.org/web/packages/rgdal/index.html)
-   [Rgooglemaps](http://cran.r-project.org/web/packages/Rgooglemaps/index.html)
-   [rworldmap](http://cran.r-project.org/web/packages/rworldmap/index.html)
-   [sp](http://cran.r-project.org/web/packages/sp/index.html) (core)
-   [USAboundaries](http://cran.r-project.org/web/packages/USAboundaries/index.html)
-   [UScensus2010](http://cran.r-project.org/web/packages/UScensus2010/index.html)

### Related links:

-   [GitHub package: rMaps](https://github.com/ramnathv/rMaps)
-   [GitHub package: cartodb](https://github.com/Vizzuality/cartodb-r)
-   [GitHub package: rydn](https://github.com/trestletech/rydn)

