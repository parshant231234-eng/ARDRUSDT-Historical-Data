# ARDRUSDT 1-Minute Historical Kline Dataset

An institutional-grade, open-source archive of cleaned, standardized, and validated **1-minute intraday historical kline data** for **ARDRUSDT** (Binance Spot).

---

## 📊 Dataset Specifications
- **Symbol:** `ARDRUSDT`
- **Market:** Binance Spot
- **Timeframe:** 1 Minute (`1m`)
- **Total Months:** `75` months
- **Total Candles:** `3,233,746` 1-minute candles
- **Historical Range:** `2020-05-15 08:00:00` to `2026-07-10 02:59:00` (UTC)
- **Schema:** `timestamp, datetime_utc, open, high, low, close, volume, quote_volume, trade_count, taker_buy_volume, taker_buy_quote_volume`

---

## 🏛️ Directory Hierarchy
```text
ARDRUSDT-Historical-Data/
├── README.md
└── 1m/
    └── <YYYY>/
        └── <MM>/
            └── ARDRUSDT_1m_<YYYY-MM>.csv
```

---

## ⚡ 1-Line Pandas Stream Loader
Load any month directly from GitHub's raw CDN without cloning the repository:

```python
import pandas as pd

url = "https://raw.githubusercontent.com/parshant231234-eng/ARDRUSDT-Historical-Data/main/1m/2026/11/ARDRUSDT_1m_2026-11.csv"
df = pd.read_csv(url)
print(df.head())
```
