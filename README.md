# TTC Delay Predictor

## Overview:
- Subway delays are a major inconvenience for Toronto commuters, affecting travel time and overall transit efficiency. This project aims to build a regression model to predict subway delays based on factors such   as time of day, station location, and train line. By identifying key patterns in delay occurrences, we can provide actionable insights to improve transit operations and commuter experience.

## Stakeholders & Impact:
- **Toronto Transit Commission (TTC), City Planners:** This project will help TTC/city planners optimize schedules, deploy resources effectively, and improve service reliability through data-driven decision making.
- **Local Businesses:** This project will allow businesses near transit hubs to adjust schedules based on predicted delays as it would lead to more productive employee performances driving down costs. It would also allow businesses to import/export goods/services more efficiently driving down business costs.
- **Commuters:** Delays impact work, school and appointments of transit users. This project will provide real-time insights into transit delays so commuters can plan accordingly reducing stress and driving up productivity.
- **Environmental Policy Advocates:** Public transit delays push people toward private cars, thus increasing emissions. This project can support policies aimed at improving public transport reliability and usage of TTC.

## Transit Delays versus Society: 
- **Social Impact**:
Subway delays increase commuter stress, leading to dissatisfaction with public transit. People who rely on the TTC for work, school, and appointments experience daily disruptions. Unreliable service can push riders toward other transportation options, reducing trust in the system.
- **Economic Impact**:
Transit delays reduce workplace productivity as employees arrive late or miss important meetings. Businesses near subway stations may also suffer revenue losses if delays discourage foot traffic. A poorly functioning transit system can weaken a city's overall economic efficiency.
- **Environmental Impact**:
Frequent delays push commuters toward personal vehicles, increasing traffic congestion and carbon emissions. This shift away from public transportation contributes to pollution and makes urban areas less sustainable. A more reliable subway system encourages people to choose eco-friendly transit options.
- **How This Project Aims to Help**:
Our machine learning model predicts subway delays, allowing transit authorities to take proactive measures. Identifying high-delay periods helps optimize train schedules, reducing disruptions. These insights can improve the overall commuter experience, making public transit a more attractive and efficient choice.

## Research Question:
- Can we predict the average delay (Min Delay) of Toronto transit vehicles based on factors like time of day, station location, and train line?

## Dataset:
- Source: Open Toronto Data - TTC Subway Delay Data
- Description: The dataset from Open Toronto covers TTC subway delays from 2017-2025. The dataset includes historical subway delay records, including details on station, time, line, delay reason, and duration. The dataset has missing values, inconsistent station names, and lacks real-time external factors like weather and special events.
- Dataset Limitations: no real-time tracking, station-based delays and duration inconsistencies
  
## Key Features Used:
- Time Period: Time of the delay occurrence.
- Station: The affected subway station.
- Line: Subway line affected.
- Min Delay: Duration of the delay (target variable).
- Cause: The reason for the delay.

## Project Objectives:
- Data Cleaning & Preprocessing 
- Handle missing values and outliers.
- Convert categorical data into numerical format.
- Standardize numerical features.

## Exploratory Data Analysis (EDA):
- Identify trends and patterns in subway delays.
- Visualize peak delay times and affected stations.
- Determine the most influential factors causing delays.

## Regression Model Development:
- Train and evaluate multiple models:
  - Linear Regression
  - Random Forest Regressor
  - Gradient Boosting Regressor
- Select the best-performing model based on Mean Squared Error (MSE) and R² score.

## Business Impact Analysis:
- Identify critical time periods and stations for delay occurrences.
- Estimate potential cost savings from reducing delays.
- Provide insights for TTC and city planners to improve transit efficiency.

## Results
- The best-performing model was [model name], with an R² score of [R² value].
- Peak delay times were observed during morning (7-9 AM) and evening rush hours (5-7 PM).
- The most affected stations were [Top 3 stations].
- Delay reasons such as [most common delay reasons] had a significant impact.
- Estimated cost of subway delays per occurrence: $[estimated cost].

## Output files:
- Model performance results: model_results.csv
- Business impact report: business_analysis.txt

## Business Impact Summary:
- Transit Scheduling Improvements: Predictive insights can help optimize subway schedules during peak hours.
- Infrastructure Planning: Identifying problematic stations helps prioritize maintenance and upgrades.
- Economic Benefits: Reducing delays can save operational costs and improve commuter satisfaction.

## Future Work:
- Integrate real-time delay prediction using live data feeds.
- Improve model accuracy with additional external factors (e.g., weather, special events).
- Develop a web dashboard for interactive delay forecasts.

## Contributors:
- Chinyere Johnson
- Tian Qin
- Faraz Shahid
- Joey Poh
- Peeu Banerjee

## References:
- Open Toronto Data - TTC Subway Delay Data: https://open.toronto.ca/dataset/ttc-subway-delay-data/
- Scikit-learn documentation: https://scikit-learn.org/
