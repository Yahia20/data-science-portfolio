# DVD Rental Duration Prediction

## Project Overview
A DVD rental company wants to predict how many days a customer will rent a DVD based on various features. The goal is to develop a regression model with a Mean Squared Error (MSE) of 3 or less on the test set. This will help the company optimize its inventory planning.

## Dataset
The dataset (`rental_info.csv`) contains information about DVD rentals, including:
- **rental_date**: Date and time of rental.
- **return_date**: Date and time of return.
- **amount**: Amount paid for rental.
- **rental_rate**: Rental rate of the DVD.
- **release_year**: Release year of the movie.
- **length**: Length of the movie in minutes.
- **replacement_cost**: Cost to replace the DVD.
- **special_features**: Special features available (e.g., Deleted Scenes, Behind the Scenes).
- **Movie Ratings**: Dummy variables for movie ratings (NC-17, PG, PG-13, R).

## Features and Target
- **Target Variable**: `rental_length_days` (computed as `return_date - rental_date` in days)
- **Feature Engineering**:
  - Extracted rental duration.
  - Created dummy variables for special features.
  - Dropped redundant squared features.

## Models Implemented
The following regression models were tested:
- **Linear Regression**
- **Lasso Regression**
- **Ridge Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **Gradient Boosting Regressor**

## Performance Evaluation
Each model was evaluated using:
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**
- **R² Score**

Additionally, **K-Fold Cross-Validation** was performed to ensure model stability.

## Results
The best-performing model was selected based on MSE and overall performance. The boxplot visualization compared the cross-validation scores of all models.

## How to Run the Project
1. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```
2. Run the Python script:
   ```bash
   python rental_prediction.py
   ```
3. View model evaluation results and visualization outputs.

## Conclusion
This project helps the DVD rental company predict rental durations, allowing better inventory planning. The best-performing model ensures accuracy with an MSE below 3, meeting business requirements.

## Future Improvements
- **Feature Engineering**: Add customer demographics and movie genres.
- **Advanced Models**: Try XGBoost or Neural Networks.
- **Hyperparameter Tuning**: Use GridSearchCV for better optimization.

