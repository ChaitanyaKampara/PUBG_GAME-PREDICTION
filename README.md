# PUBG_GAME-PREDICTION
# Introduction
In this Project to predict the outcome of a game we need to train our model on a large dataset containing all various parameters of a game or information of a player like the guns he used, average headshot rate, his group rank etc. The datasets we are going to use 29 features. These 29 features along with the output of the game will be provided to train the model. 
# Data Wrangling
Data wrangling is the process of cleaning, organizing, and preparing d ata for analysis. In the context of the PUBG win prediction model, data wrangling would involve several steps to ensure that the data is in a usable form for the machine learning model.
Some of the data wrangling tasks that might be performed include:
* Removing any unnecessary or irrelevant columns from the dataset
* Handling missing values in the data (e.g. imputing missing values, dropping rows with missing values)
* Converting categorical data, such as the type of equipment a player used, into numerical form (e.g. using one-hot encoding)
* Splitting the data into training and testing sets
# Feature Engineering
Feature engineering is the process of creating new features or modifying existing features in a dataset in order to improve the performance of a machine learning model. In the context of the PUBG win prediction model, feature engineering might involve creating new features based on existing data or transforming existing features in a way that makes them more useful for the model.
This might include:
* Normalizing the features.
* Dropping unnecessary features which would only lead to increase in models complexity
* Creating features based on combinations of existing features
* Creating a new feature that represents the total number of kills a player made in a game, by summing up the number of kills made with each type of weapon.
# CatBoost Model

Let’s first take a look at why we chose the CatBoost Model for this dataset. 
* CatBoost is effective for working with categorical data:
  The PUBG game includes a number of categorical features, such as the type of equipment a player used or the location on the map where a player was killed. CatBoost is particularly effective for handling categorical data, as it can automatically encode the categories as numerical values and handle missing values.
* CatBoost is fast and easy to use:
 Training a CatBoost model is typically fast, and the library includes a number of built-in features that make it easy to use, such as automatic handling of missing values and support for parallelization. This can make it a good choice for quickly prototyping and testing models.
* CatBoost is a powerful and accurate algorithm:
 In general, gradient boosting algorithms like CatBoost are known to be powerful and accurate, and they have been successful in a number of machine learning competitions. This makes them a good choice for many types of problems.

Given the characteristics of the PUBG game data and the strengths of the CatBoost algorithm, it is good to consider using CatBoost for this type of problem.
After using CatBoost model for our dataset we can predict the performance using RMSE

# Libraries Used In This Project:
* working :
numpy 
pandas <br>
* visualisation :
matplotlib
seaborn
StandardScaler <br>
* model :
catboost  <br>
* Metrics :
mean_squared_error
r2_score
