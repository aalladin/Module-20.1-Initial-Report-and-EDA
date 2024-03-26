# Module-20.1-Initial-Report-and-EDA
### Customer Churn Prediction in Media Services

**Author**: Murtuza A. Alladin

---

#### Executive Summary

This capstone project aims to predict customer churn for a media service provider using machine learning techniques. The project encompasses the creation of a predictive model, extensive data analysis, and clear communication of findings. The outcome is a robust model that can help the company identify key factors leading to churn and proactively implement retention strategies.

---

#### Rationale

Customer churn is a critical metric that can significantly impact the revenue and growth of a media service provider. Understanding the factors that contribute to churn can empower the company to take effective actions to retain customers and improve service quality. This project is not only a demonstration of predictive modeling but also a crucial business insight tool.

---

#### Research Question

How can we predict the likelihood of a customer churning from a media service provider, and what are the main factors that contribute to their decision to leave?

---

#### Data Sources

The dataset for this project consists of eight CSV files containing customer information and interactions with the media service:

1. `media_customers.csv`: Customer demographics and account information.
2. `media_show_events.csv`: Customer interactions with media shows.
3. `media_subscription_events.csv`: Subscription events, such as sign-ups and cancellations.
4. `media_shows.csv`: Information about media shows available on the service.
5. `media_episodes.csv`: Episode details for the shows.
6. `fact_media_campaign_data.csv`: Media campaign performance data.
7. `dim_media_campaign_data.csv`: Media campaign details.
8. `media_customer_counts.csv`: Aggregated customer interaction counts.

---

#### Methodology

**Data Preprocessing and Feature Engineering**

1. Data Cleaning: Handle missing values and eliminate irrelevant data.
2. Data Integration: Merge multiple datasets to create a comprehensive dataset for modeling.
3. Categorical Encoding: Encode categorical variables using techniques like one-hot encoding.
4. Feature Engineering: Develop new features that can enhance model performance.

**Feature Selection**

1. Chi-Square Test: Employ the chi-square test to select significant categorical features.

**Model Building**

1. Dataset Splitting: Divide the data into training and testing sets.
2. Model Training: Build predictive models using Random Forest and XGBoost.
3. Model Evaluation: Assess the performance of the models using accuracy, precision, recall, and F1-score.

**Visualization**

1. Data Exploration: Visualize the data distribution and relationships using Matplotlib and Seaborn.
2. Feature Importance: Display the importance of different features in the Random Forest model.

---

#### Results

Based on the classification report, we can summarize the key findings as follows:

- **Class 0 (Negative Class)**
  - **Precision**: 76% of the instances predicted as class 0 were actually class 0.
  - **Recall**: 90% of the actual class 0 instances were correctly predicted by the model.
  - **F1-Score**: The balance between precision and recall for class 0 is 83%, which is relatively high.

- **Class 1 (Positive Class)**
  - **Precision**: 67% of the instances predicted as class 1 were actually class 1.
  - **Recall**: 41% of the actual class 1 instances were correctly predicted by the model.
  - **F1-Score**: The balance between precision and recall for class 1 is 51%, indicating a need for improvement in identifying positive cases.

- **Overall Model Performance**
  - **Accuracy**: The model correctly predicted 74% of all cases.
  - **Macro Average**:
    - **Precision**: 72% average precision across both classes.
    - **Recall**: 66% average recall across both classes.
    - **F1-Score**: 67% macro-average F1-score.
  - **Weighted Average**:
    - **Precision**: 73% precision weighted by the number of instances in each class.
    - **Recall**: Matches the overall accuracy of 74%.
    - **F1-Score**: 72% weighted average F1-score, which benefits from the model's performance on the more prevalent class.

These results indicate that while the model has decent performance in predicting non-churners (class 0), it struggles with accurately identifying churners (class 1). Further model refinement and feature engineering may be necessary to improve its predictive power for both classes.

---

#### Next steps

To improve the model's performance, we can explore the following strategies:

1. Perform hyperparameter tuning to optimize the Random Forest and XGBoost models.
2. Investigate alternative feature selection methods to identify the most impactful predictors of churn.
3. Collect additional data that may help in distinguishing between churners and non-churners.
4. Deploy the model to a test environment to monitor its performance on new, real-time data.

Additionally, the company can utilize```markdown
the insights from the predictive model to develop targeted customer retention programs. By understanding the key factors that lead to churn, the company can implement personalized marketing campaigns, enhance customer service efforts, and offer tailored incentives to retain customers at risk of churning.

---
