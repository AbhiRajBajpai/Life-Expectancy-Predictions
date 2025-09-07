# TCS Stock Analysis and Price Prediction 📈

## Introduction
This project performs a comprehensive analysis of the historical stock data for Tata Consultancy Services (TCS), one of the largest IT services companies in the world. The goal is to gain insights from historical price and corporate action data, and then build a predictive model using a Long Short-Term Memory (LSTM) neural network to forecast future stock prices.

---

## Datasets Used
This project utilizes three distinct datasets to provide a holistic view of TCS's stock performance:

1.  **`TCS_stock_history.csv`**: Contains daily time-series data, including the open, high, low, and closing prices, as well as trading volume.
2.  **`TCS_stock_action.csv`**: Details corporate actions such as dividend payments and stock splits on specific dates.
3.  **`TCS_stock_info.csv`**: A summary file with general, static information about the company.

---

## Project Workflow
The analysis is structured in a step-by-step manner, from data exploration to predictive modeling.

### 1. Data Loading & Preprocessing
- All three datasets are loaded into pandas DataFrames.
- The 'Date' columns are converted to a proper `datetime` format to enable time-series analysis.

### 2. Exploratory Data Analysis (EDA)
- **Corporate Actions**: The `TCS_stock_action.csv` data is analyzed to visualize the history of dividend payments and identify any stock splits.
- **Historical Trends**: The `TCS_stock_history.csv` data is plotted to visualize the long-term trend of the closing price and trading volume.
- **Integrated Analysis**: The dividend payment dates are overlaid on the historical price chart to visually correlate corporate actions with price movements.

### 3. Predictive Modeling with LSTM
- **Data Preparation**: The closing price data is scaled and transformed into sequences suitable for a time-series model (a 60-day window is used to predict the next day's price).
- **Model Architecture**: A Long Short-Term Memory (LSTM) model is built using TensorFlow/Keras. LSTMs are specifically designed to recognize patterns in sequential data, making them ideal for stock price forecasting.
- **Training**: The model is trained on the first 80% of the historical data.

### 4. Evaluation & Visualization
- The trained model is used to make predictions on the remaining 20% of the dataset (the test set).
- The predicted prices are plotted against the actual prices to visually assess the model's performance in tracking the stock's trend.

---

## How to Run This Project
1.  **Prerequisites**: Ensure you have Python and the following libraries installed:
    ```
    pip install pandas numpy matplotlib seaborn scikit-learn tensorflow
    ```
2.  **Data**: Place the three CSV files (`TCS_stock_history.csv`, `TCS_stock_action.csv`, `TCS_stock_info.csv`) in the same directory as your script or Jupyter notebook.
3.  **Execution**: Run the cells in the notebook sequentially to perform the analysis and train the model.

---

## Tools and Libraries
- **Python 3**
- **Pandas**: For data manipulation and analysis.
- **Matplotlib & Seaborn**: For data visualization.
- **Scikit-learn**: For data preprocessing (MinMaxScaler).
- **TensorFlow (Keras)**: For building and training the LSTM model.
