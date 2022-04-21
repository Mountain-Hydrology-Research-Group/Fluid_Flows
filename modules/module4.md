# 4) Watershed Hydrology


```note
## Lab 4: Preparing for watershed delineation

We will be delineating Seattle's Cedar River Watershed as homework this week, following pre-recorded tutorials. GIS is a very marketable skill, and consultants are often asked to delineate watersheds. First, you will need to decide which software you want to use.

Arc-GIS:  
* Arc-GIS is proprietary software, but the UW has permission to use it.  You can access Arc-GIS in the CEE computer lab, or through [remote login](https://www.ce.washington.edu/current/computing/computers-available-remote-desktop) to the CEE computers.  If you have a PC, you may also install Arc-GIS on your laptop by following the instructions at this [link](https://sites.uw.edu/arcgis/software/arcgis-desktop/arcgis-pro/).  Note that this also requires installing VPN software to connect to the UW network securely, which enables the licensing through UW.   
* For further background on Arc-GIS, I recommend class material from David Tarboton from Utah State University and David Maidment from U. Texas Austin, available [here]( http://hydrology.usu.edu/dtarb/giswr/2018/).  For watershed delineation, check out exercise 4 from class 11, see minute 10 of this [video](https://www.youtube.com/watch?v=hE2hBMRJq3U&feature=youtu.be).

qGIS: 
* qGIS is open source software and can be installed locally without license issues.  If you want to use a Mac, this is your only choice.  You can download and install [here](https://qgis.org/en/site/forusers/download.html).
* For further background, the authors of QGIS for Hydrological Applications, Kurt Menke and Hans van der Kwast, put on a special QGIS Hydro Webinar Series in spring 2020, including webinars on [how to georeference a physical map](https://www.youtube.com/watch?v=hPLqy-NBgu8), [how to get tables and coordinates into qGIS and interpolate to rasters](https://www.youtube.com/watch?v=84cq3CmBwck), [spatial analysis](https://www.youtube.com/watch?v=XFFAS-UctBs), and [stream and catchment delineation](https://www.youtube.com/watch?v=2Ub0c7Ss-T4).

```


## Homework 4

### Problem 1: Delineate the Cedar River Watershed

Either install GIS software locally or go to the CEE computer lab (see notes above).
 
**A.** Go to the class [canvas page](https://canvas.uw.edu) and download the files relevant to your chosen software.  

**B.** Delineate the Cedar River Watershed above Cedar Falls and calculate its area.  Follow the video directions for [ArcGIS](https://youtu.be/MR6_IenN9vI) or for qGIS in [Part 1](https://youtu.be/u9tiOomhgIg) and [Part 2](https://youtu.be/IXkFH0elFZk).

**C.** When completed, take a screen shot of your delineated watershed that shows that it's on your computer to submit with your homework along with the area you estimated.
 


### Problem 2: Monthly Water Balance in the Cedar River Watershed 

Download the [Cedar_average_monthly_waterbalance.xlsx](data/Cedar_average_monthly_waterbalance.xlsx) data file.

The file contains long-term data relevant to the watershed that is Seattle's primary water supply.  Note that the temperature and precipitation values are climatological averages from 1898 to 2016 at Cedar Lake, Washington.  The streamflow is monthly average values from 2001 to 2019 at USGS gauge 12116400 (which is listed as having an area upstream of 217 km^2, which is slightly but not very different from what you should have calculated for Part 1, but use the 217 value here).  The ET values are estimated from monthly graphs produced by NOAA, available [here](http://www.cpc.ncep.noaa.gov/soilmst/e.shtml).  ET values from pan evaporation estimates are also included in the file for your reference, but you do not need to use then in your calculations.   Remember that the Cedar River has the Chester Morse Reservoir above this location and also, as we discussed in lecture, some snow.  The total precipitation values represent rain and snow together, but only at one location in the watershed. 

 **A.** Convert all the units to mm/month and plot the component parts of the basin water balance each month all in the same units (mm/month). 

 **B.** Determine the residual storage term each month (where storage is the sum of water in minus water out).  Calculate the total residual storage over the year.

 **C.** Discuss what you think the storage term means physically and where you think there might be errors in the water balance terms.

