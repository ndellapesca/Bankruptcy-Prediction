# bankruptcy-prediction
Using a dataset with financial data from 6,000 companies, I implemented a variety of machine learning models to predict the likelihood of bankruptcy. Given the highly imbalanced nature of the dataset (with only ~3% of companies experiencing bankruptcy) I employed six different imbalance handling techniques to enhance model performance.
To determine the optimal decision threshold for classifying a company as bankrupt, I used Youden’s J statistic. This metric ensures a balanced trade-off between true positive and true negative rates, critical for minimizing financial risk. However, future companies that are more concerned with accurately predicting potential bankruptcies can opt for lower thresholds or assess their probability of bankruptcy. This "better safe than sorry" approach prioritizes identifying potential bankruptcies, even if it comes at the expense of overall model accuracy. 
Throughout the modeling process, I recorded several performance metrics, including model accuracy, Youden’s J statistic, AUC, F1 Score, Cohen’s Kappa, and Matthew’s Correlation Coefficient. These metrics provide a comprehensive view of each model's performance in many different aspects, catering to the diverse needs of companies by allowing them to select the most relevant metrics for their specific financial situation, enabling more tailored and informed decision-making.
By integrating these imbalance techniques and evaluating multiple performance metrics, my approach offers a reliable framework for predicting corporate bankruptcy, addressing the unique challenges posed by the imbalanced dataset and optimizing model accuracy and reliability, while meeting the diverse needs of companies and adapting to their unique financial situations.
| Method                | Data                  | Threshold | Youden’s J | Accuracy | AUC   | Sensitivity | Specificity | F1     | Kappa  | MCC    |
|-----------------------|-----------------------|-----------|------------|----------|-------|-------------|-------------|--------|--------|--------|
| Undersampling         | balanced_df           | 0.5       | 0.5341     | 0.767   | 0.8341| 0.7159      | 0.8182      | 0.7645 | 0.5341 | 0.5369 |
| Duped Oversampling    | duped_data            | 0.6       | 0.6718     | 0.8981  | 0.8754| 0.9009      | 0.7709      | 0.9448 | 0.2983 | 0.3714 |
| Random Oversampling   |oversampled_random_data| 0.59      | 0.6733     | 0.8996  | 0.8770| 0.9041      | 0.7692      | 0.9457 | 0.3018 | 0.3742 |
| SMOTE                 | smote_data            | 0.62      | 0.6815     | 0.9120  | 0.8908| 0.9168      | 0.7647      | 0.9528 | 0.3186 | 0.3871 |
| ADASYN                | ADASYN_data           | 0.61      | 0.6701     | 0.912   | 0.8966| 0.9171      | 0.7529      | 0.9528 | 0.3150 | 0.3818 |





