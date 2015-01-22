# GETTING AND CLEANING DATA - course project

This codebook describes:  
1. General definitions for the dataset 'TidyData.txt'  
2. Data and variabls contained in the dataset  
3. Transformations performed to clean up the data  

## General definitions for the dataset 'TidyData.txt'  
This dataset contains a summary from the original data, focused on the averages of a set of features (the ones related to means and standard deviations). It contains 40 records, each one representing a valid combination for 'individual' and 'activity'.

The file contains headers and the columns are separated by tabs (sorry for not using comma separated values, but it doesn't work well in my computer, since it runs Windows in Portuguese and interprets ',' as '.'!)

## Data and variables contained in the dataset  
The dataset has 3 'identification' columns that defines the groups and 66 'numeric values' columns.   

The 3 'identification' columns are:  
* individual: identification of the indidividual subject to the measures (30 distinct individuals, coded from 1 to 30)
* act_id: code for the type of activity being measured (6 distinct types, coded from 1 to 6)
* act_label: description for the type of activity

The 66 'numeric values' columns contain the mean values per grupo (individual x activity) for 66 features in the original data. The 66 selected features are the ones which contain the strings 'mean' or 'std' (lower case, except for 'meanFreq') in its name, according to the definition in the project item 2 ('Extracts only the measurements on the mean and standard deviation for each measurement')

These 66 columns are labeled according to the original data (tBodyAcc.mean...X, tBodyAcc.mean...Y, fBodyBodyGyroMag.std.., etc)


## Transformations performed to clean up the data
The R script is structured as follows:  

1. Loading and processing the data:  
a) Load auxiliary data for the training and test sets (features and activity labels)  
b) Load and process the training data set (merges individual + activity + features with column names)  
c) Load and process the testing data set (merges individual + activity + features with column names)  
d) Make a full data set (binding training and test datasets)

2. Creating the datasets demanded in the project definition:  
a) Extracts only the measurements on the mean and standard deviation for each measurement (item 2)  
b) "Tidy dataset" (item 5)
