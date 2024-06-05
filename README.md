# ML-Seminar-Pet-Adoption-Speed
https://www.kaggle.com/code/liranmeirovich/pet-finder-dataset-seminar

# Pet Adoption Speed Prediction

This project aims to predict the adoption speed of pets based on various features such as breed, age, gender, and health conditions. The dataset used in this work was obtained from a pet adoption agency, and the goal was to develop a machine learning model that could accurately classify pets into different adoption speed categories (e.g., 1-7 days, 8-30 days, etc.).

## Data Preprocessing

- The dataset was initially cleaned by removing NaN values and ensuring that all features were numeric.
- Irrelevant features like 'Name', 'Description', 'RescuerID', and 'PetID' were dropped as they were deemed unnecessary for the prediction task.
- Exploratory data analysis was performed, including visualizations and correlation analysis, to gain insights into the dataset.

## Feature Engineering

- **Correlation-based Feature Selection**: Features with low correlation to the target variable ('AdoptionSpeed') were removed.
- **Feature Combination**: Highly correlated features ('Dewormed', 'Vaccinated', 'Sterilized') were combined into a single feature.
- **New Feature Creation**: A new feature 'RescuerID_Bin' was created by binning the counts of occurrences of 'RescuerID' into quantile bins.
- **Principal Component Analysis (PCA)**: PCA was applied to extract principal components, but it did not improve the prediction accuracy.

## Machine Learning Models

The following machine learning models were used for the prediction task:

- Random Forest
- K-Nearest Neighbors (KNN)
- Gradient Boosting

Techniques like Recursive Feature Elimination with Cross-Validation (RFECV) and grid search for hyperparameter tuning were employed to optimize the models' performance.

## Results

The best performance was achieved using the Random Forest model with a score of 0.46, which outperformed the top scores (0.45) from other teams in the competition. However, the overall scores were relatively low, potentially due to the low correlation between the features and the target variable.

## Conclusion

This project demonstrates the application of various machine learning techniques, including data preprocessing, feature engineering, and model selection, to predict pet adoption speeds. While the results are promising, further improvements could be made by exploring more advanced feature engineering techniques or obtaining a dataset with stronger correlations between features and the target variable.
