# Arvato-Project-
Customer Segmentation Report for Arvato Financial Services

## Table of Contents

- [Project description and Motivation](#projectoverview)
- [Data](#data)
- [Project](#project)
- [Requirements](#requirements)


<a id='projectoverview'></a>
## Project description and Motivation
It is really important to know who are your customers. First of all it helps you to understand their needs and their special characteritics. Furthermore it is easier for you to attract new customers with similar characteristics as the ones you already have.

In this project, we will analyze demographics data for customers of a mail-order sales company Arvato in Germany, comparing it against demographics information for the general population.

### Problem Statement
“Given the demographic data of a person how can a mail order company acquire new customers”
In the first part of the project, we will use unsupervised learning techniques to perform customer segmentation, identifying the parts of the population that best describe the core customer base of the company.
Then, we’ll apply what you’ve learned on a third dataset with demographics information for targets of a marketing campaign for the company, and use a model to predict which individuals are most likely to convert into becoming customers for the company.

### Evaluation metric

The prediction will be evaluated in a Kaggle Competition. Due to the fact that the labels are highly imbalanced, the evaluation metric that has been used is the AUC for the ROC curve. The AUC considers both the true positive rate and the false positive rate. A ROC, or receiver operating characteristic, is a graphic used to plot the true positive rate (TPR, proportion of actual customers that are labeled as so) against the false positive rate (FPR, proportion of non-customers labeled as customers). We can check in the plot below how imbalanced are the 2 classes.

![download (14)](https://user-images.githubusercontent.com/18635146/112768680-cd733000-9025-11eb-87f1-527de1863efe.png)


<a id='data'></a>
## Data 
The data has been provided thanks to Arvato Financial Services and Udactity. 

4 datafiles has been used for the analysis:  
- Customer Segmentation
  - General Population demographics
  - Customer demographics
- Customer Acquisition
  - Training/Test datasets

<a id='project'></a>
## Project 

Arvato Project Workbook.ipynb
* Part 0: Get to Know the Data
  * Data Exploration and Cleaning
  * Feature Engineering
* Part 1: Customer Segmentation Report
  * Dimensionality Reduction
  * Clustering
* Part 2: Supervised Learning Model
  * Supervised Learning
  * Model Evaluation
  * Predictions on Test data
* Part 3: Kaggle Competition

### Project report
Project report could be found in [medium](https://evangelou-alexandr.medium.com/customer-segmentation-for-arvato-financial-services-43e92159f1c).

## Results
The cyustomer segmentation completed by building an unsupervised model with the use of PCA and k-means clustering. We did that by using 200 components and 11 clusters. After applying these approaches I could compare the over-represented and the underrepresented clusters and draw some conclusions. For example, I noticed that the majority of individuals of the over-represented group have high income and have a high social status. 

For the second part of the project I built a couple of different supervised learning models like xgboost and catboost and compare them. With The Cat Boosting algorithm I had the best ROC AUC score and because of that it was selected and tuned. I end up with a score of 0.79813 on the test data.

![download (22)](https://user-images.githubusercontent.com/18635146/112768898-f7792200-9026-11eb-8caa-908d9f2a9e15.png)

All the results have been  documented in the notebook Arvato_Project_Workbook.ipynb.

<a id='requirements'></a>
## Requirements

All the package requirments are at the `requirements.txt`. For install run `python install -r requirements.txt`.
