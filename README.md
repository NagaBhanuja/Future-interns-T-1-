Here is a suggested content structure for your project's **README.md** file. You can copy and paste this text into your notepad and then modify the details (like model metrics and file paths) as you set up your GitHub repository.

-----

# Sales Retail Time Series Forecasting with XGBoost (FI T-1) 📈

## Project Overview

This project implements a machine learning approach for **time series forecasting** of daily retail sales (`venda`). It uses the powerful **XGBoost Regressor** model, leveraging **feature engineering** on date/time attributes to capture seasonality and temporal trends in the data.

## Goal

To build an accurate model to forecast daily sales, providing key insights into the most predictive factors affecting retail performance.

## 📁 Repository Structure

The core of this project is contained within a single Jupyter Notebook:

  * **`Future_interns(T_1).ipynb`**: The main notebook containing all data preparation, feature engineering, model training, prediction, and evaluation steps.
  * **`mock_kaggle (2).csv`**: The raw dataset used for forecasting.

## 🛠️ Installation and Setup

To run this project locally, you'll need the following:

1.  **Python 3.x**

2.  **Jupyter Notebook** or **Google Colab** (recommended, as used for development)

3.  **Required Libraries**: Install the necessary packages using pip:

    ```bash
    pip install pandas numpy xgboost scikit-learn matplotlib seaborn
    ```

## 🚀 Usage

1.  **Clone the Repository**:
    ```bash
    git clone [Your Repository URL]
    cd [Your Repository Name]
    ```
2.  **Download Data**: Ensure the `mock_kaggle (2).csv` file is in your project's root directory.
3.  **Run the Notebook**: Open the `Future_interns(T_1).ipynb` file in your preferred Jupyter environment and run all cells sequentially.

## 📊 Methodology Highlights

  * **Data Preparation**: The `data` column was converted to a datetime object, and the dataset was split into a training set (up to `2015-04-04`) and a test set (after `2015-04-04`).
  * **Feature Engineering**: Essential time-based features were created to help the model learn patterns:
      * `hour`, `dayofweek`, `quarter`, `month`, `year`, `dayofyear`, `dayofmonth`.
  * **Modeling**: An **XGBoost Regressor** was trained to predict the `venda` (sales) column using the engineered features plus `estoque` (stock) and `preco` (price).

## 💡 Key Results

The model achieved strong performance on the test set:

| Metric                             | Value |
|
| **Root Mean Squared Error (RMSE)** | **8.44** |
| **$R^2$ Score**                    | **0.99** |
| **Mean Squared Error (MSE)**       | **71.28** |
| **Mean Absolute Error (MAE)**      | **2.51** |

### Feature Importance

The analysis of feature importance shows the key drivers of sales predictions:


### Forecast Visualization

The model's predictions closely track the actual sales data:

You can view and run the full project directly in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]([YOUR_ACTUAL_COLAB_NOTEBOOK_LINK_HERE])

-----