

# Activity 2: Simple House Price Prediction

**Course:** Machine Learning [ADPC509]  
**Class:** T.Y. B.Tech (AI & DS)  
**Academic Year:** 2026-27  
**Department:** Artificial Intelligence & Data Science  
**Institution:** Zeal College of Engineering and Research (ZCOER), Pune

## 📌 Project Overview

This project focuses on building a **Simple Linear Regression model** to predict house prices using the Boston Housing dataset.

The dataset contains information about housing characteristics, including the average number of rooms per dwelling. In this activity, the `RM` feature is used to predict the median value of owner-occupied homes, represented by the `MEDV` target column.

The notebook covers dataset inspection, feature selection, visualization, train-test splitting, model training, prediction, evaluation, and a new example prediction.

## 🎯 Objectives

- Load and inspect the dataset
- Identify an input feature and a continuous numerical target
- Visualize the relationship between the feature and house price
- Split the data into training and testing sets
- Train a Simple Linear Regression model
- Record the model coefficient, intercept, and equation
- Generate predictions on test data
- Evaluate the model using MAE, MSE, RMSE, and R²
- Visualize actual versus predicted prices
- Predict the price for a new example and discuss model limitations

## 📂 Dataset Information

| Property | Description |
|---|---|
| Dataset | Boston Housing Dataset |
| Source | [Kaggle - Boston housing dataset](https://www.kaggle.com/datasets/altavish/boston-housing-dataset) |
| Original rows | 506 |
| Original columns | 14 |
| Data type | Numerical housing and neighborhood data |
| Input feature | `RM` |
| Target column | `MEDV` |
| Feature description | Average number of rooms per dwelling |
| Target description | Median value of owner-occupied homes, in thousands of dollars |

## 🛠️ Tools and Libraries

- Python
- Google Colab / Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

## 🔍 Simple Linear Regression Steps

### Step 1: Select and Understand the Dataset

The Boston Housing dataset was selected for this activity. The dataset contains numerical information related to housing and neighborhood characteristics.

The `RM` column was selected as the input feature, while `MEDV` was selected as the continuous numerical target to be predicted.

### Step 2: Load and Inspect the Dataset

The dataset was loaded using Pandas. The first and last records, dataset shape, column names, data types, summary statistics, missing values, and duplicate records were inspected.

The dataset contains 506 rows and 14 columns. Missing values were identified and handled using the median of their respective columns before model training.

### Step 3: Select Input Features and Target

The input feature was selected as:

- `X = RM`

The target variable was selected as:

- `y = MEDV`

The average number of rooms may be related to house value, making it suitable for an initial simple regression model.

### Step 4: Visualize the Relationship

A scatter plot was created to examine the relationship between `RM` and `MEDV`.

The graph includes a title, axis labels, and grid lines. The visualization helps identify whether house value tends to increase or decrease as the average number of rooms changes.

A visible relationship does not by itself prove that the number of rooms causes a change in house price.

### Step 5: Split the Dataset

The dataset was divided into training and testing sets using an **80:20 split**.

- Training data: 80%
- Testing data: 20%
- `random_state = 42`

The training data was used to learn the model parameters, while the testing data was used to evaluate the model on unseen observations.

### Step 6: Train the Linear Regression Model

A Linear Regression model was trained using the training data.

The learned model parameters were:

| Parameter | Value |
|---|---:|
| Intercept | -36.2463 |
| Coefficient / Slope | 9.3483 |

The fitted regression equation is:

```text
MEDV ($1k) = -36.2463 + (9.3483 × RM)
```

The slope represents the estimated change in `MEDV` for a one-unit increase in `RM`. The intercept is the model’s predicted `MEDV` when `RM` is zero.

### Step 7: Generate Predictions

The trained model was used to predict house values for the test dataset.

A sample of actual and predicted values was displayed side by side, along with the difference between them, to examine prediction errors.

### Step 8: Evaluate the Model

The model was evaluated using the following regression metrics:

| Metric | Result |
|---|---:|
| MAE | 4.4783 |
| MSE | 46.1448 |
| RMSE | 6.7930 |
| R² | 0.3708 |

**Interpretation:**

- **MAE:** The model’s predictions differ from actual values by approximately 4.4783 thousand dollars on average.
- **MSE:** The average squared prediction error is 46.1448 in squared target units.
- **RMSE:** The typical prediction error is approximately 6.7930 thousand dollars.
- **R²:** The model explains approximately 37.08% of the variation in the test target values.

These results indicate that `RM` alone provides some predictive information, but it does not explain all the variation in house values.

### Step 9: Visualize Actual Versus Predicted Values

A scatter plot was created to compare actual house values with predicted house values.

The graph includes a reference line representing perfect predictions, where the predicted value equals the actual value.

Points closer to the reference line indicate more accurate predictions. The distance of points from the line shows the prediction errors.

### Step 10: Predict a New Example and Conclude

The trained model was used to predict the house value for a new example with:

```text
RM = 6.5
```

The predicted value was approximately:

```text
MEDV = 24.52 thousand dollars
```

This is equivalent to approximately **$24,517.64**.

The prediction is an estimate from the fitted model and should not be treated as an actual market valuation.

## 📁 Repository Structure

```text
simple_house_price_prediction/
│
├── Activity_2_Simple_House_Price_Prediction.ipynb
├── HousingData.csv
└── README.md
```

## ▶️ How to Run

### Using Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Upload or open `Activity_2_Simple_House_Price_Prediction.ipynb`.
3. Upload `HousingData.csv` when required by the notebook.
4. Run the notebook cells from top to bottom.
5. Review the model equation, predictions, evaluation metrics, and visualizations.
6. The notebook will display the prediction for the new example.

### Using Jupyter Notebook

1. Install Python and Jupyter Notebook, if they are not already installed.
2. Place the notebook and `HousingData.csv` in the same project folder.
3. Open Jupyter Notebook and launch `Activity_2_Simple_House_Price_Prediction.ipynb`.
4. Run the notebook cells from top to bottom.
5. Review the generated outputs and visualizations.

## 📌 Conclusion

A Simple Linear Regression model was developed to predict house values using the average number of rooms per dwelling (`RM`). The dataset was inspected, missing values were handled, and the data was divided into training and testing sets.

The model was trained and evaluated using MAE, MSE, RMSE, and R². The results show that the number of rooms has some predictive value, but the model’s performance is limited because house prices depend on several factors beyond the number of rooms.

This activity provided practical experience in regression, model training, prediction, evaluation, and visualization. A more accurate model could be developed by including additional relevant housing features and comparing multiple regression models.

---

**Author:** Sujay Dharu - Student - Department of AI & DS, ZCOER Pune

