# House Price Prediction in Taipei

This project uses real estate data from Taipei to predict housing prices. It applies machine learning techniques to model the logarithmic unit price (`log_unit_price`) of properties based on various features.

## Project Goals

- Preprocess and explore real-world housing data
- Apply Target Encoding and Random Forest Regression
- Compare model performance using RMSE
- Visualize insights to better understand pricing factors

## Dataset Description

The dataset includes:

- `district`: The district name (in English)
- `main_building_area`: Main building area of the property
- `auxiliary_area`: Additional building area
- `building_age`: Age of the building
- `total_floors`: Total number of floors
- `log_unit_price`: Log-transformed price per unit area (target variable)

## Exploratory Analysis

### District-wise Average Log Unit Price

![Average Log Unit Price by District](figures/average_log_unit_price_by_town.png)

This bar chart shows the mean `log_unit_price` for each district. Prices are generally higher in central districts like Da'an and Xinyi.

## Modeling

### Target Encoding + Linear Regression

Used target mean encoding for `district`:

- District encoded alone: **RMSE ≈ 0.5148**
- Building age alone: **RMSE ≈ 0.5303**
- Both combined: **RMSE ≈ 0.4869**

### Random Forest Regression

Added more features and tuned model hyperparameters:

- **Final RMSE ≈ 0.3648**

This result indicates Random Forest handled feature interactions better and significantly improved accuracy.

## Conclusion

Random Forest outperforms simple linear models and can model complex relationships in the data. Target Encoding also helped convert categorical variables effectively.

## Next Steps

- Test other models (e.g., Gradient Boosting, XGBoost)
- Incorporate more detailed location data (e.g., coordinates)
- Add external factors like MRT distance, school zones, etc.

## Author

This project was created as part of a data science portfolio showcasing predictive modeling and EDA skills with real-world data.
