
```markdown
# Crypto Data Pipeline

A Python-based pipeline for fetching, preprocessing, and transforming cryptocurrency price data into structured OHLCV format.
This repository demonstrates data engineering skills (API integration, preprocessing, and reproducible workflows) as part of a broader crypto analysis portfolio.

---

## 🚀 Features
- Fetch cryptocurrency price time series data via API
- Preprocess raw data (cleaning, timezone alignment, missing value handling)
- Convert data into OHLCV (Open, High, Low, Close, Volume) format
- Calculate **ATR (Average True Range)** for volatility analysis
- Modular structure for easy extension (e.g., new data sources or formats)

---

## 📂 Repository Structure
```

crypto-data-pipeline/
├── README.md
├── requirements.txt        # Dependencies
├── data/                   # Sample raw and processed data
├── notebooks/              # Example usage in Jupyter notebooks
└── src/
├── data\_fetch/         # Scripts to fetch crypto data from APIs
├── preprocessing/      # Scripts to clean & transform data
├── indicators/         # Scripts for OHLC/ATR calculations
└── utils/              # Helper functions (logging, config, etc.)

````

---

## ⚙️ Installation
```bash
# Clone the repository
git clone https://github.com/your-username/crypto-data-pipeline.git
cd crypto-data-pipeline

# Install dependencies
pip install -r requirements.txt
````

---

## 🛠 Usage

### 1. Fetch Data

```bash
python src/data_fetch/fetch_prices.py --symbol BTC --interval 1h --output data/raw_btc.json
```

### 2. Preprocess Data

```bash
python src/preprocessing/preprocess.py --input data/raw_btc.json --output data/btc_ohlcv.csv
```

### 3. Calculate OHLC + ATR

```bash
python src/indicators/calc_ohlc_atr.py --input data/btc_ohlcv.csv --output data/btc_ohlc_atr.csv --atr_period 14
```

### 4. Explore Data in Notebook

Open [notebooks/ohlcv\_analysis.ipynb](notebooks/ohlcv_analysis.ipynb) to see examples of:

* OHLC data visualization
* ATR-based volatility analysis
* Simple trading signal experiments

---

## 📊 Example Output

| timestamp           | open     | high     | low      | close    | volume | atr\_14 |
| ------------------- | -------- | -------- | -------- | -------- | ------ | ------- |
| 2025-01-01 00:00:00 | 42000.50 | 42210.75 | 41900.10 | 42150.00 | 120.35 | 350.42  |
| 2025-01-01 01:00:00 | 42150.00 | 42300.00 | 42010.25 | 42290.50 | 98.44  | 365.18  |

---

## 🔮 Future Work

* Add support for multiple exchanges (Binance, Coinbase, etc.)
* Automate scheduling with Airflow/Prefect
* Containerize with Docker for reproducible deployment
* Store processed data in a database (PostgreSQL, DuckDB, etc.)
* Extend indicator set (RSI, MACD, Bollinger Bands, etc.)

---

## 📜 License

This project is licensed under the MIT License.
Feel free to use, modify, and share.

---

```

---

