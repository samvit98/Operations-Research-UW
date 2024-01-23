**Multi-Variable Regression Model README**

This Python script implements a multi-variable regression model using the Statsmodels library for analyzing diamond prices. The model is built to predict diamond prices based on various features such as carat weight, color, cut, clarity, and more.

**File Structure:**
- `multi_variable_regression_model.py`: Python script containing the regression model implementation.
- `UV6248-XLS-ENG.xls`: Excel file containing raw diamond data.
- `Sarah_gets_diamond_model_output.csv`: Output CSV file with predicted prices.

**Dependencies:**
- `pandas`: Data manipulation and analysis library.
- `numpy`: Mathematical functions for numerical operations.
- `statsmodels`: Library for estimating and testing statistical models.
- `plotly.express`: Library for interactive data visualization.
- `sklearn`: Machine learning library for data preprocessing.

**Functions:**
1. **load_data:**
   - Loads data from an Excel file.
   - Parameters: `file_path` (str), `sheet_name` (str), `skip_rows` (int).

2. **preprocess_data:**
   - Handles missing values and transforms features.
   - Log-transforms 'Price' and 'CaratWeight'.
   - One-hot encodes 'Color' and 'Report' columns.
   - Replaces values in categorical features using mapping scales.
   - Calculates Variance Inflation Factor (VIF) before and after data transformation.

3. **build_lm_model:**
   - Builds a linear regression model.
   - Parameters: `X` (pd.DataFrame), `Y` (pd.DataFrame).

4. **visualize_residual_plot:**
   - Visualizes a residual plot.
   - Parameters: `results` (pd.DataFrame).

5. **perform_cross_validation:**
   - Performs cross-validation.
   - Parameters: `X_train` (pd.DataFrame), `X_test` (pd.DataFrame), `Y_train` (pd.DataFrame), `Y_test` (pd.DataFrame).

**Execution Steps:**
1. Load raw data from the Excel file using `load_data`.
2. Preprocess the data to handle missing values and transform features with `preprocess_data`.
3. Build a linear regression model using `build_lm_model`.
4. Visualize the residual plot with `visualize_residual_plot`.
5. Perform cross-validation using `perform_cross_validation`.
6. Use the trained model to predict prices for a final test dataset.
7. Save the predicted prices in the output CSV file.

**Output:**
- The script generates a summary of the regression model, a residual plot, and predictions for the final test dataset.
- The final predictions are saved in the `Sarah_gets_diamond_model_output.csv` file.

**Note:**
- Ensure all dependencies are installed before running the script.
- The script uses a provided Excel file (`UV6248-XLS-ENG.xls`) as input for diamond data.
- Adjust file paths and names as needed for your environment.