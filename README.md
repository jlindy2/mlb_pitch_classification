# MLB Pitch Classification
### By: Jeff Lindberg

## Executive Summary
The goal of this project was to find a way to classify pitches from the MLB using machine learning alogorithms. Initial testing was broken down into 2 classes to reduce complexity, but re-tested with 3 classes to verify model accuracy. The best model was a Random Forest algorithm. This also allowed me to determine the most import features used to classify the data. These features can be used by teams when evaluating pitchers and creating scouting reports. It can also be used to train pitch recognition for hitters and to develop pitches for pitchers. 

## Contents
1. [Introduction](#introduction)
    - [Problem Statement](#problem_statement)
    - [Dataset](#dataset)
2. [Analysis](#analysis)
    - [Data Cleaning](#data_cleaning)
    - [Exploratory Analysis](#exploratory_analysis)
    - [Modeling](#modeling)

## Introduction <a name="introduction"></a>

### Problem Statement <a name="problem_statement"></a>
As a hitter, it is difficult to differ between offspeed and breaking ball pitches coming from a pitcher. Can we find significant features of these pitches that can be seen from the hitter's perspective?

### Dataset <a name="dataset"></a>
The analysis is based on a dataset from Kaggle (https://www.kaggle.com/pschale/mlb-pitch-data-20152018#pitches.csv), scraped from MLB.com, that includes all pitches from 2015-2018. The observations include all the metrics recorded by Trackman for each pitch. The size of my initial dataset was (2867154, 40).

## Analysis <a name="analysis"></a>

### Data Cleaning <a name="data_cleaning"></a>
The inital data set was fairly clean but I still had to drop some outliers and null values. I sorted the data by year and dropped all pitches before 2018 to reduce the size of my dataset. I dropped unnecessary columns and dropped a few pitch types that distorted the data. Then I binned the remaining pitches into three classes, offspeed, breaking, and fastball variations. After all the cleaning, the size of my dataset was (381485, 24).

### Exploratory Analysis <a name="exploratory_analysis"></a>
I used exploratory analysis to see the relationship between my features and targets. This helped me drop some unnecessary features that were not continuous variables. Most of the features were normally distributed. 

### Modeling <a name="modeling"></a>
The majority of the modeling in this project came from sklearn. I used Logistic Regression, Multinomial Naive Bayes, Random Forest, XG Boost, AdaBoost, and K-Nearest Neighbors.
