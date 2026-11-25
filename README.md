# Medical Insurance Premium Prediction

## Project Overview
This project uses supervised machine learning to predict an individual's annual medical insurance premium (USD) from demographic, lifestyle, and health-related attributes. The goal is to build an interpretable regression model that can support transparent premium estimation.

**Target variable:** `annual_premium`

## Dataset
The notebook works with a CSV file named `insurance_premium.csv` containing 2,500 records. The dataset is not included in this repository. Add the dataset only if you have the right to share it publicly; otherwise, provide an approved source or keep it private.

Expected input file:
- `insurance_premium.csv`

The notebook currently loads the file using the Google Colab path `/content/insurance_premium.csv`. In Google Colab, upload the CSV with that filename before running the notebook. For local Jupyter use, change the path to the location of your CSV file.

## Workflow
1. Load the data and inspect its structure, data types, summary statistics, and missing values.
2. Explore distributions and relationships using visualisations.
3. Detect and cap outliers using the IQR method.
4. Handle missing values using statistical and KNN imputation approaches.
5. Conduct hypothesis tests for selected categorical features.
6. Encode categorical variables and scale numerical features.
7. Split the data into training, validation, and test sets.
8. Fit and evaluate Linear Regression, Ridge, Lasso, and Elastic Net models.
9. Compare model performance using R-squared, MAE, and RMSE.
10. Review model coefficients and residual behaviour.

## Tools & Libraries
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- SciPy
- Statsmodels
- Scikit-learn
- Jupyter Notebook / Google Colab

## Results
The notebook's recorded evaluation results are:

| Model | Test R² | Test RMSE (USD) | Test MAE (USD) |
|---|---:|---:|---:|
| Linear Regression | 0.868 | 2,658.30 | 1,878.26 |
| Ridge | 0.868 | 2,658.17 | 1,878.32 |
| Lasso | 0.868 | 2,658.18 | 1,878.15 |
| Elastic Net | 0.773 | 3,486.62 | 2,674.56 |

Linear Regression, Ridge, and Lasso performed similarly on the recorded test split. The Linear Regression model achieved an R² of approximately 0.868, meaning it explained about 86.8% of the variation in the test-set premiums for this dataset.

## Key Observations
- Smoking status, age, BMI, and chronic conditions were identified in the notebook as important premium-related factors.
- The Linear Regression, Ridge, and Lasso models had similar recorded test performance.
- Elastic Net performed less strongly on this particular test split.

## How to Run
1. Clone or download this repository.
2. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open `medical_insurance_premium_prediction.ipynb` in Jupyter Notebook or Google Colab.
4. Make the dataset available as `insurance_premium.csv`.
5. Run the notebook cells from top to bottom.

## Important Note
This is an educational portfolio project, not a production insurance pricing system. Results depend on the dataset and split used. Review the preprocessing workflow for data leakage and use a train-fitted preprocessing pipeline before treating the model as production-ready.

## Author
**Divya Tembhekar**

GitHub: https://github.com/DivyaTembhekar
