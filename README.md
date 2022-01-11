## Objectives
Build a predictive model to improve bike availability and reshuffling strategies across Washington DC \
Leverage existing bike share usage data through years to lower operational costs \
Improve user experience and sustain existing market share for client’s core business

## Assumptions
Assumptions:
Model does not take into account unpredictabilities during COVID pandemic

Reshuffling happens exactly halfway in time between a bike’s start trip and end trip disparities \
Starting number of bikes in each station is total number of bikes that arrived at each station in previous month and did not leave \
Weather data for a subset of stations is used to represent the overall weather for Washington DC area

## Data
Raw data: \
Dates: 2019 January 1st  ~ 2019 December 31st\
Historical and real time \
Each observation is a trip history of Capital Bikeshare bikes - the data includes: \
Duration \
Start Date \
End Date \
Start Station \
End Station \
Bike Number \
Member Type \
Having electric bikes or not, etc.\


Additional effort: \
Retrieved weather data of Washington DC from NOAA website: \
Precipitation \
Temperature \
Wind level \
etc…\

Utilized Capital Bikeshare’s API to retrieve
Longitude and latitude of each station
Total capacity of each station \




## Code

Data Preprocessing is done using Python in Jupyter Notebook for speed and efficiency in processing
- data_preprocessing_1.ipynb: First step of the data transformation stage using raw data.
- data_preprocessing_2.ipynb: Second step of the data transformation stage. 

The rest of the files are in R

- clustering.Rmd: uses hierarchical clustering using longitude and latitude of all stations, final selection of top 20 highest variance of availability stations, and all google map visualizations for clustering
- reshuffling_strategy.Rmd: generates plots for reshuffling patterns and availability trends. Also fits a logistic regression model to compare relationship between availability proportion and the odds of reshuffling (Yes vs No).
- model.Rmd: generates more columns, samples data and fits both Random Forest model and Logistic Regression model to the data and compare their confusion matrix of the Actual and the Predicted



