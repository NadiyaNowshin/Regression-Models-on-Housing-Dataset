# Boston Housing Price Prediction

## Project Overview

This project explores **regression-based machine learning models** using the Boston Housing dataset. The goal is to predict the median value of owner-occupied homes (`MEDV`) based on a set of socioeconomic, environmental, and housing-related features.

Three regression algorithms are trained and evaluated:

* **Linear Regression**
* **Ridge Regression**
* **Lasso Regression**

The models are compared using multiple regression evaluation metrics, including **Mean Squared Error (MSE), Root Mean Squared Error (RMSE), R² Score, and Mean Absolute Error (MAE)**.

## Dataset

The dataset is loaded directly from the following URL:

[Boston Housing Dataset](https://raw.githubusercontent.com/jbrownlee/Datasets/master/housing.data)

Unlike many datasets, this file does not contain column headers. The appropriate feature names are therefore assigned during data loading.

### Features

| Feature   | Description                                                       |
| --------- | ----------------------------------------------------------------- |
| `CRIM`    | Per capita crime rate by town                                     |
| `ZN`      | Proportion of residential land zoned for lots over 25,000 sq. ft. |
| `INDUS`   | Proportion of non-retail business acres per town                  |
| `CHAS`    | Charles River dummy variable                                      |
| `NOX`     | Nitric oxide concentration                                        |
| `RM`      | Average number of rooms per dwelling                              |
| `AGE`     | Proportion of owner-occupied units built before 1940              |
| `DIS`     | Weighted distance to employment centers                           |
| `RAD`     | Index of accessibility to radial highways                         |
| `TAX`     | Full-value property tax rate                                      |
| `PTRATIO` | Pupil-teacher ratio by town                                       |
| `B`       | Proportion of Black residents                                     |
| `LSTAT`   | Percentage of lower-status population                             |
| `MEDV`    | Median value of owner-occupied homes                              |

The target variable for the regression task is **`MEDV`**.

## Project Objectives

The main objectives of this project are to:

* Load and prepare the Boston Housing dataset
* Separate features and target variables
* Split the dataset into training and testing sets
* Train multiple regression models
* Generate predictions on the test set
* Evaluate model performance using multiple regression metrics
* Compare the performance of Linear, Ridge, and Lasso Regression

## Methodology

### 1. Data Loading

The dataset is loaded directly from the provided URL using Pandas.

Since the original dataset does not include column headers, the appropriate column names are assigned manually.

```python
data_url = "https://raw.githubusercontent.com/jbrownlee/Datasets/master/housing.data"
```

### 2. Feature and Target Separation

The dataset is divided into:

**Features (`X`)**

All columns except `MEDV`.

**Target (`y`)**

The `MEDV` column, representing the median value of owner-occupied homes.

### 3. Train-Test Split

The dataset is divided into training and testing subsets using an **80/20 split**.

* **80%** of the data is used for training
* **20%** of the data is used for testing

`train_test_split` from Scikit-learn is used for this process.

### 4. Regression Models

Three regression algorithms are trained on the training dataset.

#### Linear Regression

Linear Regression models the relationship between the input features and the target variable using a linear function.

#### Ridge Regression

Ridge Regression is a regularized form of Linear Regression that adds an L2 penalty to help control the magnitude of model coefficients.

#### Lasso Regression

Lasso Regression uses L1 regularization, which can reduce some feature coefficients toward zero while fitting the model.

## Model Evaluation

Each model is evaluated using the following metrics:

### Mean Squared Error (MSE)

Measures the average squared difference between actual and predicted values. Lower values indicate smaller prediction errors.

### Root Mean Squared Error (RMSE)

RMSE is the square root of MSE and represents the error in the same units as the target variable.

### R² Score

R² measures how much of the variation in the target variable is explained by the model. A value closer to 1 indicates that the model explains a larger proportion of the observed variance.

### Mean Absolute Error (MAE)

MAE measures the average absolute difference between actual and predicted values. Lower values indicate better predictive accuracy.

## Results

The performance of the three regression models is compared using a results table.

| Model             | MSE | RMSE | R² | MAE |
| ----------------- | --: | ---: | -: | --: |
| Linear Regression |   — |    — |  — |   — |
| Ridge Regression  |   — |    — |  — |   — |
| Lasso Regression  |   — |    — |  — |   — |

The values above can be updated with the results generated by the notebook.

## Technologies Used

* **Python**
* **Google Colab**
* **Pandas**
* **NumPy**
* **Scikit-learn**

## Project Structure

```text
Boston-Housing-Regression/
│
├── Boston_Housing_Regression.ipynb
├── housing.data
└── README.md
```

## How to Run

### Google Colab

Open the `.ipynb` notebook in Google Colab and run the cells sequentially.

The dataset can be loaded directly from the provided URL, so a local copy of the dataset is not necessarily required.

### Local Environment

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

Navigate to the project directory:

```bash
cd YOUR_REPOSITORY
```

Install the required libraries:

```bash
pip install pandas numpy scikit-learn
```

Then open the notebook using Jupyter Notebook or JupyterLab.

## Author

**Nadiya Nowshin**
