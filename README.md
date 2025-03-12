# Predicting TTC Subway Delays Using Machine Learning

## Overview
- Subway delays are a major inconvenience for Toronto commuters, affecting travel time and overall transit efficiency. This project aims to build a regression model to predict subway delays based on factors such   as time of day, station location, and train line. By identifying key patterns in delay occurrences, we can provide actionable insights to improve transit operations and commuter experience.

## Research Question
- Can we predict the average delay (Min Delay) of Toronto transit vehicles based on factors like time of day, station location, and train line?

## Dataset
- Source: Open Toronto Data - TTC Subway Delay Data
- Description: The dataset includes historical subway delay records, including details on station, time, line, delay reason, and duration.

## Key Features Used:
- Time Period: Time of the delay occurrence.
- Station: The affected subway station.
- Line: Subway line affected.
- Min Delay: Duration of the delay (target variable).
- Cause: The reason for the delay.

## Project Objectives
- Data Cleaning & Preprocessing
- Handle missing values and outliers.
- Convert categorical data into numerical format.
- Standardize numerical features.

## Exploratory Data Analysis (EDA)
- Identify trends and patterns in subway delays.
- Visualize peak delay times and affected stations.
- Determine the most influential factors causing delays.

## Regression Model Development
- Train and evaluate multiple models:
  - Linear Regression
  - Random Forest Regressor
  - Gradient Boosting Regressor
- Select the best-performing model based on Mean Squared Error (MSE) and R² score.

## Business Impact Analysis
- Identify critical time periods and stations for delay occurrences.
- Estimate potential cost savings from reducing delays.
- Provide insights for TTC and city planners to improve transit efficiency.
