
# False Alerts in Cook County’s Electronic Monitoring System

**Date:** June 2024  
**Tools:** Python | Pandas | GeoPandas

## Overview
[2-3 sentence description of what this project was about and what you created]

## Skills Demonstrated
- [Skill 1]
- [Skill 2]
- [Skill 3]

Research Question:
My project aims to study potential associations between electronic monitoring false alerts and Chicago's built environment.

Electronic monitoring is a form of remote surveillance law enforcement uses as an alternative to incarceration: a person on house arrest may be tracked via a GPS ankle monitor, for example. However, GPS has limitations that can affect the accuracy of its monitoring: GPS signals are compromised by interference in densely built-up urban areas. This can lead to 'false alerts', when a GPS error makes it seem like a person is breaking the terms of their home arrest, even though no violation occurred. There are reports that false alerts have caused rule-following supervisees to be harassed by law enforcement.

I will measure the rate of false alerts by zip code. Is there a relationship between the rate of false alerts and zip codes with high building heights? Is the relationship between the rate of false alerts and zip codes with a high building density?

Through my code, I will run a correlation analysis between the rate of false alerts and average building height and building density. I will also map these variables to analayze a potential spatial realtionship.

Data Overview:
I am using two main datasets for this project. My Electronic Monitoring False Alert data comes from the Cook County Sheriff's Office, and my Chicago building structure data comes from the FEMA USA Struture Data Set. I will also be using a shapefile of Chicago's Zip codes in order to map the data.

FEMA USA Structure Data Set: https://gis-fema.hub.arcgis.com/pages/usa-structures
FEMA's USA Structures dataset is a comprehensive inventory of all structures larger than 450 square feet. From this data, I created a dataset that only includes the structures in Chicago.
Each instance in this data set is a structure: there are 557,540 structures in Chicago.
The main fields of intrest are "HEIGHT" and "SQ METERS". "HEIGHT" is the individual height for each building, and "SQ METERS" is the individual building size. All measurements are in meters.
I am defining building density as the sum of the total building size per zip code divided by the area of the zip code.
According to the FEMA ArcGIS page, the USA Structures data was collected in 2021 and last updated on April 23, 2025.
False Alert by Zip Code:
The False Alerts by Zip Code data come directly from the Cook County Sheriff's Office.
Each instance in the False Alert dataset is a Zip Code: 164 instances.
The False Alert data set only contains three columns: 'Zip' identifies the Zip Code, 'Total Alerts' is a count of all alerts that took place in the Zip Code, and 'False Alerts' is the number of alerts in a zip code determined to be false.
The False Alerts data collected the total number of alerts and false alerts between January 2022 and November 2023.
Workflow Overview
My primary goal is to merge the Chicago Structures, False Alert by Zip Code, and Zip Code Shapefiles into a single dataset organized by zip code. The False Alert by Zip Code and Zip Code Shapefiles are already organized by zip code, so the majority of my work is focused on organizing the Chicago Structures dataset.
10,672 structures did not have an assigned zip code; they contained “null” values in the zip code column. However, since the structural data does contain the latitude and longitude of these structures, I was able to join these structures to the zip code shapefile table spatially.
After the null zip codes were updated, I was able to organize the structural data by zip code.
I was able to find the area of the Zip Codes by using the Zip Codes shapefile, which allowed me to find the average building density per square meter for each zip code. I was then able to combine the structural data and false alert data to the zip code shapefile by using the zip code as a common key.
I then was able to run a correlation analysis and map the geospatial data.


## Outputs
[Include maps, charts, or other visual products here]

![Map/Figure Title](../images/project-name-map.png)

## Challenges & Solutions
[Optional: What problems did you encounter and how did you solve them?]

## Code/Data
[Optional: Link to GitHub repo, data sources, notebooks, etc.]

---

