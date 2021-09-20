
# ImpatientGIS

## Chapter 2
# Visualize Categories and Quantities of Data.

## 2.1 Classify Polygon Data

*Invent another Question to ask the data . .How does the location of polling stations relate to amount of neighborhood participation in this area?*

**Choropleth maps** to show quantity

By making graduated colored polygons, one can reveal the quantity of electors in each neighborhood. 
Turn off the other layers, and the confusing lables. 

![](SHOTS2/GraduatedColors.png)

**Symbology > Primary symbology > Graduated Colors > Field > SUM_ELECTNO **(sum of the numbers of participants in this neighborhood survey).

![](SHOTS2/GraduatedColors2.png)

Look carefully at the map. Neighborhoods have very different areas. And the color of the neighborhood depends on the total number of participants. The biggest participant population shows to be in the largest areas of neighborhood - this seems rather obvious and probably not very useful. Actually it would be more useful to show proportionally how active participants in each neighborhood are, dependent on its area. - ie. we'd rather show density of participation. To do that you need to find an attribute that gives area.  

Then normalize the total ELECTNO number by dividing that total by area **Normalization > Shapearea >.** 
*'Normalizing' is a way to calculate this new data-attribute 'on the fly' in order to quickly reveal the data in a way that is useful.*

**Classification Methods**

The choice of classification methods tells the GIS how to divide the resulting range of outcomes into the 5 different color buckets.  Depending on your data and the story you want to tell, different methods work well in diffrent contexts.  Standard deviations are best for statistical models, quantile splits the data evenly, and manaul allows one to set the specific limits. (Each classification method is clearly described in the drop-down. ) Test each of the different **Classification Methods** to find one that gives the best spread of colors across the density range. 

![](SHOTS2/ClassificationMethods.png)

## 1.6 Map Design

Visual communication requires careful observation of the relationships between color, scale and ideas: design the layer choices, colors, lables and Classification Method to best communicate the study issue.  Think about the story that the map is trying to tell, and take control of the messaging. Dont let ESRI defaults be in charge. Design it your way!

*Clearly some very active and dense neighborhoods seem to have few council polling sites!  Which neighborhoods could use a new site? Maybe Pilton? It might be worth doing additional research into the neighborhood as part of the study.*

![](SHOTS2/Pilton.png)

**SAVE** the map for future analysis.


## 3.1 Working with Fields

A feature layer has a series of attributes. These are the columns on the table.  Normalising was a way to calculate density 'on the fly'. But what if one wanted to do additional work using this data set.  One might want to add a new field. Make a new field that gives the 'density' of neighborhood participation. 

In the attribute table, **Add a field**

![](SHOTS2/addField.png)

Make a space for a 'float' type, for a calculation of activist density. 

![](SHOTS2/FieldDensity.png)

At the top of the window/ ribbon is a new 'save' button for this Field editing session. **Save** the modifications to the table.

In the Attribute table, Right-Click on the field to **Calculate Field**
![](SHOTS2/calculate.png)

Double-clicking a field name brings that field into the calculation.  Multiply the ELECTNO by 1000 to have density results in sq.m instead of sq.Km.  

![](SHOTS2/AcDensity.png) 

Run the calculation. Then check the new field. Right-click on the column and **Sort Descending** to check that the field has populated with data. Note that there are many neighborhoods with '0'in this column. *Why?*

## 3.2 Visualise that data in 3d
*Where are the most densely active neighborhoods in the city?*

To get the data into 3-d, first check the coordinate system - Is the map projecting to a curved surface or a flat surface?

*All GIS data is located, through its lat-long data, at a specific place on the globe.  That georaphic location doesn't change.  But the way that the map makes that data visible, changes according to the particular strategy that the map-maker choses to use, to project the elemets of that geographic data onto flat screen- or page.* see  https://www.esri.com/arcgis-blog/products/arcgis-pro/mapping/gcs_vs_pcs/ 

On the Anlysis Tab > Environments > Output Coordinates

![](SHOTS2/BritishNat.png) 

The British National Grid is like a flattened grad set across the UK. So we will make a local 'scene'.

*The choice between local and global depends on the scale of the data - on whether you want to make a 3d of a flat surface (like a city), or see 3-d world data on a globe. This specific data came from a dataset which was projected onto the British grid using a 'flattened' projection, like a folded city-map from which distances can be measured, rather than the 'geographical' system which is curved like a classroom globe.*

View > Convert > to Local Scene

![](SHOTS2/Convert.png)

Return to **Map**>Explore> Use the mouse wheel button to zoom back from the 3d model. 

Drag the layer from the **2D Layers** up into the **3D Layers** section in *Contents* to create a volumetric visualisation of the density of activities in SUM_ELECNO.  

Instruct the data to read density as the 'z'value.

**Feature Layer** > Appearance > Extrusion > Type > Absolute Height.
The vertical value **Field** is AcDenisty.

'Units' are meaningly for this 'z' dimension; select 'Kilometers'for now.  

It looks terrible! That vertical value is too high in. Trying 'meters' doesnt seem to help either with the vertical proportion - it is too low.

Create a new custom 'Field' expression.   
 ![](SHOTS2/Expression.png)
 ![](SHOTS2/ExpressionBuilder.png)
 
 Double-click on 'AcDenisty' and multiply by something like 50.  

![](SHOTS2/3d.png)

*What does this map show? What are the neighborhoods with extra-tall data towers, compared to the very low ones . .and what do you think this could reveal to the city?*