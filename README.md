CRAN Task View: Mapping tools and services
------------------------------------------

  ----------------- --------------------------------------------------------------------------------------
  **Maintainer:**   Jeff Hollister, Karthik Ram, Hadley Wickham, Scott Chamberlain, Ramnath Vaidyanathan
  **Contact:**      hollister.jeff at epa.gov
  **Version:**      2015-02-07
  ----------------- --------------------------------------------------------------------------------------

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
View](http://cran.r-project.org/web/views/Spatial.html).

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
    plots, and uses ggplot2 plotting framework. Source not available.
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
    (via [zoom](http://cran.r-project.org/web/packages/zoom/index.html))
    as well as identifying features. [Source on
    Github](https://github.com/jhollist/quickmapr)
-   [Rgooglemaps](http://cran.r-project.org/web/packages/Rgooglemaps/index.html):
    Query Google static maps, and use the map as a background image to
    overlay plots within R. [Source on
    Github](https://github.com/markusloecher/RgoogleMaps)
-   [rMaps](https://github.com/ramnathv/rMaps): A general purpose
    wrapper around man Javascript mapping libraries, including
    [Leaflet](http://leafletjs.com/),
    [Datamaps](http://datamaps.github.io/), and
    [Crosslet](http://sztanko.github.io/crosslet/). [Source on
    Github](https://github.com/ramnathv/rMaps)
-   [sp](http://cran.r-project.org/web/packages/sp/index.html): Core
    package in R for doing spatial data manipulation and analysis.
    Plotting capabilities in
    [sp](http://cran.r-project.org/web/packages/sp/index.html) based on
    [lattice](http://cran.r-project.org/web/packages/lattice/index.html).
    [Source on
    R-Forge](https://r-forge.r-project.org/projects/rspatial/)

### Projecting Data

-   Differences between geographic (i.e. GPS, DMS, DD, Lat-Long) and
    projected data
-   [mapproj](http://cran.r-project.org/web/packages/mapproj/index.html)
-   [PBSmapping](http://cran.r-project.org/web/packages/PBSmapping/index.html)
-   [rgdal](http://cran.r-project.org/web/packages/rgdal/index.html)
    and/or
    [sp](http://cran.r-project.org/web/packages/sp/index.html):spTransform()

### Geocoding

-   [geocodeHERE](http://cran.r-project.org/web/packages/geocodeHERE/index.html):
    Client for Nokia's [HERE geocoding
    API](https://developer.here.com/geocoder). [Source on
    GitHub](https://github.com/corynissen/geocodeHERE/)
-   [ggmap](http://cran.r-project.org/web/packages/ggmap/index.html):
    The function `geocode` in
    [ggmap](http://cran.r-project.org/web/packages/ggmap/index.html)
    uses the [Google Geocoding
    API](https://developers.google.com/maps/documentation/geocoding/?csw=1).
    [Source on Github](https://github.com/)
-   [rydn](https://github.com/trestletech/rydn): Client for the Yahoo!
    Developers Network [BOSS PlaceFinder
    API](https://developer.yahoo.com/boss/). [Source on
    Github](https://github.com/trestletech/rydn)

### Sources of Map Data

-   [maps](http://cran.r-project.org/web/packages/maps/index.html)
-   [rworldmap](http://cran.r-project.org/web/packages/rworldmap/index.html)
-   [osmar](http://cran.r-project.org/web/packages/osmar/index.html)
-   [UScensus2010](http://cran.r-project.org/web/packages/UScensus2010/index.html)
-   [geomapdata](http://cran.r-project.org/web/packages/geomapdata/index.html)

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
-   [ggmap](http://cran.r-project.org/web/packages/ggmap/index.html)
-   [lattice](http://cran.r-project.org/web/packages/lattice/index.html)
-   [leafletR](http://cran.r-project.org/web/packages/leafletR/index.html)
-   [mapproj](http://cran.r-project.org/web/packages/mapproj/index.html)
-   [maps](http://cran.r-project.org/web/packages/maps/index.html)
-   [maptools](http://cran.r-project.org/web/packages/maptools/index.html)
-   [micromap](http://cran.r-project.org/web/packages/micromap/index.html)
-   [OpenStreetMap](http://cran.r-project.org/web/packages/OpenStreetMap/index.html)
-   [osmar](http://cran.r-project.org/web/packages/osmar/index.html)
-   [PBSmapping](http://cran.r-project.org/web/packages/PBSmapping/index.html)
-   [plotGoogleMaps](http://cran.r-project.org/web/packages/plotGoogleMaps/index.html)
-   [raster](http://cran.r-project.org/web/packages/raster/index.html)
-   [rgdal](http://cran.r-project.org/web/packages/rgdal/index.html)
-   [Rgooglemaps](http://cran.r-project.org/web/packages/Rgooglemaps/index.html)
-   [rworldmap](http://cran.r-project.org/web/packages/rworldmap/index.html)
-   [sp](http://cran.r-project.org/web/packages/sp/index.html) (core)
-   [UScensus2010](http://cran.r-project.org/web/packages/UScensus2010/index.html)
-   [zoom](http://cran.r-project.org/web/packages/zoom/index.html)

### Related links:

-   [GitHub package: rMaps](https://github.com/ramnathv/rMaps)
-   [GitHub package: cartodb](https://github.com/Vizzuality/cartodb-r)
-   [GitHub package: rydn](https://github.com/trestletech/rydn)

