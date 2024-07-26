---

# Tourism Package Purchase Prediction

## Overview
This project predicts customer likelihood to purchase a new travel package using machine learning. We analyze various customer attributes from the `Tourism.xlsx` dataset to build and evaluate predictive models.

## Dataset Features
- **CustomerID**: Unique customer identifier
- **ProdTaken**: Binary indicator of package purchase
- **Age**: Customer age
- **TypeofContact**: Contact method (Self Enquiry, Company Invited)
- **CityTier**: Customer's city tier
- **DurationOfPitch**: Sales pitch duration
- **Occupation**: Customer occupation
- **Gender**: Customer gender
- **NumberOfPersonVisiting**: Group size
- **NumberOfFollowups**: Follow-up count
- **ProductPitched**: Type of product pitched
- **PreferredPropertyStar**: Preferred hotel rating
- **MaritalStatus**: Customer marital status
- **NumberOfTrips**: Customer's trip count
- **Passport**: Passport ownership status
- **PitchSatisfactionScore**: Sales pitch satisfaction rating
- **OwnCar**: Car ownership status
- **NumberOfChildrenVisiting**: Number of children in group
- **Designation**: Customer's job designation
- **MonthlyIncome**: Customer's monthly income

## Tech Stack
- Python 3.x
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn, XGBoost
- Missingno

## Key Findings from EDA
- 20% of customers purchased the travel package
- Most customers from Tier 1 cities
- Average pitch duration: 2-3.5 minutes
- Majority are salaried or small business owners
- Preferred hotel rating: 3-star
- Average 2-6 trips per year
- Income range: $20k-$40k monthly

## Data Preprocessing
- Log transformation for outlier handling
- Median/mode imputation for missing values
- Dummy encoding for categorical features

## Model Performance Summary

| Model                | Baseline f1-score | Tuned f1-score |
|----------------------|-------------------|----------------|
| Decision Tree        | 0.794             | 0.882          |
| Random Forest        | 0.755             | 0.822          |
| Bagging Classifier   | 0.736             | 0.904          |
| AdaBoost             | 0.359             | 0.807          |
| Gradient Boosting    | 0.403             | 0.927          |
| XGBoost              | 0.819             | -              |
| Stacking Classifier  | -                 | 0.835          |

## Conclusion
The Gradient Boosting model with tuned hyperparameters achieved the best performance, with a weighted f1-score of 0.927 on the test set.

## Future Work
- Advanced feature engineering
- Experiment with neural networks and other ensemble methods
- Real-time prediction deployment and marketing integration

---
