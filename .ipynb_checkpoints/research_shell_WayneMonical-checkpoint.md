
# Elk Migration Research Summary

## Summary 

In the Fall 2024 introductory Data Science class, my team and I researched the **migration patterns of elk** in Yellowstone National Park in relation to **environmental factors**. This project challenged me to combine disparate data sources and learn to work with a unique file type. The project was featured in class, and the project website is available [here](https://brooklynnrm.github.io/Elk-Migration.github.io/index.html). 


## Combining Data

I combined five data sources to create a unified table to make analysis easy. Each data source was documented, examined, and cleaned. Each row in the table was a single observation of a single elk with a timestamp, a location given in latitude and longitude, the temperature, rainfall, vegetation, and chemical contamination at that location. *Combining these data sets allowed us to answer our questions about elk movement in relation to the environmental factors and make surprising discoveries.* 

We discovered that **high arsenic concentrations** were reported in July and August of 2010 at the water sampling site GRTE_SNR01. At the same time, two elk had traveled around this sampling site, potentially exposing themselves to unhealthy levels of arsenic in water. Other notable markers of poor water quality that we observed included low dissolved oxygen concentrations in June and July of 2010, as well as relatively high chloride levels in October of 2010. Chloride is a chemical that may indicate the presence of lead in water, which has no safe concentration for exposure.

![arsenic](images/arsenic.png)

## Geographic Data

I learned to utilize geographic data in the form of raster files. I imported vegetation land cover data taken via satellite from the state of Wyoming. After much experimentation, I learned to use the tools in the [terra R package](https://cran.r-project.org/web/packages/terra/index.html). I reprojected the coordinates of the raster file to latitude and longitude, so that they would align with the elk's location data (also given in latitude and longitude) and the maps given in the [ggmap package](https://cran.r-project.org/web/packages/ggmap/index.html), allowing side by side comparisons of elk activity along geographic and natural borders. 

![maps](images/elk_paths.png)



# 


