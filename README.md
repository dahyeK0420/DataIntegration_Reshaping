# Data Cleansing and Pre-processing

This program aims to collect data regarding features of properties in a dataset. The features include the suburb the property is located at, shortest distance to areas such as supermarket, train stations, shopping centres, and hospitals. It also includes the travel distance to the CBD Melbourne via the nearest station retrieved from given dataset. After completing the data set on the property, the program builds a model to predict the property price basd on its linear relationship with continuous variables in the dataset. The model aims to evaluate whether the property is overpriced in respect to its surrounding environments and features.

## 1. Prepare for Dataset of Real Estate by Parsing various Data Sources

* ``real_estate.json``: involves half of the dataset regarding the properties 
* ``real_estate.xml``: other half of the dataset regarding the properties 

## 2. Add Additional Attributes for Modelling - Calculating the Distance between the Property and each Landmark 

Four locations are considered for each property - supermarket, shopping centre, hospital, and train station. The information on the geographical coordinate and its ID are given in different formats, and thus they are all parsed using different libraries and functions. The distiance between the properties and aforementioned landmarks is calculated using Haversine Distance 

* ``hospitals.pdf``: dataset on the hospital ID and geographical coordinate of the hospitals in Victoria
* ``supermarkets.xlsx``: dataset on the supermarket ID and geographical coordinate of supermarkets in Victoria
* ``shoppingcenters.html``: dataset on the shopping centres ID and geographical coordinate of shopping centres in Victoria

## 3. Determine the Suburb each Property is Located at 
The information regarding suburbs in the region is stored as geographical shape file. To parse these data into a readable data frame, I used shapefile library. All the files with ``VIC_LOCALITY_POLYGON`` heading are utilised for this task 

## 4. Determine the Nearest Train Station to the Property and the Relevant Travel Itineraries 

## 5. Data Reshaping 
This part of the program prepares the dataset to be processed for a linear regression model for property price prediction. In order to apply the dataset for the modelling process, the attributes should first satisfies the *linearity*, *normality*, and *independence* assumptions. This part of the program reshapes the dataset for *linearity* and *normality* assumptions. This also includes MinMax/Standard scaling process for each feature. 

