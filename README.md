CRAN Task View: Mapping tools and services
------------------------------------------

  ------------------------------------ ------------------------------------
  **Maintainer:**                      **Contact:**
  Jeff Hollister, Scott Chamberlain,   hollister.jeff at epa.gov
  Karthik Ram, Hadley Wickham, Ben     
  Marwick, Cory Nissen                 
  ------------------------------------ ------------------------------------

This task view contains information about mapping and visualizing
spatial data in R. The base version of R does not ship with many tools
for mapping spatial data. Thankfully, there are an increasingly large
number of tools for doing so, both with just R or javascript libraries.
A list of available packages and functions is presented below, grouped
by the type of activity. If you have any comments or suggestions for
additions or improvements for this taskview, go to Github and [submit an
issue](https://github.com/ropensci/maptools/issues), or [make some
changes](https://github.com/ropensci/maptools/CONTRIBUTING.md) and
[submit a pull request](https://github.com/ropensci/maptools/pulls). If
you can't contribute on Github, [send Jeff an
email](mailto:hollister.jeff@epa.gov). If you have an issue with one of
the packages discussed below, please contact the maintainer of that
package. This task view is focused on mapping spatial data and less so
on the foundations of working with spatial data in R. That material is
covered in detail in the [Spatial Task
View](Spatial%20Task%20View.html). There is some overlap between the two
task views, but an effort has been made to reduce redundancy so that
these task views compliment one another.

Mapping tools in R
------------------

### Visualization

-   [cartodb](https://github.com/Vizzuality/cartodb-r): CartoDB R
    client. Not on CRAN, and hasn't been active for a while. [Source on
    Github](https://github.com/Vizzuality/cartodb-r)
-   [cartographer](https://github.com/ropensci/cartographer):
    Interactive maps in R using
    [d3-carto-map](https://github.com/emeeks/d3-carto-map). [Source on
    Github](https://github.com/ropensci/cartographer)
-   [ggmap](http://cran.r-project.org/web/packages/ggmap/index.html):
    Visualization of spatial data and models on top of Google Maps,
    OpenStreetMaps, Stamen Maps, or CloudMade Maps using ggplot2.
    [Source on Github](https://github.com/dkahle/ggmap)
-   [leaflet](http://cran.r-project.org/web/packages/leaflet/index.html):
    Client for the JavaScript library Leaflet.js. Uses
    [htmlwidgets](http://cran.r-project.org/web/packages/htmlwidgets/index.html)
    to provide structure for output. Integrated with R Console, RStudio,
    and R Markdown v 2. Can include interactive maps with markdown
    documents as well as with
    [shiny](http://cran.r-project.org/web/packages/shiny/index.html)
    apps. [Source on Github](https://github.com/rstudio/leaflet)
-   [leafletR](http://cran.r-project.org/web/packages/leafletR/index.html):
    Another client for the JavaScript library Leaflet.js. Basic mapping
    functionality to combine vector data and online map tiles from
    different sources. [Source on
    Github](https://github.com/chgrl/leafletR)
-   [mapview](http://cran.r-project.org/web/packages/mapview/index.html):
    This package provides wrappers to the
    [leaflet](http://cran.r-project.org/web/packages/leaflet/index.html)
    package that simplifies the creation of maps. Stated purpose of the
    package is to facilitate interactive viewing of spatial data in R.
    [Source on
    Github.](https://github.com/environmentalinformatics-marburg/mapview)
-   [micromap](http://cran.r-project.org/web/packages/micromap/index.html):
    This group of functions simplifies the creation of linked micromap
    plots, and uses ggplot2 plotting framework. [Source on
    Github.](https://github.com/USEPA/R-micromap-package-development)
-   [OpenStreetMap](http://cran.r-project.org/web/packages/OpenStreetMap/index.html):
    An R client for fetching raster images via the Open Street Maps API.
-   [plotGoogleMaps](http://cran.r-project.org/web/packages/plotGoogleMaps/index.html):
    This package provides a interactive plot device for handling the
    geographic data for web browsers. It is designed for the automatic
    creation of web maps as a combination of users' data and Google Maps
    layers.
-   [quickmpar](http://cran.r-project.org/web/packages/quickmpar/index.html):
    Quick visualization of
    [sp](http://cran.r-project.org/web/packages/sp/index.html) and
    [raster](http://cran.r-project.org/web/packages/raster/index.html)
    objects. Provides basic interactivity including zooming and panning
    as well as identifying features. [Source on
    Github](https://github.com/jhollist/quickmapr)
-   [rasterVis](http://cran.r-project.org/web/packages/rasterVis/index.html):
    Package for enhanced visualization of raster data. [Source on
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
    spatial package in R with basic spatial data manipulation methods.
    Most spatial analysis packages reuse the classes and methods
    provided by
    [sp](http://cran.r-project.org/whttp://cran.r-project.org/web/packages/sp/index.html).
    Plotting capability in
    [sp](http://cran.r-project.org/whttp://cran.r-project.org/web/packages/sp/index.html)
    is provided through plot methods. More advanced plotting based on
    [lattice](http://cran.r-project.org/web/packages/lattice/index.html).
    [Source on GitHub](https://github.com/edzer/sp/)
-   [tmap](http://cran.r-project.org/web/packages/tmap/index.html):
    Package provides an approach to build thematic maps (e.g.
    chloropleth or bubble maps). Utilizes a grammar of graphics syntax.
    [Source on GitHub](https://github.com/mtennekes/tmap)

### Projecting Data

Coordinates for spatial data can come in many different flavors with
different units, datum, projections, and more. Many of the tools will
visualize your data regardless of the native coordinate reference
system; however, most (all?) of the javascript libraries assume some
flavor of latitude-longitude, thus if your data are projected they need
to be transformed back to geographic coordinates prior to mapping. For
most mapping and visualization efforts unprojected data (often displayed
in Web Mercator/EPSG::3857) is fine; however, if accurate area, length,
or distance measurements are required through interacting with the map,
then projections need to be considered. A discussion of projections and
coordinate systems is beyond the scope of this task view. To learn more
a good starting place is [NCEAS' Overview of Coordinate Reference
Systems in
R](https://www.nceas.ucsb.edu/\~frazier/RSpatialGuides/OverviewCoordinateReferenceSystems.pdf).
This more general discussion of projection from the
[USGS](http://egsc.usgs.gov/isb//pubs/MapProjections/projections.html)
is also good.

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
    [Source for `sp` on GitHub](https://github.com/edzer/sp/). [Source
    for `rgdal` on
    R-Forge](https://r-forge.r-project.org/projects/rgdal/).
-   [mapproj](http://cran.r-project.org/web/packages/mapproj/index.html):
    This package provides a function to convert two vectors representing
    longitude (x) and latitude (y) to projected coordinates.
-   [PBSmapping](http://cran.r-project.org/web/packages/PBSmapping/index.html):
    The function `convUL` will transform coordinates between Universal
    Transverse Mercator (UTM) and longitude-latitude. A data frame with
    a `projection` attribute is required input. [Source on Google
    Code](http://code.google.com/p/pbs-software/)

### Geocoding

Geocoding is the process of converting address or place name information
into geographic coordinates. Most of these have somewhat restricted
Terms of Service(TOS). Be sure to read those carefully prior to use.
Links for the TOS are provided.

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

### Map Data

There are \*many\* possible sources and formats of data to use as base
layers, so this list will most certainly be incomplete. Details for
reading and writing most types of spatial data are already included in
the [Analysis of Spatial Data Task
View](Analysis%20of%20Spatial%20Data%20Task%20View.html), thus this list
will focus on additional sources or features not discussed in that task
view.

-   [geojsonio](http://cran.r-project.org/web/packages/geojsonio/index.html):
    Provides utility for working with geojson data in R. Includes
    functions to convert sp objects, lists, and character to geojson
    format.
-   [geonames](http://cran.r-project.org/web/packages/geonames/index.html):
    functions for working with [geonames](http://www.geonames.org/), a
    geographical database that covers all countries and contains over
    eight million place names
-   [maps](http://cran.r-project.org/web/packages/maps/index.html):
    Collection of coarse scaled for the US, some European countries, and
    a world map. Stored as \`map\` objects and various other geographic
    datasets. Location information in decimal degrees. Needs conversion
    to work with visualization from
    [sp](http://cran.r-project.org/web/packages/sp/index.html),
    [ggmap](http://cran.r-project.org/web/packages/ggmap/index.html),
    etc. Code for projections and additional maps in packages
    [mapproj](http://cran.r-project.org/web/packages/mapproj/index.html)
    [mapdata](http://cran.r-project.org/web/packages/mapdata/index.html).
-   [openadds](https://github.com/sckott/openadds): An R client for
    [Openaddresses](http://openaddresses.io). The Openaddresses data
    comes in a variety of formats and this package provides common
    interface to simplify working with it in R. [Source on
    Github](https://github.com/sckott/openadds)
-   [osmar](http://cran.r-project.org/web/packages/osmar/index.html):
    Package for interacting with the Open Street Map API in R. Functions
    for converting an open street map object into
    [sp](http://cran.r-project.org/web/packages/sp/index.html) or
    [igraph](http://cran.r-project.org/web/packages/igraph/index.html)
    objects. [Source on
    R-Forge.](https://r-forge.r-project.org/projects/osmar/)
-   [prism](https://github.com/ropensci/prism): Accesses climate data
    from [PRSIM](http://www.prism.oregonstate.edu/). Also provides some
    basic plotting and mapping functions.
-   [rworldmap](http://cran.r-project.org/web/packages/rworldmap/index.html):
    Set of functions to create country based world maps. Allows for
    joining of user specified data and can display chloropleth, gridded,
    bubble plot, bar charts, or pie charts. Data stored as \`sp\`
    objects. [Source on Google
    Code.](https://code.google.com/p/rworld/downloads/list)
-   [tigris](https://github.com/walkerke/tigris): Access US Census TIGER
    shapefiles directly in R. This package is currently in active
    development.
-   [USAboundaries](http://cran.r-project.org/web/packages/USAboundaries/index.html):
    provides spatial objects with the boundaries of states or counties
    in the United States of America from 1629 to 2000. It provides data
    from the Atlas of Historical County Boundaries.
-   [UScensus2010](http://cran.r-project.org/web/packages/UScensus2010/index.html):
    Functions to facilitate accessing data from the 2010 US Census using
    a suite of packages. Includes spatial data for census geographies
    (e.g. tracts, blocks, block groups, etc.). This packages is the
    third in a series of related package suites:
    [UScensus1990blkgrp](http://cran.r-project.org/web/packages/UScensus1990blkgrp/index.html)
    and
    [UScensus2000](http://cran.r-project.org/web/packages/UScensus2000/index.html).

### CRAN packages:

-   [geocodeHERE](http://cran.r-project.org/web/packages/geocodeHERE/index.html)
-   [geojsonio](http://cran.r-project.org/web/packages/geojsonio/index.html)
-   [geonames](http://cran.r-project.org/web/packages/geonames/index.html)
-   [ggmap](http://cran.r-project.org/web/packages/ggmap/index.html)
-   [htmlwidgets](http://cran.r-project.org/web/packages/htmlwidgets/index.html)
-   [igraph](http://cran.r-project.org/web/packages/igraph/index.html)
-   [lattice](http://cran.r-project.org/web/packages/lattice/index.html)
-   [leaflet](http://cran.r-project.org/web/packages/leaflet/index.html)
-   [leafletR](http://cran.r-project.org/web/packages/leafletR/index.html)
-   [mapdata](http://cran.r-project.org/web/packages/mapdata/index.html)
-   [mapproj](http://cran.r-project.org/web/packages/mapproj/index.html)
-   [maps](http://cran.r-project.org/web/packages/maps/index.html)
-   [mapview](http://cran.r-project.org/web/packages/mapview/index.html)
-   [micromap](http://cran.r-project.org/web/packages/micromap/index.html)
-   [OpenStreetMap](http://cran.r-project.org/web/packages/OpenStreetMap/index.html)
-   [osmar](http://cran.r-project.org/web/packages/osmar/index.html)
-   [PBSmapping](http://cran.r-project.org/web/packages/PBSmapping/index.html)
-   [plotGoogleMaps](http://cran.r-project.org/web/packages/plotGoogleMaps/index.html)
-   [quickmpar](http://cran.r-project.org/web/packages/quickmpar/index.html)
-   [raster](http://cran.r-project.org/web/packages/raster/index.html)
-   [rasterVis](http://cran.r-project.org/web/packages/rasterVis/index.html)
-   [rgdal](http://cran.r-project.org/web/packages/rgdal/index.html)
-   [Rgooglemaps](http://cran.r-project.org/web/packages/Rgooglemaps/index.html)
-   [rworldmap](http://cran.r-project.org/web/packages/rworldmap/index.html)
-   [shiny](http://cran.r-project.org/web/packages/shiny/index.html)
-   [sp](http://cran.r-project.org/web/packages/sp/index.html) (core)
-   [tmap](http://cran.r-project.org/web/packages/tmap/index.html)
-   [USAboundaries](http://cran.r-project.org/web/packages/USAboundaries/index.html)
-   [UScensus1990blkgrp](http://cran.r-project.org/web/packages/UScensus1990blkgrp/index.html)
-   [UScensus2000](http://cran.r-project.org/web/packages/UScensus2000/index.html)
-   [UScensus2010](http://cran.r-project.org/web/packages/UScensus2010/index.html)

### Related links:

-   [Analysis of Spatial Data Task
    View](http://cran.r-project.org/web/views/Spatial.html)

