# Stroke-Prediction

Using a dataset containing patient attributes, I will attempt to model and predict the occurance of strokes in the patient using R. Initially, I will only be using the SVM polynomial kernel. Further itterations will make use of different approaches.  

This stroke prediction dataset contains 5110 observations with 12 attributes. As mentioned previously, one of these attributes will be our response variable, i.e., whether the patient suffered a stroke or not. The attributes contained have both categorical and numerical values. A full description of all variables can be seen below:
1.	ID (categorical): Unique identifier
2.	Gender (categorical): “Male”, “Female”, or “Other”
3.	Age (numerical): Age of the patient
4.	Hypertension (categorical): 0 if the patient does not have hypertension and 1 if the patient does
5.	Heart Disease (categorical): 0 if the patient does not have any heart diseases, 1 if the patient has a heart disease
6.	Ever Married (categorical): “Yes” or “No” 
7.	Work type (categorical): "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
8.	Residence (categorical): “Urban” or “Rural”
9.	Average Glucose (numerical): Average glucose level in blood
10.	BMI (numerical): Patient body mass index
11.	Smoking (categorical): "formerly smoked", "never smoked", "smokes" or "Unknown"
12.	Stroke (categorical): Dummy variable, 0 if the patient never had a stroke, 1 if the patient has had a stroke. This will be our response variable.

One of the biggest challenges in this dataset is the heavy classs imbalance (~1:20). This means that sampling approaches such as oversampling, undersampling and/or SMOTE will be required. This of considerable importance as we are dealing with a medical diagnosis situation and it is desirable to reduce the false negatives as much as possible.

Libraries used:

library(data.table)
library(mltools)
library(e1071)
library(ggcorrplot)
library(MLmetrics)
library(caret)
library(kernlab)
library(themis)
