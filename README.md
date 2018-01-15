# Data-Mining-Approach-to-Identify-Air-Quality-Profiles-in-USA

A data mining approach to identify the distinct multi-pollutant air quality profiles within the US


## Data Collection

In this project, we manually extract the historical data from the EPA Air Quality Data
via Google Cloud Platform queries reporting criteria chemical pollutants readings and ambient
weather conditions.


## Data Processing

1. Extract the mean value of each pollutant on the same day at the same site.

2. Create a new column for each measured variable in the joint dataset with the most
frequently used unit of measure to ensure each variable has only one standard unit.

3. Remove the rows/instances that have pollutants of which the sampling period is shorter
than 8 hours since the time resolution for the final dataset is 1 day.

4. Finally, after the previous update the team has realized that there are still significant
amount of duplicated rows existed in the final subset and this is largely due to that the meteorological
factors are generally reported multiple times per day per site.We further calculated
the daily average meteorological conditions for each site.


## Methods

We mainly focused on prototyped-based clsutering methods in this project: Both K-means
and K-medoids have been implemented and compared. 

PAM (Partition Around Medoid) as the most common algorithm for Kmediods have been chosen for demonstrative purpose.

Furthermore, from the correlation result, as there are some correlations exhibited between the variables which suggest
that the spherical assumption might not stand, hence Hierarchical and Distribution-based are also the candidates for model selection.

For the Site-specific analysis, another variation of K-means - K-medians has also been compared against other algorithms.

