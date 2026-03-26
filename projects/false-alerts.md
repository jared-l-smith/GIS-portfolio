
# False Alerts in Cook County’s Electronic Monitoring System

**Date:** June 2024  
**Tools:** Python | Pandas | GeoPandas

## Overview
[2-3 sentence description of what this project was about and what you created]

## Skills Demonstrated
- [Skill 1]
- [Skill 2]
- [Skill 3]

# Background:

Electronic monitoring is a form of remote surveillance that law enforcement uses as an alternative to incarceration: a person on house arrest may be tracked via a GPS ankle monitor, for example. Advocates of this form of tracking believe it improves the quality of life for the monitored individual. A person on house arrest may not be confined to their home: they can travel to work and school while under law enforcement supervision. 

However, a major downside of GPS monitoring is ‘false alerts’: a weak GPS signal can distort the location of the monitored individual. This makes it appear that a person is breaking the terms of their home arrest, even though no violation occurred. Reports indicate that false alerts have led law enforcement to harass rule-following supervisees. Cook County, Illinois, has one of the largest electronic monitoring caseloads among local government units in the United States.

In cities, a common source of GPS signal error is interference from the built environment. Tall buildings can block or reflect signals, preventing a strong, clear connection between the GPS satellite and the receiver. This project investigates the potential relationship between false alerts in Cook County’s electronic monitoring program and the built environment in Chicago. 

# Research Question: 

Is there a relationship between the rate of false alerts and zip codes with high building heights? 

Is the relationship between the rate of false alerts and zip codes with a high building density?

I will run a correlation analysis between the rate of false alerts and average building height and building density. I will also map these variables to analyze a potential spatial relationship.

# Data Overview:

## FEMA USA Structure Dataset: https://gis-fema.hub.arcgis.com/pages/usa-structures

* This dataset includes height and area measurements of all structures in the United States with a floor area of 450 square feet or more. 
* I created a dataset of all buildings within Chicago's city boundaries: each entry represents one of the 557,540 structures.

## False Alert by Zip Code: 

* This data was provided directly by the Cook County Sheriff's Office.
* Each record in the False Alert dataset represents a Chicago zip code, 56 in total. 
* This dataset includes three columns: 'Zip' (zip code), 'Total Alerts' (total alerts), and 'False Alerts' (false alerts per zip code). 
* I created a new column titled ‘False Alert Rate’: the number of false alerts divided by the total number of alerts. 

## Zip Code Shapefiles: https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Chicago-Zip-Code-and-Neighborhood-Map/mapn-ahfc

*  This data is available on the City of Chicago’s data portal. 
* It also includes the area of individual zip codes.

# Data Management Workflow 

My primary objective is to merge these datasets into a single dataset that organizes all data by zip code. I performed all of my work using the Pandas and Geopandas Python libraries. 

In the Structures dataset, 10,672 structures lacked zip codes, showing “null” values in that column. However, the structure data included latitude and longitude, which allowed me to spatially join the structures to the zip code shapefile. This filled the 10,672 null values with the correct zip code for those structures. I then organized this data by zip code, producing a dataset that included the average building height and area for each Chicago zip code. 

I am defining building density as the total building area per zip code divided by the zip code's area. I used the zip codes shapefile to determine each zip code's area, enabling me to calculate the average building density per square meter for each zip code. 

I then combined the structural and false alert data with the zip code shapefile using the zip code as a common key. This produced a geocoded dataset containing the average building height, density, and false alert rate for each Chicago ZIP code. 

# Presenting Results

## Rate of False Alerts and Building Height

(images/faz_height_map.png)

This map shows the relationship between the rate of false alerts by zip and the average building height in Chicago. 

There is a slight spatial pattern: false alert rates are high along the shore of Lake Michigan. These areas have a higher average building height, as many high-rise buildings line the lakefront. The zip codes with the highest average building height are in the downtown business district (the “Loop”), and zip codes farthest from the Loop have the lowest building height.

[FA and Building Height Scatterplot Here]

The evidence suggests a weak association between the rate of false alerts and building height.

The results of Spearman's correlation analysis between building height and the rate of false alerts yield a coefficient value of 0.2226, suggesting a weak, positive relationship between the two variables. 

 The analysis provided a p-value of .1092. This p-value is not statistically significant, suggesting no association between building height and the rate of false alerts.

## Rate of False Alerts and Building Density

[FA and Density Map Here]

This map shows the relationship between the rate of false alerts by zip and the average building height in Chicago. 

The zip codes with the highest building density are directly adjacent to the central downtown business district. The north and north-west sides of Chicago have higher building density than the south and south-west sides. There is a slight spatial pattern: the denser zip codes north of the loop also have higher false alert rates, but high false alert rates are not exclusive to those areas.

[FA and Density Scatterplot Here]

The evidence suggests a weak association between the rate of false alerts and building density.

The correlation analysis yields a Spearman’s rho of .1417, indicating a very weak, positive relationship between the variables. The  analysis also provided a p-value of .3115. This p-value is not statistically significant, suggesting no association between building density and the rate of false alerts.

# Conclusion

My analysis indicates a weak, positive relationship between the rate of false alerts and zip codes with a high average building height and high building density. 

However, further research is needed to understand why Cook County's Electronic Monitoring system has such a high rate of false alerts. Based on the data I received from the Sheriff’s Office, the minimum rate in a zip code was 90.9 percent. Even 60608, the zip code with the highest number of total alerts (n = 24,919), had a false alert rate of 98.37 percent. While there is something amiss with the Electronic Monitoring program, my research suggests that building height and density are unlikely to be the cause.



---

