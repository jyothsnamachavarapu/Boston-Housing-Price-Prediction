# Boston Housing Price Prediction

## Abstract
This study evaluates the Boston Housing dataset to forecast property values using machine learning techniques. The dataset, sourced from the UCI Machine Learning Repository, includes attributes like per capita crime rates, residential zoning proportions, nitric oxide levels, and median owner-occupied home values. Through meticulous preprocessing, the dataset was refined to ensure completeness, handle outliers, and enhance model robustness.

We applied multiple regression models, including Linear Regression, Random Forest, Decision Tree, K-Nearest Neighbors, XGBoost, Gradient Boosting, and AdaBoost. Among these, the **Random Forest** model emerged as the most effective, achieving the lowest Mean Squared Error (MSE), Mean Absolute Error (MAE), and the highest R-squared value, signifying its accuracy and reliability. Exploratory data analysis revealed the significant impact of variables like the number of rooms per dwelling and the percentage of lower-status population on housing price predictions. 

Cross-validation further validated the robustness of the Random Forest model, which demonstrated strong generalization across different subsets of data. The model was ultimately applied to real-world price predictions, showcasing its practical utility for real estate stakeholders and policymakers.

---

## Key Features
- **Dataset**: Boston Housing dataset from the UCI Machine Learning Repository (506 entries, 14 attributes).
- **Models Evaluated**: 
  - Linear Regression
  - Random Forest
  - Decision Tree
  - K-Nearest Neighbors
  - XGBoost
  - Gradient Boosting
  - AdaBoost
- **Best Model**: Random Forest (Highest R²: 0.866, Lowest RMSE: 2.383).
- **Key Predictive Features**:
  - **RM**: Average number of rooms per dwelling.
  - **LSTAT**: Percentage of lower socio-economic status population.
  - **NOX**: Nitric oxide concentration.
- **Performance Metrics**: Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared (R²).

---

## Methodology
### 1. Data Collection
- Source: UCI Machine Learning Repository.
- Includes 506 entries and 14 features related to socio-economic, demographic, and environmental factors.

### 2. Data Preprocessing
- **Missing Values**: Dataset contained no missing values.
- **Outlier Handling**: Statistical checks employed to detect and mitigate outliers.
- **Normalization**: Standardized feature scaling for consistency.
- **Exploratory Data Analysis (EDA)**:
  - Correlation matrices to identify key relationships.
  - Scatter plots and heatmaps for visual insights.

### 3. Model Development and Evaluation
- **Training/Testing Split**: Data split into 80% training and 20% testing sets.
- **Cross-Validation**: K-fold cross-validation to ensure robustness.
- **Feature Importance**:
  - Random Forest and Gradient Boosting identified key predictors like RM and LSTAT.
- **Model Comparison**:
  - Metrics: MAE, MSE, and R² used to assess model precision and explanatory power.

### 4. Results
- **Random Forest**:
  - Best performance (R²: 0.866, RMSE: 2.383).
  - Robust against overfitting, effectively captures non-linear relationships.
- **Gradient Boosting**:
  - R²: 0.634, proficient in predictive accuracy with moderate error rates.
- **AdaBoost**:
  - Moderate accuracy (R²: 0.706) but effective in ensemble regression.
- **Other Models**: Linear Regression, Decision Trees, and KNN provided useful comparative baselines.

---

## Results Summary
| Model             | R²   | MAE   | MSE   | RMSE  |
|-------------------|-------|-------|-------|-------|
| Random Forest     | 0.866 | 1.732 | 5.679 | 2.383 |
| Gradient Boosting | 0.634 | 2.104 | 8.625 | 2.937 |
| AdaBoost          | 0.706 | 2.004 | 7.921 | 2.812 |

---

## Best Model: Random Forest
- **R²**: 0.866
- **RMSE**: 2.383
- **Key Predictors**:
  - RM: Positive correlation with housing prices (larger living spaces fetch higher values).
  - LSTAT: Negative correlation (areas with lower socio-economic status have lower property values).

Visualizations:
- Actual vs. Predicted Prices.
- Residual Analysis (Residuals vs. Fitted Values).

---

## Insights and Applications
- The study reveals the critical role of socio-economic and residential features in determining housing prices.
- RM and LSTAT emerged as the most influential predictors, with significant implications for urban planning and housing policies.
- Random Forest was the most effective model, combining high accuracy with robustness against overfitting.

---

## Future Directions
1. **Advanced Ensemble Techniques**:
   - Explore model stacking or blending to combine the strengths of individual models.
2. **Enhanced Feature Engineering**:
   - Include additional data like proximity to schools, public transportation, and amenities.
   - Develop interaction terms and polynomial features to capture complex patterns.
3. **Deep Learning**:
   - Investigate neural networks for improved handling of non-linearities and feature interactions.
4. **Temporal Analysis**:
   - Study temporal changes in economic conditions and their effects on housing markets.
5. **Robustness Checks**:
   - Conduct sensitivity analyses to evaluate model stability under varying conditions.

---

## References
1. Harrison, D., & Rubinfeld, D. L. (1978). "Hedonic Housing Prices and the Demand for Clean Air." *Journal of Environmental Economics and Management*, 5(1), 81-102.
2. Quinlan, J. R. (1993). "Combining Instance-Based and Model-Based Learning." *Machine Learning*, 2, 75-80.
3. Belsley, D. A. (1991). "Conditioning Diagnostics: Collinearity and Weak Data in Regression." *John Wiley & Sons*.

---

## License
This project is licensed under the MIT License. See `LICENSE` for details.
