
## GEOG 458 Lab 4 – Tile Map Generation Live Web Map You can view the interactive web map 

### Project Overview 

This project demonstrates the generation of web map tiles using QGIS and
their integration into a Mapbox GL JS application. The goal of this lab
was to create four separate raster tile sets and combine them into a
single interactive web map with layer controls. The map focuses on Road
Weather Information (RWI) Stations in Seattle, Washington, and explores
different ways of pairing thematic data with basemap styles. All tiles
were exported in Web Mercator (EPSG:3857) using QMetaTiles and organized
in a standard {z}/{x}/{y}.png structure.

### Study Area 

The examined geographic area is Seattle, Washington The map extent was
limited to the Seattle city region in order to:

-   Reduce tile count

-   Stay within GitHub file size limits

-   Improve performance

### Tile Sets Description  

#### Modified Basemap 

A customized grayscale basemap created using Mapbox Studio. Minor
modifications were made to color scheme and styling to create a clean
monochrome design. Designed to function as a contextual base layer. Zoom
Levels: 10–13

#### RWI Station Data 

Road Weather Information (RWI) Stations exported as raster tiles. This
version includes the grayscale basemap baked into the tiles (similar to
the professor’s 911 example). Ensures the thematic data remains paired
with grayscale styling even when switching basemap radio buttons. Zoom
Levels: 10–13

#### Basemap and Data

Combined export of grayscale basemap and RWI stations. Functions as a
fully pre-rendered thematic map. Demonstrates raster pairing of data and
basemap inside QGIS before export. Zoom Levels: 10–13

#### UW Theme 

A themed basemap inspired by University of Washington colors. Designed
in Mapbox Studio using customized color and styling elements.
Demonstrates how thematic visual identity can be implemented in basemap
design. Zoom Levels: 10–13.

###  Technical Workflow 

1.  Created and styled basemaps in Mapbox Studio.
2.  Loaded Mapbox WMTS layers into QGIS.
3.  Styled and overlaid RWI station data.
4.  Exported raster tiles using QMetaTiles.
5.  Organized tile structure in /assets/.
6.  Integrated all tile sets into a full-screen Mapbox GL JS web
    application.
7.  Implemented:
    1.  Basemap radio controls
    2.  Tile layer checkboxes
    3.   Scale bar
    4.  Navigation controls

### Repository Structure

geog_458_lab4/\
│\
├── index.html\
├── README.md\
└── assets/\
├── Modified Basemap/\
├── RWI Station data/\
├── Basemap and Data/\
└── UW Theme/

Each tile set follows the `{z}/{x}/{y}.png` tile pyramid format.
