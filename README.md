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

## Questions We Are Trying to Answer: 
- What times of the day have the longest delays?
- Which subway lines/stations are most affected?
- How predictable are delays based on historical trends?
- Can machine learning provide accurate delay forecasts?
  
## Dataset:
- Source: Open Toronto Data - TTC Subway Delay Data
- Description: The dataset from Open Toronto covers TTC subway delays from 2017-2025. The dataset includes historical subway delay records, including details on station, time, line, delay reason, and duration. The dataset has missing values, inconsistent station names, and lacks real-time external factors like weather and special events.
- Dataset Limitations: no real-time tracking, station-based delays and duration inconsistencies

 ## Risks & Uncertainties:
- Like any data-driven project, this model comes with challenges. One major risk is data gaps and inaccuracies—some delays might be underreported or missing, which could impact the reliability of our predictions. Additionally, the dataset has a limited scope, as it doesn’t account for external factors like weather, accidents, or labor strikes, all of which can significantly impact subway delays. Another challenge is changing transit patterns like the COVID-19 pandemic, new subway expansions, or shifts in commuter behavior could make historical data less predictive of future delays.
- To address these uncertainties, we’ll focus on data cleaning and validation to handle inconsistencies and ensure accuracy. Feature engineering will play a key role in making our model more robust by identifying patterns even within an imperfect dataset. In the future, we may integrate external data sources like weather reports and real-time transit feeds to enhance prediction accuracy and make the model even more useful for riders and transit authorities alike.

## Key Features Used:
- Time Period: Time of the delay occurrence.
- Station: The affected subway station.
- Line: Subway line affected.
- Min Delay: Duration of the delay (target variable).
- Cause: The reason for the delay.

## Project Objectives:
## 1. Develop an Accurate Subway Delay Prediction Model
- Build a machine learning regression model to predict average subway delay times (in minutes) using historical TTC subway delay data.
- Compare different regression models, starting with a baseline Linear Regression model, and explore advanced techniques like Random Forest Regressor or deep learning.
- Optimize model performance using hyperparameter tuning to improve prediction accuracy.
  
## 2. Analyze Key Factors Affecting Subway Delays
- Investigate how factors such as time of day, station location, and train line influence subway delays.
- Perform feature importance analysis to determine which variables contribute most to delays.
- Conduct error analysis to identify and mitigate common sources of prediction errors.

## 3. Ensure High-Quality Data Processing & Preparation
- Perform data cleaning, including handling missing values, standardizing station and train line names, and converting time fields into meaningful numerical/categorical features.
- Engineer new features such as rush hour indicators, day of the week, seasonal trends, and location-based encoding to enhance predictive power.
- Normalize numerical variables and encode categorical variables for improved model performance.

## 4. Evaluate and Validate Model Performance
Assess model accuracy using key performance metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared (R²).
Compare model results against the baseline model to determine performance improvements.
Use cross-validation techniques to ensure model generalizability across different time periods and conditions.

## 5. Visualize and Interpret Model Findings
- Generate data visualizations to illustrate subway delay trends by station, time of day, and train line.
- Compare actual vs. predicted delay distributions to validate model effectiveness.
- Present findings in a clear and interpretable manner for stakeholders, enabling informed decision-making.

## 6. Document Methodology and Findings
- Compile a comprehensive project report detailing the methodology, findings, and recommendations.
- Prepare a presentation summarizing the project’s key insights and predictive outcomes.

## 7. Lay the Foundation for Future Enhancements
- Identify potential areas for improvement, such as incorporating real-time transit data, weather conditions, or passenger load data for more accurate predictions.
- Discuss possible deployment strategies to integrate the model into TTC’s operational decision-making systems.

## 8. Business Impact Analysis:
- Identify critical time periods and stations for delay occurrences.
- Estimate potential cost savings from reducing delays.
- Provide insights for TTC and city planners to improve transit efficiency.

## Dataset Cleaning: 
During the data cleaning process, several steps were taken to ensure data consistency and reliability. First, missing values in numerical columns, "Min Delay" and "Min Gap", were imputed with the average values for the corresponding "Station" to maintain accurate delay estimates. Rows with missing values in essential categorical columns, such as "Station", "Date", "Time", and "Day", were removed to preserve data integrity. For categorical fields, missing values in "Code" were replaced with the most common delay reason associated with the respective "Station", while missing values in "Bound" (train direction) and "Line" (subway line) were replaced with their most frequent values for the corresponding "Station" to maintain consistency. Additionally, rows where the "Vehicle" column was missing were removed to ensure that every record had a valid vehicle number.

