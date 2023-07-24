# Quality classification of molded products via Machine Learning and Control Theory

## Table of contents
* [Introduction](#introduction)
* [Technologies](#technologies)
* [Solution](#solution)
* [Results](#results)
* [Author](#author)

## Introduction

This work addresses the challenge of predicting the quality of molded plastic products in a manufacturing setting through the application of machine learning and control theory techniques. The goal is to develop a model capable of accurately classifying the quality of molded products based on production process parameters, using real data from in-line industrial measurements. The dataset utilized in this study originates from a plastic products manufacturing company and comprises four quality classes: Waste, Acceptable, Target, and Inefficient.

## Technologies

The project has been completed using Python and Jupyter Notebook, with the following libraries utilized:
* numpy
* matplotlib.pyplot
* pandas
* seaborn
* sklearn
* xgboost
* pykalman

## Solution

First of data analysis stage was conducted, where standardizing and normalizing of data were applied and existence of linear correlations and importance of features for tree-based algorithms have been checked. Based on this information 8 different datasets were buided:
* Standardized data
* Normalized data
* Standardized data without strong correlations
* Normalized data without strong correlations
* Standardized data without not important features for tree-based algorithms
* Normalized data without not important features for tree-based algorithms
* * Standardized data without both strong correlations and not important features for tree-based algorithms
* Normalized data without both strong correlations and not important features for tree-based algorithms


Then, various machine learning techniques are employed and compared:
* Classification models, including Logistic Regression, Ridge Classifier, Decision Trees, Random Forest, Gradient Boosting, XGBoost, SVM Classifier, and K-Nearest Neighbors (KNN).
* Regression models; Linear Regression, Polynomial Regression, Ridge Regression, Lasso Regression, Decision Tree Regressor, Random Forest Regressor, Gradient Boosting Regressor, XGBoost Regressor and SVM Regressor, with rounding predicted values to closest integer to use them for classification task.
* Control theory algorithms: PCA-based algorithm with a Kalman filter and a Random Forest Classifier, same algorithm with an entropy-based feature selection and RT-based algorithm that leverages a tree growth process followed by SVM Regression for dataset partitioning at each leaf node.


## Results

Between regression models,the best algorithms are tree-based algorithms, especially ensembles algorithms! And the best achieved accuracy is 95.88% by XGBoost gradient boosting implementation on normalized data set with following parameters of model. 

Between classification models, also the tree-based algorithms, especially ensembles algorithms giving best results! Here the top achieved accuracy is 95.53% by scikit learn gradient boosting implementation on normalized data set without not important features with next parameters.

In control theory algorithms, the entropy-based feature selection improved result of PCA-based algorithm. But at all there are bad results and it was expected, because for this algorithm data should be time sequenced, it is not like that.

## Author
Danylo Savchak
[daniel.savchak@gmail.com](mailto:daniel.savchak@gmail.com)

