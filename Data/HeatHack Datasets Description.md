
# HeatHack 2022 – Dataset Description

_Hacking solutions to address the challenge of climate change and urban heat in the Triangle_

  

### Data Overview

The HeatHack 2022 Data Science Collabathon aims to bring together coders, programmers, data visualization whizzes, and environmental enthusiasts to help us discover actionable insights, develop engaging data visuals, and create action plans to address the growing and intensifying challenge of climate change and urban heat in the Triangle.

The datasets we provide consist of air temperature, humidity, or heat index collected by our citizen scientists during the HeatWatch campaign last summer at Durham/Raleigh and Chapel Hill. To learn more about the campaign, please find more details here: [HeatWatch: Chapel Hill – Data release and report](https://datadrivenlab.org/climate/ddl-releases-2021-chapel-hill-heatwatch-data-report/); [Urban Heat Island Temperature Mapping Campaign – Raleigh and Durham 2021](https://climate.ncsu.edu/research/uhi/#:~:text=Raleigh%20and%20Durham%20%E2%80%93%202021&text=In%202021%2C%20Raleigh%20and%20Durham,cities%20of%20Raleigh%20and%20Durham.). To reduce the time cost of data preprocessing, we have cleaned the campaign data and enriched the datasets with a range of variables including landcover/ land use, vegetation index, built-up area index, land surface temperature, etc. Depending on your team’s challenge, you are welcome to use other data either from public sources or your own research. We also provided the links to other external data sources. Please find them at the end of this document.


The data are provided primarily as excel sheets. From the first tab of each excel sheet, you will find the detailed description and data type of each variable. For those people familiar with working with spatial data, we have provided these data in the spatial form as well. There are shapefiles of both the point data and the aggregated census tract and block group. In addition, we have provided all the raw remote sensing data in raster form.
  

### Data Pre-Processing

The original heat data exists in two forms– the original point data, and a continuous raster. The original points represent the actual collected temperature values during the HeatWatch campaigns and the raster represents temperature estimates for the entire study area, using the collected points and additional variables used in the prediction methodology.
  

For the Heat Hack, we have provided the temperature data in three formats: original point data, the original raster data, and the datasets aggregated to census tracts and block groups. The original point temperature and aggregated data have been supplemented by a number of other variables calculated by remote sensing data. These variables are described in the “Input Variables” section.

In the point data, each row corresponds to a geographical location where the citizen scientist collected the air temperature and humidity during the campaign (See figure below). This type of data gives more details of how the variables (ex: heat or other input variables) may vary at the individual’s level.


![point_data](Doc/point_data.png?raw=true "Title")

The aggregated datasets aggregate both the temperature data and the other remote sensing data, to the census tract and block group to produce an easy analyze the dataset. These data represent mean values per census tract and block group for the temperature data and all of the input variables. The aggregated datasets focus on the neighborhood level. By joining the demographic and economic data (also provided), you may find insights into how the temperature can vary between different social-economic groups.

![group_data](Doc/group_data.png?raw=true "Title")

### Input Variables

We have provided hackers with a number of interesting input variables that hackers may choose to use.

__Land Cover Data:__

Temperature is often correlated with land cover. To explore potential relationships between land cover and temperature, we have provided a number of land cover variables, including NDVI and NDBI, which represent the Normalized Difference Vegetation Index (a measure from -1 to 1 that represents vegetation cover in an area) and the Normalized Difference Built Index (a measure from -1 to 1 that represents how developed an area is). Both of these indexes are calculated using bands in the LANDSAT satellite. In addition, we have provided two different land cover classification datasets, including the 2016 National Land Cover Database (30m resolution), and the 2020 European Space Agency WorldCover dataset (10m resolution).

  
  

__Land Surface Temperature Data:__

Although there are differences between ambient temperature, which represents the data collected by the heat campaigns, and Land Surface Temperature (LST), which is most often collected by satellites, these two temperatures are correlated. We have provided a number of land surface temperature estimates from three different satellites– ECOSTRESS, MODIS, and LANDSAT. The ability of these satellites to capture LST is a function of cloud coverage, meaning that on days where there is a lot of cloud coverage, LST might not be captured. Because of this, you may notice different dates of LST which don’t exactly line up with the study days. These satellites also have different return periods, and different spatial resolutions.

  

__NAIP Imagery:__

The National Agriculture Imagery Program (NAIP) collects leaf-on aerial imagery at 1m resolution. This imagery contains 4 bands (Red, Green, Blue, and Near Infrared) that may have interesting relationships to heat and temperature.

  

__ACS Data:__

For those hackers interested in exploring relationships between heat and community variables, we have provided a great number of demographic variables collected from the American Community Survey. Visit the README_ACSData.txt file for complete information on the variables available.

  
  
 __Low Income Energy Affordability Data (LEAD):__

The Low-Income Energy Affordability Data (LEAD) Tool was developed by the US Department of Energy to help stakeholders better understand the energy burdens on low and moderate income households throughout the US. The LEAD Tool provides information on energy and housing characteristics for cohorts of households at the state, city, county, and census tract levels. LEAD data for North Carolina is available in a Google Drive folder at the following link: https://drive.google.com/drive/folders/198XITVRTHJOcFwMB_9pQb-eOXuHRaBiJ?usp=sharing. The folder includes six Excel files organized by the income brackets used (area median income (AMI), federal poverty line (FPL), and state median income (SMI)) and geography (census tracts and states, counties, and cities) and a data dictionary included as a separate file ("LEAD Data Dictionary").

If you'd like to download data for additional US states or learn more about the LEAD tool, please visit: https://www.energy.gov/eere/slsc/maps/lead-tool
  
  

__Other Data__

To help brainstorm and execute potential hack ideas, we have provided links to a large number of other interesting spatial datasets that have not been pre-processed.

  

Raleigh/Durham Spatial Data:
https://docs.google.com/document/d/1E7pbUoQAUjs_fQKOQSa0j-VI1iQCHqIp/edit

  
Chapel Hill Spatial Data:
https://docs.google.com/document/d/1fb5g6LH2NKTMmcGMXa-il9kH1S07a1SO/edit


General North Carolina Spatial Data:
https://docs.google.com/document/d/173nQyvWEAcvhGVBrktf97IXrRC9ml3_7/edit

Awesome Public Datasets
https://github.com/awesomedata/awesome-public-datasets#natural-language