To resolve inconsistencies, "Station" names were standardized based on actual TTC subway station names, while bus stops were mapped to their correct street intersections. Non-standard TTC names that did not represent actual subway stations or bus stops were identified and removed to prevent errors in analysis. The "Bound" column was also corrected by removing non-standard or incorrect train directions that did not align with TTC's defined data standards. Similarly, the "Line" column was cleaned by removing any entries that did not correspond to an actual TTC subway line.

Furthermore, outliers above the 99th percentile in numerical columns were detected and removed to prevent skewed results. Duplicate records were also identified and eliminated to ensure the dataset did not contain redundant data points. The "Vehicle" column was checked for inconsistencies, and any values that were zero, negative, or non-numeric were removed. The "Date" and "Time" columns were also reviewed for consistency, ensuring they followed the correct format and contained valid timestamps.

These comprehensive cleaning steps enhanced data quality, removed inconsistencies, and ensured that the dataset was accurate, structured, and suitable for analysis and predictive modeling.


## Model Evaluation and Analysis:

The following models were trained and evaluated:
1.	Linear Regression (Baseline model)
2.	Random Forest Regressor (Improved model)
3.	Optimized Random Forest (Tuned for best performance)
4.	XGBoost Regressor (Gradient boosting alternative)
5.	Stacking Model (Combining Random Forest and XGBoost)

Performance was evaluated using:
•	Mean Absolute Error (MAE)
•	Mean Squared Error (MSE)
•	R² Score

Feature Importance Analysis
•	Random Forest and XGBoost feature importances were compared.
•	Important features included previous delays, time of day, and rolling averages.

Residual Analysis
•	Examined model errors and residual distributions.
•	Identified high-error cases and potential biases in predictions.

3. Findings and Insights
Model Performance Comparison
Model	MAE	MSE	R²
Linear Regression	1.25	10.48	0.86
Random Forest	0.38	8.55	0.88
Optimized RF	0.37	7.97	0.89
XGBoost	0.42	10.76	0.86
Stacked Model	0.41	9.20	0.88 

•	The Optimized Random Forest performed the best, achieving the lowest MAE and highest R².
•	XGBoost had competitive performance but slightly underperformed Random Forest.
•	The stacking model showed improvements in some cases but added complexity.


## Results:
- !(https://github.com/user-attachments/assets/fbd514bb-ecb5-416b-ab2f-409c60477afa)
*Figure 1: Line graph showing the Trend of Average Delay Time Over the Years.*

- The best-performing model was Optimized Random Forest, with an R² score of 0.89, MSE of 7.97 and MAE of 0.37.

![image](https://github.com/user-attachments/assets/b05538a0-1a69-4018-a453-f3a729f759e2)
*Figure 2 showing the comparison of models.*
 
- Peak delay times were observed during morning (7-9 AM) and evening rush hours (5-7 PM).
  
![image](https://github.com/user-attachments/assets/8bac6f97-8457-45dc-a09c-961e41f02d1d)
*Figure 3 showing Heatmap Delays by Hour and Day.*

- The most affected stations were Kennedy, Kipling and Finch station.


- The minimum gap had a significant impact.
![image](https://github.com/user-attachments/assets/db9526b7-bf27-4017-864a-619eff4c1d6e)

  
- Estimated cost of subway delays per occurrence: $[estimated cost].

- Actual vs predicted delays (using the best model: Optimized Random Forest)

!(https://github.com/user-attachments/assets/301bec86-464e-4e73-820f-0b8241a2c1f4)
*Figure 6: Scatter plot comparing actual and predicted delays.*



## Output files:
- Model performance results: model_results.csv
- Business impact report: business_analysis.txt

## Business Impact Summary:
- Transit Scheduling Improvements: Predictive insights can help optimize subway schedules during peak hours.
- Infrastructure Planning: Identifying problematic stations helps prioritize maintenance and upgrades.
- Economic Benefits: Reducing delays can save operational costs and improve commuter satisfaction.

## Future Work:
For more effective business impact, we recommend the following measures:
- Integrate real-time delay prediction using live data feeds.
- Improve model accuracy with additional external factors (e.g., weather, special events).
- Develop a web dashboard for interactive delay forecasts.
- Gather data on passenger count to determine the quanitiy of passengers affected by delays.
- Gather data on delay reasons to compare the impact of delays on passenger count.

## Contributors:
- Chinyere Johnson
- Tian Qin
- Faraz Shahid (Data Acquisition, Collection, Cleaning, Initial Exploration including Statistics/Visualizations)
- Joey Poh
- Peeu Banerjee

## References:
- Open Toronto Data - TTC Subway Delay Data: https://open.toronto.ca/dataset/ttc-subway-delay-data/
- Scikit-learn documentation: https://scikit-learn.org/
