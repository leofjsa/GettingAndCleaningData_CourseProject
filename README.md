# Understand this repo
There are 2 important files in this repo (in addition to this "readme.txt"):  
* CodeBook.md:  
* run_analysis.R:  

The file CodeBook.md describes:  
1. General definitions for the dataset 'TidyData.txt'  
2. Data and variabls contained in the dataset  
3. Transformations performed to clean up the data  

The run_analysis.R contains all the R scripts used to perform the analysis.  
This script assumes that the data is available and unziped in a folder called "UCI HAR Dataset" in the working directory.

The R script is structured as follows:  

1. Loading and processing the data:  
a) Load auxiliary data for the training and test sets (features and activity labels)  
b) Load and process the training data set (merges individual + activity + features with column names)  
c) Load and process the testing data set (merges individual + activity + features with column names)  
d) Make a full data set (binding training and test datasets)

2. Creating the datasets demanded in the project definition:  
a) Extracts only the measurements on the mean and standard deviation for each measurement (item 2)  
b) "Tidy dataset" (item 5)