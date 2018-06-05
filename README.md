# Project-TCET
Academic project for evaluating impact of hazardous waste product.

Our custom script tool aims to demonstrates impacted study areas from nuclear waste that allows the non-technical user who may or may not have technical understanding of GIS technology to use geospatial analysis to visualize hazardous waste permeation in their surrounding environment. Thus, we designed this ArcGIS custom script tool to provide knowledgeable visual information regarding past, present, and future costs to the environment, economy, and human wellness for public users.

Project Tool Primary Functionalities:
1) Land use impact assessment - 
   The land use tool was built with multiple functions to analyze the relationship between waste sites and land use parcels from the  census.  First the tool creates a buffer around the waste site points with a variable input.  The parcel data was dissolved next to combine like land use types, before being clipped to the buffer zone.  A field was added to the new clipped parcels to calculate the area within the buffer for each land use type.  This value gives us an idea of how much area may be within a dangerous distance from these waste sites.
 
2) Land cover prediction surface generation - 
   This tool was created using EBK (Empirical Bayesian Kriging) interpolation method to display a surface prediction map.  This displays random variables at locations where data has not been collected and helps the user understand weather a critical value has been exceeded or approaching a threshold.  

3) Local hydrology delineation - 
   The hydrological delineation tool was built with multiple raster analysis functions to derive the local hydrology through accumulation of water flow and drainage basins.  The tool takes in a single digital elevation model (DEM) to process.  Flow direction and accumulation was determined from the DEM and stream features are derived from “True” streams through the con tool. The stream features are then queried to filter out primary streamflow in the area. Basin polygons are derived from flow direction raster data to delineate drainage basins in the study location

