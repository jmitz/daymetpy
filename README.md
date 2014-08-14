# DaymetPy

Functions to (batch) download single pixel [Daymet data](http://daymet.ornl.gov/) directly into your python workspace, or save them as csv files on your computer. Both a batch version as a single download version are provided. Consider downloading gridded data if you download extensive coverage within a single region.

## Installation

clone the project to your home computer using the following command (with git installed)

	git clone https://khufkens@bitbucket.org/khufkens/daymetpy.git

alternatively, download the project using [this link](https://bitbucket.org/khufkens/daymetpy/get/master.zip).

Next, make the script executable

	chmod +x /foo/bar/download.Daymet.py

## Use

For a single site use the following format

 	download_Daymet(site="Oak Ridge National Laboratories",lat=36.0133,lon=-84.2625,start_yr=1980,end_yr=2010,internal=TRUE)

with the subroutine as found in the script. You can use this subroutine in your own code if needed. This subroutine takes the following parameters.
  
Parameter     | Description                      
------------- | ------------------------------ 	
site	      | site name
lat           | latitude of the site
lon           | longitude of the site
start_yr      | start year of the time series (data start in 1980)
end_yr        | end year of the time series (current year - 2 years / for safety, tweak this check to reflect the currently available data)


In stand alone mode, on a terminal you are restricted to batch mode. Batch mode uses a comma separated file with site names and latitude longitude which are sequentially downloaded. Format of the comma separated file is as such: site name, latitude, longitude.

	./download.Daymet.py my_sites_file.csv
