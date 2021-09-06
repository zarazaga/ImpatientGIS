
# ImpatientGIS

## Chapter 3
# Visualize Categories and Quantities of Data.

## 3.1 Work with data

Neighborhood activists need good places to meet, like cafes or pubs. Find out whether the level of activism has any relation to the number of cafes. 

Back to the 2d map. 

Turn on the layer for Shops, and select a sub-set of the data that is ONLY the shops that are cafes, restaurants and pubs.

**Using Select by Attribute**

![](SHOTS3/2select.png)

Shop-survey has an attribute called 'Descrip10' with use type. Right-click and 'Sort Ascending' to read through the list of names.  Its not a very tidy data-set. Note that there are sometimes several similar names for the same sort of use. You could, however, use this information to select those uses, and then export the selected data to create new layers - first extracting coffeeshop/cafes, and also pubs/bars. (but it takes a long time since the data is messy)
However there is also another useful attribute called 'CLASS10'. The class type 3 appears to map fairly nicely to the combination of cafes, bars and restaurants that we were looking at. In order to select restaurants and bars - one can 'select by attribute' in CLASS 10
![](SHOTS3/selectAttr2.png)
**Map** > Select by attribute > useclass10 = Class 3

This selection is now visible in the table.

![](SHOTS3/selection.png)

Export those selected features to create a new data set. 
**Data** > Export Features > Feature Class to Feature Class

The is a geoprocessing tool - a first, fairly simple manipulation of data.

![](SHOTS3/export.png)

This new dataset will be placed INSIDE the globaldatabase (.gdb) .  *One can use the 'export features tool to export the whole dataset, into the gdb, or to export only certain elements of it, as here.* 

![](SHOTS3/feature2feature.png)

After using the select tool, remember to **clear** the selection.

![](SHOTS3/2select.png)

The restaurants and cafes seem to be more connected to the road pattern than the neighborhoods.
![](SHOTS3/AllPubCafe.png)

Rather than extracting data according to its attributes it can be extracted according to its location. 

*How many cafes and restuarants are within 0.5 km of the tram line?*


## 3.2 Symbology: Heat Map & dot density

Clearly cafes and restaurants are not well distributed. Messing around with the symbology allows differnt visualisations of the same data- communicating the story in different ways.

**Appearance** > Symbology > Primary Symbology > Heat Map
This symbology reveals the density of points in a dataset. 

![](SHOTS3/HeatMap.png)

This allows one to see that the center of the city is the most densly provided with eaterys. 

![](SHOTS3/EdinHeatMap.png)

Changing the symbology of the neighborhood layer allows one to see clearly that there are active zones which could use a community cafe!

![](SHOTS3/DotDensity.png)

## 3.3 Statistics

One can use simple geospatial statistics tools to bring together data. 
*How many bars and restaurants are within each neighborhood?*

There are hundreds of tools in a GIS software like ArcGIS Pro. And new ones are alwasy added. Eventually one can write one's own tools. Some tools are used frequently, and some are only used by specialists in their own area.  
Many GIS tasks become so common one forgets they are geoprocessing tools. 
ie- the tool **Feature Class to Feature Class** (when data was exported to the geodatabase) was already an example tested here. 

Some of the most common tools appear as icons in the Analysis ribbon. But most tools are in the toolbox. 

![](SHOTS3/findTools.png)

The next chapter will jump into various different kinds of **Spatial Tools**.  Statistics are **Analysis tools**

![](SHOTS3/toolbox.png)

**Analysis** > Tools > **Summarize Within** > 

![](SHOTS3/Summarize.png)

The new CafeBar)neighborhoods layer, (which has been saved in the geodatabase) can now be symbolised as a polygon layer, to show those neighborhoods that have more, and fewer, cafes.

And this new data can be shown in relation to the tram line, to build on a discussion of development of that line. 
![](SHOTS3/tramCafe.png)




