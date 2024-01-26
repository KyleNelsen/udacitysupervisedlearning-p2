# Data Analyst Nanodegree
# Unsupervised Learning
## Project: Creating Customer Segments with Arvato

### Overview
This is my project for the Unsupervised Learning part of the Udacity Data Analytics Nanodegree. It involves wrangling some datasets and using Kmeans clustering to find segments of the population that are popular and unpopular with a mail-order sales company in Germany. The datasets were only allowed to be used for the project and had to be deleted afterwards.

### Files
- Data_Dictionary.md - Explains the datasets and columns

- Identify_Customer_Segments - all of the code

### Datasets
-Udacity_AZDIAS_Subset.csv: Demographics data for the general population of Germany; 891211 persons (rows) x 85 features (columns).

-Udacity_CUSTOMERS_Subset.csv: Demographics data for customers of a mail-order company; 191652 persons (rows) x 85 features (columns).

-AZDIAS_Feature_Summary.csv: Summary of feature attributes for demographics data; 85 features (rows) x 4 columns

### Steps
- Step 0 - Load Data
  Loaded datasets and explored them
- Step 1 - Preprocessing
  Assessed missing data
  Converted missing value codes to NaNs - used Feature_Summary.csv to find missing value codes in AZDIAS_Subset.csv and converted them to NaN's
  Assessed missing data in each column - removed outliers
  Assessed missing data in each row - created 2 subsets and use the subset with less missing values per row
  Re-Encoded Features - dropped multi-lvel features and re-enocded binaray feature with non-numerical values into numerical
  Engineered Mixed-Type Features - engineered 4 new columns out of 2 old columns. Dropped the 2 old columns
  Created a cleaning function - cleaning function allows to perform the same preprocessing on the customer data
  
- Step 2 - Feature Transformation
  Applied feature scaling - used standard scaler
  Performed Dimensionality Reduction - used Principal component analysis (PCA) to find the number of components to retain
  Interpreted Principal Components - made a function that prints the top features and their weights of a given component
  
- Step 3 - Clustering
  Applied Clustering to General Population - used the elbow method to determine the optimal number of clusters
  Applied all steps to Customer Data - applied all the steps I did on the general population data to the customer data
  Compared Customer Data to General Population - determined which segments of the population that are popular and unpopular with the company.
