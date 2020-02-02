# Ecommerce-Fraud-Detection

Summary:

The given case is divided in three parts:

- Data Exploration
- Data Prep
- Data Modelling

Data Exploration:
In this module the given dataset was analyzed to understand the data. Here are some insights:
Libraries Used:
Numpy : To perform operations
Pandas : To create dataframes
Matplotlib: To perform Visualization
Sklearn: To import Random Forest Model

- Load the csv files.
- The Fraud_data contains rows & columns(151112, 14)
- The Ip_Address_country contains rows & columns (138846, 3)
- Lower Bound and Upper Bound Ip address are mapped to the Ip_Address and country
  in Fraud_Data.
- The data is imbalanced as target variables contains 90.50% No Fraud data and 9.50%
  Fraud data.
- The Fraud occur most on the purchase date of Jan 2nd 2015.
- The purchase time is uniformly distributed for the Fraud data.
- The fraud data was recorded on the Chrome browser among all.
- United States has the most fraud data.
- The channel was uniformly distributed when analyzing the fraud and no fraud data.
- The age is uniformly distributed for both fraud and no fraud data.
- Gender is uniformly distributed for both fraud and no fraud data.
- Most of the purchase value between 0 and 40 has the fraud data.
- For the age group of 28-35 most fraud occurred.
- From the analysis we can find that most frauds occur when the purchase_date and
  signup_date are same while purchase_time and sign_up time are uniformly distributed.
- Deleted the NaN rows from the country column.

Data Prep:

- All the columns are converted into numeric form for data modelling.
- Since the data is unbalanced, undersampling method (since we have enough data, used
  this method over oversampling method) is used to balance the data for improving the
  classification performance.
- Signup_time and Purchase_time driver variables are excluded from the analysis as they
  have least significant impact on the target variable.

Data Modelling:
- Random Forest model is applied on the data to classify the prediction of Fraud and
  No-Fraud.
- It is used as it can achieve the higher accuracy for the large datasets.
- Random Forest has Precision of 86% , Recall of 59% and F1 of 69%.
