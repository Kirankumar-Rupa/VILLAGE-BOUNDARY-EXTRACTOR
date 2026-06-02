# *VILLAGE-BOUNDARY-EXTRACTOR*
## *Motivation:*
Sometimes we need only few village shapefiles, but it takes time or sometimes system crashes due to heavy data to extract such village boundaries from the whole state data, so this code helps to extract the village Boundary by Village Attributes and Filter Options and converts to the Shape file. This code is useful mostly for the low-configuration systems as GIS Softwares so much time for loading or sometimes its crashes.

## *Data Sources:*
you can download few of the Village Boundary Geojson files from [*Data {Meet}*](https://projects.datameet.org/indian_village_boundaries/) Website
Here are the available Data from the above website currently
* Bihar
* Karnataka
* Kerala
* Goa
* Gujarat
* Maharastra
* Sikkim
* Odisha

## *Procedure:*
1. Install Geopandas library into your python.
2. Download Geojson file from the link or any other sources.
3. Assign the full path of the Geojson file to the *gdf* variable.
4. You can see the Column Headings present in the Geojson file after running the *print(gdf.columns)*
5. Next you can see the format of the Attribute names in specified column, if you want to view other column change the column name in *for name in sorted(gdf["column_name"].dropna().unique()):*
6. Filter the data by Specified Column and its value
7. After finding the village that you need assign it to a *feature* variable
8. Here I filtered by *(gdf["NAME"] == "Chicholi") &  (gdf.index == 8307)* name and its index number
9. You will get a preview on maps.
10. Give output path in the *output* variable
11. Here the Shape file is saved and ready.
