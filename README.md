# -Stock-Market-Performance-Dashboard-Power-BI-

This repository contains an interactive **Power BI dashboard** analyzing **S&P 500 Stock Market Data (2014–2017)**. The report covers stock prices, trading volumes, volatility trends, and performance insights using dynamic visuals and DAX measures.

---

## 📁 Project Files
- **Stock Price 1 power bi dashboard.pbix** – Main Power BI file
- **S&P 500 Stock Prices 2014–2017.csv** – Source dataset
- **PowerBI_Stock_Report.docx** – Documentation report
- **Dashboard Screenshot** – Included for preview

---

## ✅ Key Features
- 📌 **KPI Cards**
  - Total Stocks
  - Total Volume
  - Average Close Price
  - Highest Close Price
  - Lowest Close Price
  - Daily Price Change %
  - Close Volatility %

- 📈 **Visualizations**
  - Close Volatility % Trend
  - Average Close Price Trend
  - Total Volume by Stock Symbol
  - Interactive Slicers (Date, Symbol)

- 🧮 **DAX Measures** for financial analytics
- 🎨 Clean layout and color formatting
- 🔍 Slicers for better interactivity

---

## 🧮 DAX Measures Used

### **Total Volume**
```
Total Volume = SUM('S&P 500 Stock Prices 2014-2017'[volume])
```

### **Average Close**
```
Average Close = AVERAGE('S&P 500 Stock Prices 2014-2017'[close])
```

### **Highest Close**
```
Highest Close = MAX('S&P 500 Stock Prices 2014-2017'[close])
```

### **Lowest Close**
```
Lowest Close = MIN('S&P 500 Stock Prices 2014-2017'[close])
```

### **Total Stocks**
```
Total Stocks = DISTINCTCOUNT('S&P 500 Stock Prices 2014-2017'[symbol])
```

### **Close Volatility %**
```
Close Volatility % =
VAR PrevClose =
    CALCULATE(
        AVERAGE('S&P 500 Stock Prices 2014-2017'[close]),
        DATEADD('S&P 500 Stock Prices 2014-2017'[date], -1, DAY)
    )
RETURN
DIVIDE(
    AVERAGE('S&P 500 Stock Prices 2014-2017'[close]) - PrevClose,
    PrevClose
)
```

---
✅ 📂 Dataset Source

This dataset is downloaded from Maven Analytics:
🔗 https://mavenanalytics.io/data-playground/s-p-500-stock-prices

---


## 🔧 How to Use
1. Download the `.pbix` file
2. Open in **Power BI Desktop**
3. Ensure dataset is correctly loaded
4. Refresh data
5. Use slicers for interaction

---

## 🎯 Dashboard Insights
- Identifies **most volatile stocks**
- Shows **price growth trends**
- Highlights high-volume stocks
- Provides 4-year market performance overview

---

## 👨‍💻 Developed By
**Satyam Birajdar**

---

## ⭐ Support
If you like this project, give it a **star**!
