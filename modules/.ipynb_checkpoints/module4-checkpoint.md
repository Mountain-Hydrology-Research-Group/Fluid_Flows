# 4) Watershed Hydrology


```note
## Lab 4: Preparing for watershed delineation

Most of hydrology involves solving for the mass balance of water within a control volume, but the control volume has a unique shape, defined as all locations upstream of a designated spot on a river, where all droplets of water falling within that shape will flow downhill and reach the designated spot. 

We will be delineating Seattle's Cedar River Watershed as homework this week, following online directions or a pre-recorded tutorial. GIS is a very marketable skill, and consultants are often asked to delineate watersheds. First, you will need to decide which software you want to use.

Arc-GIS:  
* Arc-GIS is proprietary software, but the UW has permission to use it.  You can access Arc-GIS in the CEE computer lab, or through [remote login](https://www.ce.washington.edu/current/computing/computers-available-remote-desktop) to the CEE computers.  If you have a PC, you may also install Arc-GIS on your laptop by following the instructions at this [link](https://sites.uw.edu/arcgis/software/arcgis-desktop/arcgis-pro/).  Note that this also requires installing VPN software to connect to the UW network securely, which enables the licensing through UW.   
* For further background on Arc-GIS, I recommend class material from David Tarboton from Utah State University and David Maidment from U. Texas Austin, available [here]( http://hydrology.usu.edu/dtarb/giswr/2018/).  For watershed delineation, check out exercise 4 from class 11, see minute 10 of this [video](https://www.youtube.com/watch?v=hE2hBMRJq3U&feature=youtu.be).

qGIS: 
* qGIS is open source software and can be installed locally without license issues.  If you want to use a Mac, this is your only GIS choice.  You can download and install [here](https://qgis.org/en/site/forusers/download.html).
* For further background, the authors of QGIS for Hydrological Applications, Kurt Menke and Hans van der Kwast, put on a special QGIS Hydro Webinar Series in spring 2020, including webinars on [how to georeference a physical map](https://www.youtube.com/watch?v=hPLqy-NBgu8), [how to get tables and coordinates into qGIS and interpolate to rasters](https://www.youtube.com/watch?v=84cq3CmBwck), [spatial analysis](https://www.youtube.com/watch?v=XFFAS-UctBs), and [stream and catchment delineation](https://www.youtube.com/watch?v=2Ub0c7Ss-T4).

Python:
* If you feel comfortable with Python, you can use it to delineate watersheds, using the [pysheds](https://mattbartos.com/pysheds/) Python package and following the step-by-step directions [here](https://medium.com/@ilmachairas/basin-delineation-on-python-5e9da00a3534).
* You can download an example jupyter notebook to try on our jupyterhub [here](lab4/1_Pysheds_delineation.ipynb).  This was put together by Emma Boudreau following the information and links above.  Reach out if you need help with the pip install on the jupyterhub. 

USGS StreamStats:
* [StreamStats](https://streamstats.usgs.gov/ss/) is a Web-application that provides access to many GIS-analytical tools that are useful to understand watershed characteristics and hydrology, as well as mapping out locations of USGS gauges and providing associated streamflow data.
* [Watershed Delineation](https://www.usgs.gov/streamstats/identify-study-area-and-delineate-basin) can be completed very easily following the linked [directions](https://www.usgs.gov/streamstats/identify-study-area-and-delineate-basin).  However, many of the steps involved are not clear from following this process, so if you choose this route, the homework asks you to explain the processes of how the calculation took place.


```


## Homework 4

### Problem 1: Delineate the Cedar River Watershed

Either install GIS software locally or go to the CEE computer lab (see notes above).
 
**A.** Go to the class [canvas page](https://canvas.uw.edu) and download the files relevant to your chosen software.  Note that if you are using the StreamStats   

**B.** Delineate the Cedar River Watershed above Cedar Falls (this corresponds to USGS gauge 12116400) and calculate its area.  Follow the video directions for [ArcGIS](https://youtu.be/MR6_IenN9vI) or for qGIS in [Part 1](https://youtu.be/u9tiOomhgIg) and [Part 2](https://youtu.be/IXkFH0elFZk).  If you choose to use StreamStats, export your shape file as a .kml file and then import it to [Google Earth](https://earth.google.com/).  Click on the arrow to expand the properties and get the info for the shape.  Also, in properties, change the fill to 0 and make the outline a width and color you can see.

**C.** When completed, take a screen shot of your delineated watershed that shows that it's on your computer to submit with your homework along with the area you estimated.  If you used StreamStats and Google Earth, use 3-D mode to rotate and zoom in and out and create some snapshots to annotate to show the physical process of how the edges of the watershed were determined (following our discussion in class).
 


### Problem 2: Monthly Water Balance in the Cedar River Watershed 

Download the [Cedar_average_monthly_waterbalance.xlsx](data/Cedar_average_monthly_waterbalance.xlsx) data file.

The file contains long-term data relevant to the watershed that is Seattle's primary water supply.  Note that the temperature and precipitation values are climatological averages from 1898 to 2016 at Cedar Lake, Washington.  The streamflow is monthly average values from 2001 to 2019 at USGS gauge 12116400 (which is listed as having an area upstream of 217 km^2, which is slightly but not very different from what you should have calculated for Part 1, but use the 217 value here).  The ET values are estimated from monthly graphs produced by NOAA, available [here](http://www.cpc.ncep.noaa.gov/soilmst/e.shtml).  ET values from pan evaporation estimates are also included in the file for your reference, but you do not need to use then in your calculations.   Remember that the Cedar River has the Chester Morse Reservoir above this location and also, as we discussed in lecture, some snow.  The total precipitation values represent rain and snow together, but only at one location in the watershed. Note: You may also want to look at lab 5-1 for help with this problem in Python, but you are also welcome to use Excel.

 **A.** Convert all the units to mm/month and plot the component parts of the basin water balance each month all in the same units (mm/month). 

 **B.** Determine the residual storage term each month (where storage is the sum of water in minus water out).  Calculate the total residual storage over the year.

 **C.** Discuss what you think the storage term means physically and where you think there might be errors in the water balance terms.

