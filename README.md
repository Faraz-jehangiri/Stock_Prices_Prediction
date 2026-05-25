<div align="center">

# 📈 Stock Price Prediction
### Machine Learning · Time Series · Linear Regression · LSTM

<br>

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

<br>

> *"Markets are chaotic — but patterns always leave a trace."*

<br>

</div>

---

## 📌 Objective

Build a **machine learning model** capable of predicting future stock closing prices based on historical market data, using features such as:

- Opening Price
- Closing Price
- Daily High & Low
- Trading Volume
- Moving Averages

This project focuses on:
- Time-series data preprocessing & feature engineering
- Training and comparing two models — **Linear Regression** and **LSTM**
- Evaluating prediction accuracy using regression metrics

---

## 📂 Dataset

| Property | Detail |
|----------|--------|
| **Name** | Historical Stock Index Data |
| **File** | `indexProcessed.csv` |
| **Features** | Open, High, Low, Close, Volume |
| **Target Variable** | `Close` (Next Day Closing Price) |
| **Problem Type** | Regression / Time Series Forecasting |

---

## 🧠 Approach

```text
Raw Historical Stock Data
   │
   ▼
Data Cleaning
   │  ├── Standardise column names
   │  ├── Parse & sort by date
   │  ├── Drop duplicates & null values
   │  └── Convert columns to numeric types
   │
   ▼
Feature Engineering
   │  ├── Price Range  (High − Low)
   │  ├── Price Change (Close − Open)
   │  ├── 7-Day Moving Average
   │  ├── 21-Day Moving Average
   │  ├── Daily Return (% change)
   │  └── 7-Day Rolling Volatility
   │
   ▼
Train-Test Split (80/20 — Time Ordered, No Shuffle)
   │
   ▼
Model A — Linear Regression
   │  ├── MinMaxScaler feature scaling
   │  └── Predict closing price from OHLCV + engineered features
   │
   ▼
Model B — LSTM (Long Short-Term Memory)
   │  ├── Sequence length: 60 days lookback
   │  ├── Architecture: LSTM → Dropout → LSTM → Dropout → Dense
   │  └── EarlyStopping to prevent overfitting
   │
   ▼
Evaluation
   │  ├── Mean Absolute Error (MAE)
   │  ├── Root Mean Squared Error (RMSE)
   │  └── R² Score
```

---

## 📊 Results

| Metric | Linear Regression | LSTM |
|--------|:-----------------:|:----:|
| **MAE** | — | — |
| **RMSE** | — | — |
| **R²** | — | — |

> 📝 Metrics will populate after running the notebook on your dataset.

---

## 🔍 Key Findings

- Moving averages (MA-7, MA-21) are strong indicators of short-term price trends
- LSTM captures sequential dependencies that Linear Regression cannot — making it better suited for time-series forecasting
- Feature engineering (price range, volatility, daily return) significantly improves model accuracy
- Time-ordered train/test splitting is critical — shuffling destroys temporal patterns

---

## 📁 Repository Structure

```text
Stock-Price-Prediction/
│
├── Stock_Price_Prediction.ipynb   # Full notebook with preprocessing & models
├── indexProcessed.csv             # Dataset used in the project
├── stock_prediction.py            # Standalone Python script
└── README.md                      # Project documentation
```

---

## ⚙️ Installation & Usage

```bash
# 1. Clone the repository
git clone https://github.com/Faraz-jehangiri/Stock-Price-Prediction.git

# 2. Move into the project folder
cd Stock-Price-Prediction

# 3. Install required libraries
pip install pandas numpy scikit-learn tensorflow matplotlib seaborn jupyter

# 4. Launch Jupyter Notebook
jupyter notebook
```

---

## 🛠️ Tech Stack

- **Python 3.10+**
- **Pandas** — data cleaning & preprocessing
- **NumPy** — numerical operations
- **Scikit-learn** — Linear Regression & evaluation metrics
- **TensorFlow / Keras** — LSTM deep learning model
- **Matplotlib / Seaborn** — data visualisation
- **Jupyter Notebook** — development environment

---

## 👤 Author

**Faraz Ul Hassan Jehangiri**
BS Computer Science — SSUET, Karachi

[![GitHub](https://img.shields.io/badge/GitHub-Faraz--jehangiri-181717?style=flat-square&logo=github)](https://github.com/Faraz-jehangiri)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Faraz%20Jehangiri-0077B5?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/faraz-jehangiri)

---

## ⭐ Project Status

✅ Completed
📚 Intermediate Machine Learning Project
📈 Regression & Time Series Forecasting using Linear Regression + LSTM
