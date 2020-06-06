# ImpatientGIS

## Introduction



### Installling ArcGIS Pro
The license for ArcGIS Pro is embedded into an arcGIS online account.  It seems confusing- why is an online account needed in order to get a desktop software? This is because ArcGIS Pro is fully integrated with the online software- you will access data throught the online portal, and can save and share your work through the online platform. Tools and tasks are visually similar. Think of it as two access points to one platform.  
The online user account is needed in order to sign on to Pro, and is individual to each user account, rather than to each computer. This means a downloaded copy can be loaded on any computer, but only people like you who have a license can sign into it. 

**is there a free 180 days with this book?  I will need help with instructions for non-students!**

From your *ArcGIS online* account:
Download the ArcGIS Pro installer from the *My settings* page in your user profile.  

1.	Log into your *ArcGIS Online* account
2.	Go to "*My settings*" [top right]
3.	Choose “*Licenses*”
4.	Click the download link next to ArcGIS Pro

### Is ArcGIS different from ArcMap and ArcGIS Pro?
ArcGIS is a collective name for many different GIS softares made by ESRI. It has two primary desktop versions: ArcMap and ArcGIS Pro. In this book we will often shorten the name to '*Pro*'.  
Once you know how to work with one GIS software you will understand the structure of many others. Although it is written for this software, many of the instructions, ideas and tools here can be adapted to other GIS packages including open source software and older GIS packages. 

ArcGIS Pro (like ArcMap) only works on Windows. A mac will need bootcamp or parallels: https://pro.arcgis.com/en/pro-app/get-started/run-pro-on-a-mac.htm

### Backup data for the exercises
Gathering data is a primary part of doing geospatial work. Learning GIS here will include gathering and creating datasets. But a backup copy of the data is available at escri.com/impatientGIS. 

### ArcGIS Pro Help
Software changes fast. It's frustrating. As soon as one learn's something, a new aspect will be developed.  But you have to start somewhere. This book will not teach you everything you need to know- rather it is intended to give you enough knowledge to ask the right questions. The greatest source for using ArcGIS Pro is the ESRI help webiste. But often it is hard to understand the instructions until you have some GIS experience. In some ways the aim of this book it to make you comfortable making use of, and asking specific and difficult questions from, ESRI help.

https://pro.arcgis.com/en/pro-app/help

## Chapter 1
# import point and polygon data into ArcGIS Pro

*example: A women's health NGO wants to build a new clinic in Botswana. We need location data: where are existing clinics exist and where are the gaps where a new one would be most helpful?* 

Jump in! First search the internet for *shapefiles* about *health* in *Bostwana*. 

*A **shapefile** is a geospatialdata-file in which information is packaged along with geometries (points or shapes) and their location in the world, usually defined by a lat-long coordinate. Such data can also be saved in a table, with lat.long data, or as a geoJson (a java native geospatial data structure)*.  

You search for Botswana, shapefile, health, and you find the *Bostwana Humnaitarian Data Exchange*. That sounds promising. Narrowing the format options to *zipped shapefiles* reduces the length of the list. I downloaded *Botswana-healthsites* and . Try to avoid raster data which shows, for example population density per-pixel.



Geospatial data vector data has points, lines or polgons

*note: Each chapter builds up an example study to follow. But you can always choose to create a similar study, using a location or question that is more interesting to you.*


