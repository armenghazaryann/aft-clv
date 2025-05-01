# Customer Churn Prediction Analysis

This project focuses on predicting customer churn using Accelerated Failure Time (AFT) models. The analysis uses customer data to build and evaluate several models to predict churn and analyze the factors influencing customer retention.

## Report
After evaluating different models for predicting customer churn, I chose the LogNormal AFT model because it provided the best fit, with the lowest AIC score. This model indicates that several factors have a significant impact on churn, including age, customer category, internet and voice subscriptions, and marital status. Notably, customers who subscribe to either internet or voice services are more likely to churn. This could suggest issues with pricing or dissatisfaction with the service. On the flip side, older, married, or retired individuals tend to stay longer as customers, contributing to a higher customer lifetime.

When I calculated Customer Lifetime Value (CLV), I found that the most valuable customer segments are older, married individuals with longer tenures, especially those in the "Total service" or "Plus service" categories. Interestingly, customers who don't have internet or voice add-ons had higher predicted CLVs. This might be because customers who opt for additional services have higher expectations, and they tend to leave if those expectations aren’t met.

To reduce churn, I recommend prioritizing high-CLV customers, particularly those in premium service categories. It's also worth investigating why customers with internet or voice services are leaving, as offering bundles or enhancing service quality could help address this. Finally, targeted outreach, such as emails or calls, should be directed at younger and unmarried subscribers, as they seem to be at a higher risk of churning.


## Key Steps

1. **Data Management**:
   - Data was loaded and preprocessed to ensure clean and usable input for modeling.
   - Columns such as `churn` were encoded and checked for consistency.

2. **Modeling**:
   - The following AFT models were evaluated:
     - **WeibullAFT**
     - **LogLogisticAFT**
     - **LogNormalAFT**
   - AIC scores were calculated for each model, and the LogNormal AFT model showed the best fit.

3. **Model Evaluation**:
   - Survival curves were plotted for each model to visualize customer retention.
   
4. **Recommendations**:
   - Focus on retaining high-CLV customers, particularly those in premium service categories.
   - Investigate customer churn in internet or voice service subscriptions and explore bundling offers.
   - Target outreach efforts at younger and unmarried customers.

## Installation

To get started, clone the repository and install the necessary dependencies:

```bash
git clone git@github.com:armenghazaryann/aft-clv.git
cd aft-clv
pip install -r requirements.txt
```