# Data Extraction

The data in this folder is extracted from [Odisha Geoportal](http://gisodisha.nic.in/state/) .

## Link Referance

Refer to the [link](http://164.100.140.64/arcgis/rest/services/OdishaNIC/MapServer) to extract the data.

# Data Access

## API
 * [Services](http://164.100.140.64/arcgis/rest/services)
  * [Odisha NIC Map Server](http://164.100.140.64/arcgis/rest/services/OdishaNIC/MapServer)
    * Layers :
        * [ADMINISTRATIVE LAYER](http://164.100.140.64/arcgis/rest/services/OdishaNIC/MapServer/0)
          * [State_Boundary](http://164.100.140.64/arcgis/rest/services/OdishaNIC/MapServer/1)      
          * [District_Boundary](http://164.100.140.64/arcgis/rest/services/OdishaNIC/MapServer/3)       
          * [Block_Boundary](http://164.100.140.64/arcgis/rest/services/OdishaNIC/MapServer/5)     
          * [Gram Panchayat_Boundary](http://164.100.140.64/arcgis/rest/services/OdishaNIC/MapServer/7)
          * [Village_Boundary](http://164.100.140.64/arcgis/rest/services/OdishaNIC/MapServer/9)
          * [Assembly Constituency_Boundary](http://164.100.140.64/arcgis/rest/services/OdishaNIC/MapServer/13)
          * [Parliamentary Constituency_Boundary](http://164.100.140.64/arcgis/rest/services/OdishaNIC/MapServer/14)

## Folders
  The "Odisha Boundary" folder contains two folders namely "Administraive Boundary" and "Political Boundary". The administrative boundary folder contains the State, District, Block, Gram Panchayat (GP) and Village Boundary. These boundaries are as per the Census of India, 2011. Further, the political boundary folder contains the Assembly Constituency (AC) and Parliamentary Constituency (PC) boundaries.
  
## Format 
  This Repository contains Geospatial Data in [GeoJSON Format](https://en.wikipedia.org/wiki/GeoJSON), which is an open standard format designed for representing simple geographical features.
  
  In case you need this data in shp or KML, or any one of the myrid Vector formats, you could use Gdal's ogr2ogr tool to convert these GeoJSON to your prefered format. This can be done by the following commands:

```ogr2ogr -f shp <output name>.geojson <input name>.geojson``` 

```ogr2ogr -f KML <output name>.kml <input name>.geojson``` 

```ogr2ogr -f LIBKML <output name>.kmz <input name>.geojson```

  
## Saving it using QGIS
 
 The respective Map Server links mentioned above was used to extract the boundary files on QGIS. The steps taken to extract the boundary files from the Map Server link are as follows:
    
   * OGIS 3.18 has been used. Open QGIS on your system and create a new project.
   * On the left-hand side of the screen, the Browser side bar contains ArcGIS REST Servers. Right click on it.
   * A drop-down menu appears, now select "New Connection" from the drop down menu. A pop-up window would appear with the heading "Create a New ArcGIS REST ServerConnection".
   * In the Connection Details of the pop-up window, write the Name in which you want to save the files and in the URL section, enter the Map Server link. Then Click "OK" in the bottom right of the pop-up window.
   * You would now be able to see the name in which you saved the file under ArcGIS REST Servers and from there you can use the boundary files and it will get loaded on the QGIS.

# Data License

Unless explicitly stated, all datasets in this repository is shared under CC BY 4.0 license. Please mention and link to relevant dataset in the attribution, eg. maps of India by CivicDataLab (CC BY 4.0)
    
        
       






