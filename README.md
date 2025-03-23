# TTC Delay Predictor

![image](https://cdn.ttc.ca/-/media/Project/TTC/DevProto/Icons/TTC-LOGO.svg?h=80&iar=0&w=130&rev=70dfaadb771a4a7486ae723e174fa823&hash=94FBEA98380BF40A67DA1D1C9E2FFB73)

## 1.0 Overview:
- Subway delays are a major inconvenience for Toronto commuters, affecting travel time and overall transit efficiency. This project aims to build a regression model to predict subway delays based on factors such   as time of day, station location, and train line. By identifying key patterns in delay occurrences, we can provide actionable insights to improve transit operations and commuter experience.

## 2.0 Stakeholders & Impact:
- **Toronto Transit Commission (TTC), City Planners:** This project will help TTC/city planners optimize schedules, deploy resources effectively, and improve service reliability through data-driven decision making.
- **Local Businesses:** This project will allow businesses near transit hubs to adjust schedules based on predicted delays as it would lead to more productive employee performances driving down costs. It would also allow businesses to import/export goods/services more efficiently driving down business costs.
- **Commuters:** Delays impact work, school and appointments of transit users. This project will provide real-time insights into transit delays so commuters can plan accordingly reducing stress and driving up productivity.
- **Environmental Policy Advocates:** Public transit delays push people toward private cars, thus increasing emissions. This project can support policies aimed at improving public transport reliability and usage of TTC.

## 3.0 Transit Delays versus Society: 
- **Social Impact**:
Subway delays increase commuter stress, leading to dissatisfaction with public transit. People who rely on the TTC for work, school, and appointments experience daily disruptions. Unreliable service can push riders toward other transportation options, reducing trust in the system.
- **Economic Impact**:
Transit delays reduce workplace productivity as employees arrive late or miss important meetings. Businesses near subway stations may also suffer revenue losses if delays discourage foot traffic. A poorly functioning transit system can weaken a city's overall economic efficiency.
- **Environmental Impact**:
Frequent delays push commuters toward personal vehicles, increasing traffic congestion and carbon emissions. This shift away from public transportation contributes to pollution and makes urban areas less sustainable. A more reliable subway system encourages people to choose eco-friendly transit options.
- **How This Project Aims to Help**:
Our machine learning model predicts subway delays, allowing transit authorities to take proactive measures. Identifying high-delay periods helps optimize train schedules, reducing disruptions. These insights can improve the overall commuter experience, making public transit a more attractive and efficient choice.

## 4.0 Research Question:
- Can we predict the average delay (Min Delay) of Toronto transit vehicles based on factors like time of day, station location, and train line?

## 5.0 Questions We Are Trying to Answer: 
- What times of the day have the longest delays?
- Which subway lines/stations are most affected?
- How predictable are delays based on historical trends?
- Can machine learning provide accurate delay forecasts?
  
## 6.0 Dataset:
- Source: Open Toronto Data - TTC Subway Delay Data
- Description: The dataset from Open Toronto covers TTC subway delays from 2017-2025. The dataset includes historical subway delay records, including details on station, time, line, delay reason, and duration. The dataset has missing values, inconsistent station names, and lacks real-time external factors like weather and special events.
- Dataset Limitations: no real-time tracking, station-based delays and duration inconsistencies

 ## 7.0 Risks & Uncertainties:
- Like any data-driven project, this model comes with challenges. One major risk is data gaps and inaccuracies—some delays might be underreported or missing, which could impact the reliability of our predictions. Additionally, the dataset has a limited scope, as it doesn’t account for external factors like weather, accidents, or labor strikes, all of which can significantly impact subway delays. Another challenge is changing transit patterns like the COVID-19 pandemic, new subway expansions, or shifts in commuter behavior could make historical data less predictive of future delays.
- To address these uncertainties, we’ll focus on data cleaning and validation to handle inconsistencies and ensure accuracy. Feature engineering will play a key role in making our model more robust by identifying patterns even within an imperfect dataset. In the future, we may integrate external data sources like weather reports and real-time transit feeds to enhance prediction accuracy and make the model even more useful for riders and transit authorities alike.

## 8.0 Key Features Used:
- Time Period: Time of the delay occurrence.
- Station: The affected subway station.
- Line: Subway line affected.
- Min Delay: Duration of the delay (target variable).
- Cause: The reason for the delay.

## 9.0 Project Objectives:
###   9.1 Develop an Accurate Subway Delay Prediction Model
- Build a machine learning regression model to predict average subway delay times (in minutes) using historical TTC subway delay data.
- Compare different regression models, starting with a baseline Linear Regression model, and explore advanced techniques like Random Forest Regressor or deep learning.
- Optimize model performance using hyperparameter tuning to improve prediction accuracy.
  
###   9.2 Analyze Key Factors Affecting Subway Delays
- Investigate how factors such as time of day, station location, and train line influence subway delays.
- Perform feature importance analysis to determine which variables contribute most to delays.
- Conduct error analysis to identify and mitigate common sources of prediction errors.

###   9.3 Ensure High-Quality Data Processing & Preparation
- Perform data cleaning, including handling missing values, standardizing station and train line names, and converting time fields into meaningful numerical/categorical features.
- Engineer new features such as rush hour indicators, day of the week, seasonal trends, and location-based encoding to enhance predictive power.
- Normalize numerical variables and encode categorical variables for improved model performance.

###   9.4 Evaluate and Validate Model Performance
Assess model accuracy using key performance metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared (R²).
Compare model results against the baseline model to determine performance improvements.
Use cross-validation techniques to ensure model generalizability across different time periods and conditions.

###   9.5 Visualize and Interpret Model Findings
- Generate data visualizations to illustrate subway delay trends by station, time of day, and train line.
- Compare actual vs. predicted delay distributions to validate model effectiveness.
- Present findings in a clear and interpretable manner for stakeholders, enabling informed decision-making.

###  9.6 Document Methodology and Findings
- Compile a comprehensive project report detailing the methodology, findings, and recommendations.
- Prepare a presentation summarizing the project’s key insights and predictive outcomes.

###   9.7 Lay the Foundation for Future Enhancements
- Identify potential areas for improvement, such as incorporating real-time transit data, weather conditions, or passenger load data for more accurate predictions.
- Discuss possible deployment strategies to integrate the model into TTC’s operational decision-making systems.

###   9.8 Business Impact Analysis:
- Identify critical time periods and stations for delay occurrences.
- Estimate potential cost savings from reducing delays.
- Provide insights for TTC and city planners to improve transit efficiency.

## 10.0 Findings and Trends: ##

###  10.1 Trends in Subway Delays Over Time
The analysis of average delay times across years highlights a notable increase in delays, especially after 2019 (possibly due to effects of COVID-19 causing labor shortages and decrease in preventative activities). Since 2019, the cost due to delays is also on an up-ward trend with cost to TTC due to delays ballooning to over $7 million in 2022 and 2024 (refer to Figure 2). Generally, the trend suggests that delays have been worsening over time, potentially due to factors such as increased ridership, aging infrastructure, or operational inefficiencies. 
 ![image](https://github.com/user-attachments/assets/7932d642-4872-450b-b489-506dbf349360)

Figure 1. Trend of Average Delay Time Over the Years.
![image](https://github.com/user-attachments/assets/86721766-3557-416c-bb69-f59c4000f7f4)

Figure 2. Estimated cost of delays over the years (assuming $100 per minutes of cost per standard TTC data). 

Actionable Insight for TTC: Further investigation into policies or operational changes introduced around 2019-2020 may help identify key contributing factors to this exponential-like increase.

###  10.2 Delay Patterns by Time of Day
A closer look at subway delays by hour of the day shows clear rush-hour peaks around 6 AM - 9 AM and 4 PM - 6 PM, which correspond to typical commuter traffic (rush hour times).
 ![image](https://github.com/user-attachments/assets/28214c20-f988-404a-b02e-62942af122a6)

Figure 3. Plot of Average Delay (in minutes) by Time of the Day (24-hour format). 
 ![image](https://github.com/user-attachments/assets/be5f8e44-1a36-4c22-9a07-4937edbf1766)

Figure 4. Plot of number of Delays by Time of the Day (on an hourly basis). 
 ![image](https://github.com/user-attachments/assets/fe5f41a2-4e4d-4063-b2da-1bc44b8513b7)

Figure 5. Heatmap of Delays by Hour of Day (24-hour format) and Day of the Week. 

Actionable Insight for TTC: Resource allocation strategies should focus on these peak congestion periods to mitigate delays.

###  10.3 Most Delayed Stations
Some TTC subway stations experience significantly more delays than others. The data reveals that the top 10 most frequently delayed stations include Kennedy, Kipling, Finch, and St. George, among others.
 ![image](https://github.com/user-attachments/assets/ef32c19a-1174-4da8-8436-a3568dd398ac)

Figure 6. Plot of top 10 most frequently delayed stations.
 ![image](https://github.com/user-attachments/assets/d826bd4f-cb27-4655-9de4-24eadaabc19d)

Figure 7. Plot of subway delays (in minutes) at the top 10 most frequently delayed stations. 

Actionable Insight for TTC: Strategies to improve operations at these stations (e.g., better train scheduling, faster turnaround times) could have a system-wide impact on reducing overall delays.

###  10.4 Most Delayed Subway Lines
Certain subway lines experience higher average delays than others. The top 10 subway lines with the highest average delay times include 66 Bus Route, Scarbrough (SRT) Line and followed by other bus routes.
 ![image](https://github.com/user-attachments/assets/831c82d1-72df-4642-951d-1f323f9ed80d)

Figure 8. Plot of top 10 Subway/Bus Lines with Highest Average Delay (in minutes).

Actionable Insight for TTC: Focused maintenance and operational improvements on high-delay subway/bus lines could greatly improve overall service efficiency.

###  10.5 Delay Causes and Their Impact
Delays in the subway system occur due to a variety of reasons, including mechanical failures, signal issues, track maintenance, and external factors. The analysis identifies the top 10 delay reasons that result in the highest average delay times.
 ![image](https://github.com/user-attachments/assets/3b716906-0c68-47c9-be44-fa7840193674)

Figure 9. Plot of top 10 Delay Reasons with Highest Average Delay (in minutes). 
 ![image](https://github.com/user-attachments/assets/4e95a4cc-351a-41d0-bef6-67ac93c0f4b2)

Figure 10. Plot of correlation between Rush Hour, Non-Rush Hour, and top 10 most frequent Delay Codes.
Actionable Insight for TTC: Preventative maintenance focused on the most common high-delay causes could lead to a reduction in prolonged service disruptions.

###  10.6 Correlation Between Train Gap and Delays
A strong positive correlation (r = 0.91) exists between train/bus gaps (time between consecutive trains/buses) and delays. This suggests that longer gaps in train/bus schedules contribute to longer delays.
 ![image](https://github.com/user-attachments/assets/1c8d70c8-35c2-4289-afa2-373fbac70bc4)

Figure 11. Plot of Correlation between Trains/Busses Gap Time and Delay Time. 

Actionable Insight for TTC: Optimizing train frequency and reducing unexpected schedule gaps could reduce overall subway delays.

###  10.7 Directional Impact on Delays
The train’s direction of travel ('Bound') also affects delays. The topmost delayed bound directions reveal that southbound and westbound trains experience the highest delays.
 ![image](https://github.com/user-attachments/assets/b6e1a21f-f894-4689-999e-2754ab77acce)

Figure 12. Plot of Number of Delays by Train Direction. 

Actionable Insight for TTC: Operational planning should consider high-delay directions and adjust scheduling accordingly.

###  10.8 Most Delayed Vehicles and Their Associated Delay Codes
The analysis reveals that certain vehicles are repeatedly delayed. The data also shows which delay codes are most commonly associated with these delayed vehicles. The most common reasons for delays were (Low Voltage – EULV, Fire/Smoke – MUPLB, Bomb Threat – SUBT, Doors Open in Error – TUDOE, Consequential Delay – EUCD, and Track Level Debris Controllable, No Operator Immediately Available – TUNOA, Speed Control Fault – MUSC, Passenger Assistance Alarm Activated - MUPAA). Some of these reasons are controllable through proper maintenance activities, scheduling and predicable (i.e., EULV, Debris, Operator Availability) while others are not controllable (i.e., someone pulling the fire alarm). 
 ![image](https://github.com/user-attachments/assets/ca3da2c9-e6b6-4978-8c80-f164e42d22d9)

Figure 13. Plot of Top 10 Vehicles with Highest Average Delay.
 ![image](https://github.com/user-attachments/assets/c14f33ed-118e-41c7-b412-9538138bc228)

Figure 14. Plot of Top 10 most delayed vehicles and associated reasons. 
 ![image](https://github.com/user-attachments/assets/b502efc5-4957-4d79-a5e0-8d0f47244579)

Figure 15. Plot of Top 10 Vehicle with most delay occurrences and associated reasons. 

Actionable Insight for TTC: Targeted maintenance of frequently delayed vehicles as well as effective scheduling could significantly improve reliability of service.

###  10.9 Correlation Between Delay Code and Subway Line
An analysis of the correlation between subway lines and the top 10 most frequent delay codes helps understand which lines are affected by which specific delay types. Data reveals that Miscellaneous Speed Control (MUSC) and Passenger Assistance Alarm Activated (MUPAA) are the most common reasons for subway lines, which are human actions and cannot be completely controlled. However, it may be helpful looking at reasoning behind MUSC delays to understand why speed reductions happens (i.e., track conditions due to weather). This data is not available for us and integration of such data would lead to a better understanding and model. 
 ![image](https://github.com/user-attachments/assets/5abcb763-b1a1-4a49-9493-2019633ee3e2)

Figure 16. Plot of Correlation Between Subway Line and Top 10 Most Frequent Delay Code. 
 ![image](https://github.com/user-attachments/assets/b977d122-741d-4d80-984b-4824bc54ead0)

Figure 17. Plot of Correlation Between Top 10 Most Frequent Delay Codes and Bound Direction.

Actionable Insight for TTC: Customized mitigation strategies for specific subway lines based on their most common delay reasons can improve overall efficiency.

## 11.0 Data Acquisition & Cleaning: 
During the data cleaning process, several steps were taken to ensure data consistency and reliability. First, missing values in numerical columns, "Min Delay" and "Min Gap", were imputed with the average values for the corresponding "Station" to maintain accurate delay estimates. Rows with missing values in essential categorical columns, such as "Station", "Date", "Time", and "Day", were removed to preserve data integrity. For categorical fields, missing values in "Code" were replaced with the most common delay reason associated with the respective "Station", while missing values in "Bound" (train direction) and "Line" (subway line) were replaced with their most frequent values for the corresponding "Station" to maintain consistency. Additionally, rows where the "Vehicle" column was missing were removed to ensure that every record had a valid vehicle number.

To resolve inconsistencies, "Station" names were standardized based on actual TTC subway station names, while bus stops were mapped to their correct street intersections. Non-standard TTC names that did not represent actual subway stations or bus stops were identified and removed to prevent errors in analysis. The "Bound" column was also corrected by removing non-standard or incorrect train directions that did not align with TTC's defined data standards. Similarly, the "Line" column was cleaned by removing any entries that did not correspond to an actual TTC subway line.

Furthermore, outliers above the 99th percentile in numerical columns were detected and removed to prevent skewed results. Duplicate records were also identified and eliminated to ensure the dataset did not contain redundant data points. The "Vehicle" column was checked for inconsistencies, and any values that were zero, negative, or non-numeric were removed. The "Date" and "Time" columns were also reviewed for consistency, ensuring they followed the correct format and contained valid timestamps.

These comprehensive cleaning steps enhanced data quality, removed inconsistencies, and ensured that the dataset was accurate, structured, and suitable for analysis and predictive modeling.

## 12.0 Model Evaluation and Analysis:

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

## 13.0 Conclusion & Recommendations
-	Delays are rising over time, with a sharp increase post-2019. Investigating policy and operational changes from this period may help identify contributing factors.
-	Rush hour delays (6-9 AM, 4-6 PM) are the highest, requiring optimized scheduling and resource allocation to manage peak congestion.
-	Kennedy, Kipling, and Finch stations experience the most delays—improving turnaround times and traffic flow at these stations could reduce overall disruptions.
-	Certain subway/bus lines, including the Scarborough (SRT) Line, have the highest delays. Focused maintenance and operational improvements are needed for these routes.
-	Mechanical failures, track-level debris, and voltage issues are leading delay causes. Prioritizing preventative maintenance can minimize service disruptions.
-	Train/bus gaps strongly correlate with delays, highlighting the need for improved scheduling and real-time monitoring to maintain frequency.
-	Southbound and westbound routes experience the longest delays, suggesting a need for targeted scheduling adjustments to balance service efficiency.
-	Customized solutions for each subway line, including predictive maintenance and better response strategies for common delay causes, can improve overall system.

###  13.1 Delay Trends:
![image](https://github.com/user-attachments/assets/9e1f2791-c631-418c-86e2-0d6b1f9a8f9c)

*Figure 1: Line graph showing the Trend of Average Delay Time Over the Years.*

###  13.2 Model Performance Comparison:
- The best-performing model was Optimized Random Forest, with an R² score of 0.89, MSE of 7.97 and MAE of 0.37, achieving the lowest MAE and highest R².
- XGBoost had competitive performance but slightly underperformed Random Forest.
- The stacking model showed improvements in some cases but added complexity.

![image](https://github.com/user-attachments/assets/b05538a0-1a69-4018-a453-f3a729f759e2)

*Figure 2 showing the comparison of models.*

###  13.3 Peak Delay Times:
- Peak delay times were observed during morning (7-9 AM) and evening rush hours (5-7 PM).
  
![image](https://github.com/user-attachments/assets/8bac6f97-8457-45dc-a09c-961e41f02d1d)

*Figure 3 showing Heatmap Delays by Hour and Day.*

###  13.4 The Most Affected Stations:
- The most affected stations were Kennedy, Kipling and Finch station.

![image](https://github.com/user-attachments/assets/fae21c32-f818-4309-8ce5-86792503aaab)

*Figure 4 showing the top 10 most frequently delayed stations.*

###  13.5 The Most Significant Feature:
- The minimum gap had a significant impact.
 
![image](https://github.com/user-attachments/assets/db9526b7-bf27-4017-864a-619eff4c1d6e)

*Figure 5 showing the most significant feature.*

###  13.6 Actual vs predicted delays:
- Actual vs predicted delays (using the best model: Optimized Random Forest)

![image](https://github.com/user-attachments/assets/b6e71cd5-de08-4575-8ff0-a47134d4ddd6)

*Figure 6: Scatter plot comparing actual and predicted delays.*

##  14.0 Business Impact Summary:
- Transit Scheduling Improvements: Predictive insights can help optimize subway schedules during peak hours.
- Infrastructure Planning: Identifying problematic stations helps prioritize maintenance and upgrades.
- Economic Benefits: Reducing delays can save operational costs and improve commuter satisfaction.

## 15.0 Future Work:
For more effective business impact, we recommend the following measures:
- Integrate real-time delay prediction using live data feeds.
- Improve model accuracy with additional external factors (e.g., weather, special events).
- Develop a web dashboard for interactive delay forecasts.
- Enhance model capability by accounting for passenger count and delay reasons to determine the quanitiy of passengers affected by delays and to compare the impact of delays on passenger count.

## 16.0 Contributors:
- [Chinyere Johnson](https://www.youtube.com/watch?v=lqymaEIcpXk)
- Tian Qin https://youtu.be/klpSSW3gnBo
- Faraz Shahid (Video: https://youtu.be/yFL2x7UgmaA)
- Joey Poh
- Peeu Banerjee

## 17.0 References:
- Open Toronto Data - TTC Subway Delay Data: https://open.toronto.ca/dataset/ttc-subway-delay-data/
- Scikit-learn documentation: https://scikit-learn.org/
