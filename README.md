
# Global Volatility Prediction

## Overview

This project focuses on predicting stock market volatility across global financial markets using **GARCH models**. 
The predictions aim to aid traders, analysts, and researchers in better understanding the risks and volatility associated with specific stock exchanges worldwide.

The data for this project was sourced from Yahoo Finance (via the `yfinance` library) and spans multiple international stock exchanges.

## Stock Exchanges Included
1. **Bucharest Stock Exchange**
2. **Cairo Stock Exchange**
3. **Hong Kong Stock Exchange**
4. **Tel Aviv Stock Exchange**
5. **Warsaw Stock Exchange**

Each stock exchange has its own dataset and dedicated GARCH model notebook.

---

## Project Structure

### Data
The `Data/` directories contain historical stock price data for various indices and stocks. These datasets are used to train and validate the GARCH models. 

### Models
The `Model/` directories include Jupyter notebooks implementing **GARCH (Generalized Autoregressive Conditional Heteroskedasticity)** models. Each notebook performs the following:
- Data preprocessing (e.g., handling missing values, generating returns).
- Model training for volatility prediction.
- Visualization of results, including volatility forecasts.

### Directory Layout
```plaintext
Global-Volatile-Prediction-main/
├── Bucharest/
│   ├── Data/
│   │   └── BUX_stock_data.csv
│   ├── Model/
│       └── BUCHAREST_GARCH_Model.ipynb
├── Cairo/
│   ├── Data/
│   │   └── egx_stock_data.csv
│   ├── Model/
│       └── CAIRO_GARCH_Model.ipynb
├── Hong Kong/
│   ├── Data/
│   │   └── hk_stock_data.csv
│   ├── Model/
│       └── HONG_KONG_GARCH_Model.ipynb
├── Tel Aviv/
│   ├── Data/
│   │   └── tase_stock_data.csv
│   ├── Model/
│       └── ISRAEL_GARCH_Model.ipynb
├── Warsaw/
│   ├── Data/
│   │   ├── KGH.WA_historical_data.csv
│   │   ├── PEO.WA_historical_data.csv
│   │   ├── PKN.WA_historical_data.csv
│   │   ├── PKO.WA_historical_data.csv
│   │   └── PZU.WA_historical_data.csv
│   ├── Model/
│       └── Warsaw Stock Exchange Garch Model.ipynb
```

---

## Requirements

The following Python libraries are required to run the notebooks:
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `arch`
- `yfinance`
- `scipy`

Install the dependencies using:
```bash
pip install -r requirements.txt
```

---

## How to Use

1. **Data Inspection**: Explore the datasets in the `Data/` directories for each stock exchange.
2. **Model Execution**: Run the Jupyter notebooks in the `Model/` directories to:
   - Preprocess the data.
   - Train GARCH models on the stock price data.
   - Visualize the volatility forecasts.

---

## Methodology

### Data Preprocessing
- Historical stock data was downloaded via the `yfinance` API.
- Adjusted close prices were used to calculate daily returns.

### Model Selection
- GARCH models were selected to predict conditional volatility, given their effectiveness in modeling financial time series data.

### Outputs
- Volatility forecasts for each stock exchange.
- Plots of predicted vs actual volatility trends.

---

## Acknowledgments
- **Yahoo Finance**: Data source via the `yfinance` Python library.
- **GARCH Modeling**: Implemented using the `arch` library.
- Contributors: This repository is maintained by a passionate data scientist specializing in financial markets.

---

## License
This project is licensed under the MIT License.
