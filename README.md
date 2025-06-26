# Python-Traffic-flow-Analysis 
This project focuses on predicting traffic flow using historical data, which includes vehicle counts like cars, bikes, buses, trucks, time of day, and day of the week. By analyzing these variables, the system identifies traffic patterns, forecasts future traffic conditions, and offers valuable insights to support congestion management and urban mobility planning.

The model is designed to:
Predict traffic flow for specific time periods.
Help optimize traffic control strategies such as signal timings and route planning.
Support sustainability goals by reducing fuel consumption and emissions through smarter traffic management.
This system can be integrated with smart city infrastructure to enhance real-time traffic decision-making and improve overall transportation efficiency.

# Data Dictionary
The dataset contains historical records of traffic flow with the following features:
Feature	                             Description
Time	                    Timestamp of the observation (e.g., 08:30:00)
Date	                    Date of the observation (e.g., 2025-06-25)
Day of the Week	          Name of the day corresponding to the observation (e.g., Monday, Tuesday)
CarCount	                Number of cars counted at the observation point
BikeCount	                Number of bikes counted
BusCount	                Number of buses counted
TruckCount	              Number of trucks counted
Total	                    Total number of vehicles (sum of all vehicle types)
Traffic Situation	        Categorized traffic condition (e.g., Light, Moderate, Heavy)

# Data Preprocessing
The dataset was cleaned and prepared by converting date and time into a unified datetime format, encoding the day of the week using LabelEncoder, and calculating the total vehicle count from individual categories (cars, bikes, buses, trucks). Categorical traffic situations were also label-encoded for model training. All data types were verified, and a correlation analysis was performed to understand feature relationships.

# Exploratory Data Analysis (EDA)
EDA was performed to understand traffic patterns and feature relationships. Visualizations such as line plots, bar charts, and heatmaps were used to analyze vehicle trends by time and day, identify peak traffic hours, and assess correlations between vehicle types and traffic situations. This helped uncover patterns essential for accurate traffic prediction.

# Model Building
A supervised machine learning approach was used to predict traffic situations (e.g., Light, Moderate, Heavy) based on historical data. The following classification models were trained and compared:

Linear Regression:
Used as a baseline model to understand how continuous features like vehicle counts and time relate to traffic flow. Though primarily a regression algorithm, it provided insight into how strongly different features influenced total traffic volume.

Random Forest Classifier: 
An ensemble of multiple decision trees that improved accuracy and robustness by reducing overfitting. This model performed the best in capturing complex traffic patterns and was selected as the final model for prediction.

All models were trained on labeled traffic data using features such as vehicle counts, day of the week, and time. The dataset was split into training and testing sets, and hyperparameters were tuned to enhance model performance.

# Model Evaluation
Models were evaluated using metrics such as accuracy, precision, recall, and F1-score. Confusion matrices were generated to visualize prediction performance. Among the models tested, the Random Forest classifier achieved the best balance between performance and generalization, making it suitable for real-world traffic prediction scenarios.

# Conclusion
This project successfully demonstrates how machine learning can be used to predict traffic situations based on historical vehicle data. By analyzing patterns in time, day, and vehicle counts, the model provides accurate traffic predictions that can help improve congestion management and support smarter urban mobility planning.



