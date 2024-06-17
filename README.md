# Bakery Sales Forecasting with LSTM

This project is part of a competition where the goal is to predict the daily sales quantities of various bakery items across three different outlets of a bakery shop. The task is to use historical sales data from January 1st to May 31st, 2024, to forecast the sales for each item from June 1st to June 14th, 2024, for each store. Accurate demand forecasting in this context helps optimize inventory levels, reduce waste, and enhance customer satisfaction by consistently offering fresh products.

## Data

The data for this project is provided in several CSV files:

- `historical_data.csv`: Contains the historical sales data, including transaction ID, date, time, quantity, store ID, product ID, and unit price.

- `product_descriptions.csv`: Contains descriptions of the products, including product ID, category, type, and detail.

- `submission_key.csv`: Template for the competition submission, including ID (assigned for the respective date, shop, and product combination), transaction date, store ID, and product ID.

- `submission_format.csv`: Format required for the submission. The csv generated at the end of torch-lstm v3 and v4 are of this format. 


The data was preprocessed using `data-preprocessor.ipynb`. Additional feature engineering was performed using data from `product_features.csv`.

## Model Development

The project started with a Keras LSTM model (`keras-lstm.ipynb`). The model was then iteratively improved and reimplemented in PyTorch (`torch-lstm-v1.ipynb` to `torch-lstm-v4.ipynb`). Each version introduced improvements and optimizations over the previous one. The third version (`torch-lstm-v3.ipynb`) was the first to achieve satisfactory results and was used to make the initial submission. The fourth version (`torch-lstm-v4.ipynb`) incorporated additional feature engineering, resulting in a slight increase in performance.
