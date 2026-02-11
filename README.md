# ML Stock Price Prediction (95% Accuracy)

Machine learning model predicting next-day stock prices for Japanese equities using linear regression and technical indicators.

## 📊 Results

- **Accuracy:** 95.11% R² on test data
- **Error Rate:** 2.16% mean absolute error
- **Dataset:** Toyota Motor Corporation (7203.T), 2020-2024

## 🎯 Methodology

### Data
- Source: Yahoo Finance API
- Ticker: 7203.T (Toyota Motor Corporation)
- Period: January 2020 - December 2024
- Samples: 1,202 trading days

### Features (8 total)
- Lagged prices (1, 2, 5 days)
- Moving averages (5, 10, 20 days)
- Price returns
- Volume moving average

### Model
- **Algorithm:** Linear Regression
- **Split:** 80% training (961 days), 20% testing (241 days)
- **Validation:** Time-series split (no data leakage)

## 🔍 Key Findings

1. **Linear Regression outperformed Random Forest**
   - Initially tried Random Forest → severe overfitting (test R² = -0.97)
   - Switched to Linear Regression → 95% accuracy
   
2. **Simplicity beats complexity**
   - Complex models memorize noise
   - Simple models learn true patterns

3. **Feature engineering matters**
   - Lagged prices most predictive
   - Moving averages capture trends
   - Volume provides additional signal

## 💻 Technologies

- Python 3.x
- pandas, numpy
- scikit-learn
- yfinance
- matplotlib

## 🚀 Usage
```python
# Clone repository
git clone https://github.com/arihantlodha-cmd/ML-Stock-Price-Prediction

# Install dependencies
pip install pandas numpy scikit-learn yfinance matplotlib

# Run Jupyter notebook
jupyter notebook toyota-stock-ml-prediction.ipynb
```

## 📝 Future Improvements

- Test on multiple stocks (Sony, Nintendo, SoftBank)
- Implement LSTM neural networks
- Add macroeconomic indicators
- Deploy as web application

## 👨‍💻 Author

**Arihant Lodha**
- Interested in quantitative finance and machine learning


## 📄 License

MIT License - feel free to use for learning purposes

---

*Built as part of independent quantitative finance research exploring ML applications in Asian equity markets.*
```
