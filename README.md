# Crypto Data Pipeline for GMO Coin

This repository contains Jupyter notebooks for fetching cryptocurrency trade data from the GMO Coin public API, converting it into OHLC (Open, High, Low, Close) data, and subsequently calculating the ATR (Average True Range).

---

## 🚀 Features
- Fetch historical trade data from GMO Coin's API.
- Convert raw trade data into OHLC format.
- Calculate and add the ATR (Average True Range) to the OHLC data for volatility analysis.

---

## 📂 Repository Structure
```
crypto-data-pipeline/
├── README.md
├── requirements.txt        # Dependencies
├── data/                   # Directory for raw and processed data
├── notebooks/              # Jupyter notebooks for each processing step
│   ├── get_ohlcv_data.ipynb
│   └── culculate_atr.ipynb
└── src/
    └── data_fetcher/       # Python scripts for fetching data
```

---

## ⚙️ Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/crypto-data-pipeline.git
   cd crypto-data-pipeline
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## 🛠 Usage

The data processing is divided into two main steps, each handled by a separate Jupyter Notebook.

### 1. Fetch Data and Create OHLC
- **Notebook:** `notebooks/get_ohlcv_data.ipynb`
- **Purpose:** This notebook connects to the GMO Coin API to download historical trade data for a specified cryptocurrency and then processes this data to create an OHLC dataset.

### 2. Calculate ATR
- **Notebook:** `notebooks/culculate_atr.ipynb`
- **Purpose:** This notebook takes the generated OHLC data as input and calculates the Average True Range (ATR), adding it as a new column to the dataset.

---

## 📜 License

This project is licensed under the MIT License.