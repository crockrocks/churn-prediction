# Churn Prediction Model: Analysis and Recommendations
### Initial Analysis
After loading the dataset and conducting exploratory data analysis (EDA), it was observed that there were no missing values. The dataset contained three categorical features. The customer name feature was dropped as it was not relevant to the predictive task. Label encoding was applied to the Gender and Location features. Univariate analysis and visualizations were performed, and a correlation matrix was generated. The correlation matrix indicated that none of the features were significantly correlated with each other or the Churn feature.

### Model Development
The initial model selected was a RandomForestClassifier, which yielded a low accuracy. Hyperparameter tuning using RandomSearchCV did not improve the performance. Subsequently, various classification models were tested, including DecisionTree, LogisticRegression, KNeighborsClassifier, and BalancedBaggingClassifier. None of these models achieved satisfactory results.

### Neural Network Implementation
A simple three-layer feed-forward neural network was trained, but accuracy remained low. Additional features were generated and plotted, yet no improvement was observed. A more complex neural network with additional layers, dropout, and early stopping callbacks was implemented, but it also failed to enhance accuracy.

### AutoGluon Validation
AutoGluon was used to automatically train various models, confirming that the accuracy remained around 50%, consistent with previous results.

### Conclusion and Recommendations
The analysis concluded that the dataset lacks sufficient features to improve model performance. To enhance the model's accuracy, it is recommended to augment the dataset with additional features:

* Customer Activity: Metrics such as the number of logins or click-through rates to gauge engagement.
* Customer Complaints/Issues: Data on customer complaints, including support tickets and types of issues.
* Customer Satisfaction Scores: Customer satisfaction survey data, such as satisfaction scores.
* Incorporating these features is anticipated to improve the model's ability to predict customer churn accurately.
