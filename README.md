# Trader Performance vs Market Sentiment Analysis

## Objective
This project analyzes how Bitcoin market sentiment influences trader behavior and trading performance on Hyperliquid.

The analysis explores:
- trader profitability
- trading activity
- position sizing
- directional bias
- behavioral differences across market sentiment conditions

---

## Datasets Used

1. Bitcoin Fear & Greed Index dataset
2. Hyperliquid historical trader dataset

---

## Methodology

The project workflow included:
- data cleaning and preprocessing
- timestamp alignment at daily level
- feature engineering
- trader segmentation
- sentiment-based performance analysis
- behavioral analysis and strategy recommendations

Key metrics analyzed:
- daily pnl
- win rate
- average trade size
- trade frequency
- long ratio

---

## Key Insights

- Traders achieved higher average profitability during Fear conditions.
- High-activity traders significantly outperformed low-activity traders.
- Excessive long bias was associated with weaker overall performance.
- Trading outcomes were highly uneven with significant pnl dispersion.

---

## Strategy Recommendations

1. Reduce excessive directional bias during fearful market conditions.
2. Favor disciplined and consistent participation over oversized trades.

---

## Tools & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

## How to Run

1. Clone the repository
2. Install requirements:
pip install -r requirements.txt

3. Open the notebook:
jupyter notebook trader_sentiment_analysis.ipynb
