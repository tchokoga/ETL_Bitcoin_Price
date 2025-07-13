# 🟡 Bitcoin Price ETL Project

A clean and educational ETL (Extract → Transform → Load) pipeline using historical Bitcoin price data.

---

## 🧠 Project Objective

This project demonstrates how to:
- Load real financial time series data from a CSV file
- Clean and transform it using pandas
- Store the cleaned data into a local SQLite database
- Generate statistical insights and visualizations

---

## 📂 Dataset

- **Source**: [Kaggle – BTC/USD 1-Minute Historical Data](https://www.kaggle.com/datasets/mczielinski/bitcoin-historical-data)
- **File used**: `bitcoin_price.csv`
- **Content**: Minute-level BTC/USD prices from 2012 onward
- **Main fields**:
  - `Timestamp`: UNIX time
  - `Open`, `High`, `Low`, `Close`: OHLC prices
  - `Volume_(BTC)`, `Volume_(Currency)`
  - `Weighted_Price`

---

⚠️ **Note:** The full dataset and SQLite database are too large to include in this repository due to GitHub's 100MB file size limit.
>
> You can download them from Google Drive using the links below:
>
> - 📥 [Download `bitcoin_price.csv` (full version)](https://drive.google.com/file/d/147Udtsh55SJ8vD96_TBeND7b29QVDwQC/view?usp=sharing)
> - 🗄️ [Download `bitcoin.db` (SQLite database)](https://drive.google.com/file/d/1M8KF06e0ajFUJUQDSH7unDe7nNGH-kUr/view?usp=sharing)

---
## ⚙️ Stack Used

- Python
- pandas
- SQLite (via `sqlite3`)
- Plotly (interactive visualizations)
- Jupyter Notebook

---

## 📊 Pipeline Steps

### 1. Extract
- Load the original CSV file using `pandas.read_csv()`

### 2. Transform
- Clean column names
- Convert UNIX timestamp to datetime
- Drop missing values
- Sort data chronologically
- Compute daily average closing price

### 3. Load
- Save the cleaned dataset into a local SQLite database (`bitcoin.db`)
  
---

## 📈 Visualizations

Interactive line chart of Bitcoin's daily average closing price using **Plotly**

## 📄 Output Files

- `output/bitcoin_price_stats.csv` → Summary stats
- `bitcoin.db` → Cleaned data in SQLite