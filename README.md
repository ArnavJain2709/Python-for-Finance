# Python for Finance - Trading Project

A comprehensive collection of financial analysis and machine learning models for stock market prediction and portfolio optimization. This project demonstrates various quantitative finance techniques using Python.

## Project Structure

```text
TradingProj/
├── quantitative-finance-models/
│   ├── blackScholes.ipynb          # Black-Scholes option pricing model
│   ├── index.ipynb                 # Main project overview and examples
│   ├── portfolioOptimisation.ipynb # Modern Portfolio Theory implementation
│   └── stockPriceLSTM.ipynb       # LSTM neural network for stock prediction
├── Docs.docx                      # Project documentation (Word format)
├── .env                           # Environment variables (API keys)
├── .gitignore                     # Git ignore file
└── README.md                      # This file
```

## Folder Organization

### `quantitative-finance-models/` - Financial Models Collection

Complete collection of quantitative finance implementations:

- **blackScholes.ipynb** - Option pricing model
- **index.ipynb** - Project overview and examples  
- **portfolioOptimisation.ipynb** - Modern Portfolio Theory implementation
- **stockPriceLSTM.ipynb** - LSTM neural network for stock prediction

### `Docs.docx` - Project Documentation

Microsoft Word document containing:

- Detailed project specifications
- Mathematical formulations
- Research notes and references
- Implementation guidelines

## Notebooks Overview

### 1. Black-Scholes Model (`blackScholes.ipynb`)

Implementation of the famous Black-Scholes formula for European option pricing.

**Features:**

- Option pricing calculations
- Greeks computation (Delta, Gamma, Theta, Vega, Rho)
- Visualization of option payoffs
- Sensitivity analysis

**Use Case:** Valuing stock options and understanding how various factors affect option prices.

### 2. Portfolio Optimization (`portfolioOptimisation.ipynb`)

Modern Portfolio Theory implementation using real market data to find optimal asset allocations.

**Features:**

- **Data Source:** Yahoo Finance via `yfinance`
- **Assets:** SPY, BND, GLD, QQQ, VTI (ETFs representing different asset classes)
- **Risk-Free Rate:** 10-Year Treasury rate from FRED API
- **Optimization:** Maximizes Sharpe ratio using scipy optimization
- **Metrics:** Expected return, volatility, and Sharpe ratio calculation

**Key Concepts:**

- Covariance matrix calculation
- Efficient frontier theory
- Risk-return optimization
- Diversification benefits

### 3. LSTM Stock Prediction (`stockPriceLSTM.ipynb`)

Deep learning approach to stock price forecasting using Long Short-Term Memory neural networks.

**Features:**

- **Stock:** Apple (AAPL) price prediction
- **Model:** Multi-layer LSTM with TensorFlow/Keras
- **Data Processing:** MinMaxScaler normalization
- **Architecture:** 2 LSTM layers + 2 Dense layers
- **Evaluation:** RMSE and visual comparison

**Technical Details:**

- **Input:** 60-day price sequences
- **Output:** Next day's closing price
- **Training:** 80% of historical data (2012-2020)
- **Testing:** 20% for model validation

### 4. Index Overview (`index.ipynb`)

Project documentation and examples showcasing the main concepts.

## Technologies Used

### Libraries & Frameworks

- **Data Analysis:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `plotly`
- **Machine Learning:** `scikit-learn`, `tensorflow/keras`
- **Financial Data:** `yfinance`, `fredapi`
- **Optimization:** `scipy`

### APIs

- **Yahoo Finance:** Historical stock prices and market data
- **FRED (Federal Reserve):** Economic indicators and risk-free rates

## Getting Started

### Prerequisites

```bash
pip install yfinance pandas numpy matplotlib scikit-learn tensorflow fredapi python-dotenv scipy
```

### Environment Setup

1. Create a `.env` file in the project root
2. Add your FRED API key:

   ```text
   FRED_API_KEY=your_api_key_here
   ```

3. Get your free API key from [FRED](https://fred.stlouisfed.org/docs/api/api_key.html)

### Running the Notebooks

1. **Portfolio Optimization:** Start here for risk-return analysis
2. **Black-Scholes:** For option pricing and derivatives
3. **LSTM Prediction:** For machine learning stock forecasting

## Key Results & Insights

### Portfolio Optimization Results

- **Optimal Sharpe Ratio:** Maximized risk-adjusted returns
- **Asset Allocation:** Data-driven weights for each ETF
- **Risk Metrics:** Quantified portfolio volatility and expected returns

### LSTM Model Performance

- **Prediction Accuracy:** Evaluated using RMSE
- **Visual Validation:** Comparison plots of actual vs predicted prices
- **Time Series Learning:** Model learns patterns from 60-day sequences

## Security & Best Practices

- **API Keys:** Stored securely in `.env` file (not committed to Git)
- **Data Handling:** Proper error handling for API failures
- **Version Control:** `.gitignore` prevents sensitive data exposure

## Educational Value

This project demonstrates:

- **Quantitative Finance:** Portfolio theory, option pricing, risk management
- **Machine Learning:** Time series prediction, neural networks, feature engineering
- **Data Science:** ETL processes, visualization, statistical analysis
- **Software Engineering:** Clean code, documentation, security practices

## Use Cases

1. **Portfolio Management:** Optimize asset allocation for better risk-adjusted returns
2. **Options Trading:** Price derivatives and understand risk factors
3. **Algorithmic Trading:** Use ML predictions for trading strategies
4. **Financial Research:** Analyze market relationships and patterns

## Future Enhancements

- [ ] Additional ML models (Random Forest, XGBoost)
- [ ] Real-time data streaming
- [ ] Backtesting framework
- [ ] Risk management modules
- [ ] Multiple asset LSTM prediction
- [ ] Options strategy analyzer


**Author:** Arnav Jain  
**Repository:** [Python-for-Finance](https://github.com/ArnavJain2709/Python-for-Finance)  
**Contact:** For questions or collaborations, please open an issue.
