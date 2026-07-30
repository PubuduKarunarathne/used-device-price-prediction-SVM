# Used Device Price Prediction

This machine learning project predicts the normalized used prices of devices based on various hardware specifications (such as RAM, battery, and camera megapixels). 

## Data Preprocessing
* **Imputation:** Missing values in the `rear_camera_mp` column were imputed using a `KNeighborsRegressor` pipeline. 
* **Scaling & Encoding:** Numerical features were standardized using `StandardScaler`, and categorical features (like device brand and OS) were processed using `OneHotEncoder`.

## Model Architecture
The core of the prediction engine is a Support Vector Machine (SVM). 
* **Algorithm:** Support Vector Regressor (`SVR`)
* **Kernel:** Radial Basis Function (RBF)
* **Hyperparameters:** `C=1.0`, `epsilon=0.1`

## Model Performance
The SVM pipeline was evaluated on a 20% test split, yielding the following metrics:
* **R-squared ($R^2$):** 0.8442
* **Mean Absolute Error (MAE):** 0.1756
* **Mean Squared Error (MSE):** 0.0506

## Files Included
* `used_device_data.xls` - The raw dataset.
* `preprocessed_used_device_data.xls` - The cleaned and preprocessed dataset.
* `svm_predictions_plot.png` - Scatter plot visualization of actual vs. predicted prices.