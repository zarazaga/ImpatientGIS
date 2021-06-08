# ImpatientGIS

## Chapter 7
# Manipulate Imagery as Raster data


Imagery date, whether it is collacted as multispectral bands, (layers of imagery information which combined to make real-color images) or DEM (digital elevation models showing the topography of the earth's surface) or other spectral imagery, are defined by the way the data is spatially arranged. Unlike VECTOR data, in which points, lines and polygons are collected into tables with GPS information and additional attribute fields, Imagery or RASTER data information is collected in a grid, in which each small pixel square has a value, and the relationship between those values gives information.   

## 7.0 Download and Render Raster Data

*Invent a question to ask the data . .Kenya is the biggest Tea exporter in Africa; an important cash crop, it grows best on tropical red volcanic soils found in high altitude areas of Kenya, between 1,500 and 2,250 meters above sea level, with well-distributed rainfall ranging from 1,200 to 2,500 mm annually. Where might we find potential zones for further development of tea plantations in Kenya?*

Search for: (World Resource Institute) **'wri kenya gis data'**

**Download dem_250m.zip** the digital elevation model that will show to show altitude as pixels. **Unzip**, and, in a new Arcgis Pro Map, **Insert > Add Folder** , find the data, and drag it into the map. 

Since the final ambition is to measure areas for tea, the whole study should be done in a Projected Coordinate System.  

## 7.1 A short, important detour to discuss projection systems

(Remember, GCS - geographic coordinate systems, show the are desgined to reveal location accurately but does a poor job at measurement. World Geodetic System 1984 (WGS 1984) is the standard geogrphic system.  Projected systems project a piece of the world onto a flat sheet, straightening out some of the lines.  The most common projection systems are 

Heinrich C. Albers design a projection system that works well for areas - neither shape not north-south parallel lines are prioritised, but it minimises distortion for areas, within certain parallels.  Note: fully understanding coordinate systems is an expert field; for those who are impatient, it is important to know that every map requires a coordinate decision, depending on scale, and the message that will be communicated. One can google best practices for any part of the world only if the correct question has been asked . .https://www.esri.com/arcgis-blog/products/arcgis-pro/mapping/gcs_vs_pcs/

Bring it DEM first- it is already in WGS 84 – so that will set the backgound coordinate system.
Geographic vs projected- geographic is whole globe – projected is projecting the map image onto a flat sheet and straightening out the lines . .  tell the difference by the measurement scale 
WGS84 is geographic  
Equal area projection - Albers is projected – but just along two parallels – to make areas work better

## 7.2 visualise or Render DEM raster data
bring in dem
note -24 to 4786
black 67
white up to 2500      The dots are a different color depening on height
