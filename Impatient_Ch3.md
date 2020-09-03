
# ImpatientGIS

## Chapter 3
# Visualize Categories and Quantities of Data.

## 3.1 Visualise that data in 3d
*Where are the most densely inabited parts of the city?*

View > Convert > to Local Scene (*The choice between local and global depends on the projection type - how the world is seen on the screen. This specific data came in using a 'flattened' projection, like a folded city-map, rather than the geographical system like a classroom globe.*)

![](SHOTS3/Convert.png)

Return to Map>Explore> and use the wheel button on the mouse to zoom back from and into the 3d model. 

To create visualisation of the people-count in SUM_ELECNO, drag the layer from the **2D Layers** into the **3D Layers** section.
Feature Layer > Appearance > Extrusion > Type > Absolute Height.
The vertical value **Field** is SUM_ELECNO.

Wow-  that is too large a number.  AND, remember, it is absolute value. We need to normalise that number again by area.

Click on 'SUM_ELECNO' and divide it by Shapearea. Note that the numbers are so low (all <1) so it is useful to multiply it by 100.
Create a new expression.  **$feature.SUM_ELECNO*100/$feature.Shapearea**
 ![](SHOTS3/Expression.png)
 
![](SHOTS3/expressionBuilder.png)
