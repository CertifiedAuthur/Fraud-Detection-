# Fraud-Detection-

### Summary of Fraud Detection Model for E-commerce Company

#### Objective:
Our company, specializing in handmade clothes, aims to develop a tool to identify fraudulent activities in real-time to prevent theft. 

#### Scope of Work:
1. Determine the user's country from their IP address.
2. Build a machine learning model to categorize transactions as fraudulent or safe.
3. Explain the model in simple terms for non-technical users.

#### Datasets:
- Fraud Data: Contains user information like sex, age, signup time, IP address, and fraud status.
- IP Address Data: Maps IP ranges to countries.

#### Data Insights:
1. Data Size: The Fraud Data set contains 151,112 entries, and the IP Address Data set has 138,846 entries.
2. IP Mapping: Successfully mapped each IP address to its respective country.
3. Categorical Columns: 
   - "Source": SEO, Ads, Direct.
   - "Browser": Chrome, Opera, Safari, IE, FireFox.
4. Device Usage: 
   - 8.7% of transactions come from previously used devices.
   - On average, a device is used 3.1 times; the most used device appeared 20 times.
   - When a device is used more than twice, it is used on average 10.2 times.
5. Fraud Proportion: 9.3% of the dataset represents fraudulent transactions.
6. Class Balance: Used resampling techniques to balance the classes.

Analysis:
1. Source and Browser: 
   - "Direct" source has the highest traffic.
   - Chrome is the most used browser.
   - Majority of users are male.
2. Patterns: 
   - No clear patterns in weekday purchases, countries from the device, risk country, quick purchase, age category, and period of the day.
   - More frequent device usage correlates with higher fraud risk.
   - January shows the highest number of fraudulent transactions.
3. Purchase Cycle and Age: 
   - Higher fraud likelihood at specific purchase cycle stages.
   - Age is not a strong fraud predictor except for certain age groups.
   - Monitoring the number of devices can be a key factor in fraud detection.

Model Performance:
1. Logistic Regression:
   - Training Accuracy: 89.4%
   - Test Accuracy: 89.5%
   - With a 22% probability threshold: 88.7% accuracy on the test data.
2. Resampling: Achieved class balance with 23% fraud after resampling.
3. Stacking Model:
   - Iterative improvements observed in train and test scores using predict_proba.
   - Consistent scores using binary predict.
4. Random Forest:
   - Training Score: 89.1%
   - Test Score: 89.3%
5. Decision Tree:
   - Training Accuracy: 89.5%
   - Test Accuracy: 89.8%

The model shows good performance in detecting fraudulent transactions with high accuracy on both training and test datasets. The approach includes data preprocessing, feature engineering, and leveraging various machine learning algorithms to achieve robust results. The use of stacking and resampling techniques further enhances the model's performance.
