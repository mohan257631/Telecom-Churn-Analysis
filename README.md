# Customer Churn Prediction with Logistic Regression

## Project Overview

This project aims to predict customer churn using a logistic regression model. 
The dataset includes various customer attributes and services they subscribe to. 
The analysis focuses on identifying key factors that influence customer churn, with a special emphasis on interaction effects between services.

## Objectives

- Understand the factors driving customer churn.
- Assess the significance of both individual features and their interactions.
- Use logistic regression to model the likelihood of a customer churning.
- Evaluate the performance and significance of the model through key metrics.

## Dataset

The dataset includes the following features:

- **SeniorCitizen**: Whether the customer is a senior citizen.
- **Tenure**: The number of months a customer has stayed with the company.
- **PaperlessBilling**: Whether the customer uses paperless billing.
- **MonthlyCharges**: Monthly subscription charges.
- **CommunicationServices**: Whether the customer uses communication services. (extracted info)
- **OnlineServices**: Whether the customer subscribes to online services. (extracted info)
- **EntertainmentServices**: Whether the customer subscribes to entertainment services. (extracted info)
- **Loyalty**: A measure of customer loyalty. (extracted info)

## Methodology

1. **Data Preparation**: 
   - The dataset was cleaned and pre-processed, including handling missing values, removing duplicates and outlier detections with outlier evaluation.
   
2. **Feature Engineering**:
   - Extracted useful info from different variables and reduced dimensionality of the data with sufficient statistical backing.
   - Made variables much more interpretable using domain knowledge.
   - Interaction terms between key services (e.g., EntertainmentServices and OnlineServices) were created to evaluate their combined effect on churn.

4. **Modeling**:
   - A logistic regression model was used to predict customer churn.
   - Interaction terms were included in the model to explore whether combinations of services affect churn more than individual services.
   - Model assumptions were checked to ensure the validity of the logistic regression.

5. **Evaluation**:
   - Model significance was evaluated using key metrics such as:
     - Log-likelihood
     - BIC (As the sample size was big)
     - P-values for individual coefficients and interaction terms.

## **Key Findings and Recommendations:**

Based on the above analysis, we propose some measures to decrease churning.

- Customers having only Communication Services are less likely to churn.
- Customers having only Internet Services are also less likely to churn.
- Customers having only one out of Internet and Entertainment Services must be marketed the other service to make them more involved into the company environment.
- The above plan must be applied in moderation as high monthly charges act as a huge reason for customers to churn. Customers having all three services might have higher monthly charges which in turn increases the probability of their churn.
- Customers who stay long with the company are much less likely to churn. We need to make the longer contract deals much more attractive to the customers than the shorter term deals.
- Senior Citizens are a much more attractive group of customers, as once they come on board, they tend to stick around.
- Younger customers with a family are also a lucrative group of customers, as they tend to take longer contracts.

## Future Work

- Further feature engineering to capture more nuanced customer behavior.
- Explore additional machine learning models like random forests or gradient boosting to improve predictive performance.
- Experiment with resampling techniques to address class imbalance.
- This model gives the probability of churning given the different variables. Using survival analysis techniques, design a model that effectively captures the probability
of churn at various junctures of time. This will give a much broader over view of the churn and its dependencies.


## Conclusion

This project successfully identifies key drivers of customer churn and provides actionable insights for improving customer retention strategies by leveraging logistic regression and interaction terms.
