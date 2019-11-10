
What is the order?

User story - traditional WMS compared with in the browser?


Create user story:

    View raster data on a map?
    Look at raw values
    Change style / minmax values


Go through previous foss4g notes?

If only loading RGB - or simple style

    Client-side computation - uncompress, render pixels...
        Only simple computations
    WMS is service oriented - these packages are for client-side use (can be run with Node.js but Python libraries would be better!)
    WMS supports more formats...
        I have turned 100 NetCDFs (15GB) into 400,000 geotiffs!!!
            This is only 8 of 32 CMIP5 projects and only 4 of 8-10 variables available
    WCS can query NetCDF (faster?)


http://nrm-erddap.nci.org.au/erddap/info/index.html?page=1&itemsPerPage=1000

https://medium.com/@agafonkin/how-to-give-awesome-public-talks-a2b727f4bc24

Talk about WPS?
Introduction

Geotiffs → WMS → Web map

to get values - WCS or WMS GetFeatureInfo

vs

Geotiffs → Web map
Why

    Want to select and load millions of geotiffs on the fly
    Style dynamically - choose colour scheme, scale, min/max...
    Realtime analysis - contouring, filter values, raster algebra
    Inspect values
    Cache values between analysis

Why not?

    

WMS

Too many dimensions and caching becomes impractical

Dynamic styling is painful (and also makes caching impractical)

Smaller datasets generate more PNG than original dataset!?

No access to actual values - to inspect values have to use GetFeatureInfo WMS request

Millions of Geotiffs?

WMS? no
Dynamic styling?

WMS? no
Analysing values?

WPS? no
Intro to jsframeworks