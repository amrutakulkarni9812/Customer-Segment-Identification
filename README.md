![Alt text](https://www.kapturecrm.com/blog/wp-content/uploads/2017/02/b.1-1.jpg?raw=true "Customer Segmentation")
# Customer-Segment-Identification
In this project, I applied Unsupervised Learning technique such as Dimensionality reduction, Clustering to identify segments of the population that form the core customer base for a mail-order sales company in Germany.
## Installation
For running this project, the most important library is Python 3 version of Anaconda Distribution. It installs all necessary packages for the analysis and visualizations.
## Introducing the datasets
The datasets for this project are provided by Udacity's partners at Bertelsmann Arvato Analytics and represents a real-life data science task.
## File Description
### Readme
This file provides high level overview of the work done in project.
### Data
1. Udacity_AZDIAS_Subset.csv: Demographics data for the general population of Germany; 891211 persons (rows) x 85 features (columns).
2. Udacity_CUSTOMERS_Subset.csv: Demographics data for customers of a mail-order company; 191652 persons (rows) x 85 features (columns).
3. Data_Dictionary.md: Detailed information file about the features in the provided datasets.
4. AZDIAS_Feature_Summary.csv: Summary of feature attributes for demographics data; 85 features (rows) x 4 columns.
### Code
identify_customer_segments.ipynb consists of the code required to load, clean, explore, analyze and visualize the data.
### HTML Report
identify_customer_segments.html provides python notebook in html format.
## Project Motivation
The goal of this project is to help a mail-order sales company in Germany find its customer base from the general population.
These segments can then be used to direct marketing campaigns towards audiences that will have the highest expected rate of returns.
## Data Preparation
Missing data: The columns that had more than 30% missing values were dropped from the analysis. The rows with any missing values were removed from analysis but it was made sure that the distribution of most features was similar in the rows with and without any missing values. ategorical and mixed type features were cleaned and converted to binari values. Before dimensionality reduction, feature scaling was applied so that the principal component vectors are not influenced by the natural differences in scale for features. 
## Dimension Reduction and Clustering
I used sklearn's PCA class to apply principal component analysis on the data, thus finding the vectors of maximal variance in the data. I checked out the ratio of variance explained by each principal component as well as the cumulative variance explained and based on the findings, selected a value for the number of transformed features to retain for clustering. 
I used sklearn's KMeans class to perform k-means clustering on the PCA-transformed data, used scorings to determine number of clusters to retain and then refit the same k-means clustering to customer data as well. In the end, i compared the cluster distributions to see where the strongest customer base for the company is.
## Result
Based on the elbow rule, I decided to retain 30 principal components and 14 clusters. I also found out the characterisitcs that are most important to the mail-order company.
## Acknowledgement
Thanks to Udacity Data Scientist Nanodegree content creators for providing us the opportunity to work on this project.
