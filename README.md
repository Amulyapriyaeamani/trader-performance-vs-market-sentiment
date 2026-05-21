# Trader Performance vs Market Sentiment Analysis

## Objective

This project analyzes how Bitcoin market sentiment influences trader behavior and trading performance on Hyperliquid.

The analysis explores the relationship between:
- trader profitability
- trading activity
- trade sizing behavior
- directional positioning
- market sentiment conditions

The primary goal is to identify behavioral patterns and actionable insights that could support smarter trading and risk-management strategies.

---

# Datasets Used

## 1. Bitcoin Fear & Greed Sentiment Dataset
Contains:
- date
- sentiment classification
- sentiment score

Sentiment categories include:
- Extreme Fear
- Fear
- Neutral
- Greed
- Extreme Greed

## 2. Hyperliquid Historical Trader Dataset
Contains:
- account-level trade activity
- execution price
- trade size
- side (buy/sell)
- fees
- timestamps
- closed pnl
- trading behavior metrics

## Dataset Access

Due to file size limitations, the raw datasets are not included directly in this repository.

Datasets can be downloaded from the original sources below:

### Bitcoin Fear & Greed Dataset
(https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing)

### Hyperliquid Historical Trader Dataset
(https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing)
  
---

# Methodology

The project workflow included:

## Data Preparation
- loaded both datasets using pandas
- inspected dataset structure, missing values, and duplicates
- converted timestamps into daily date format
- merged datasets on common trading dates

## Feature Engineering
Created key analytical metrics including:
- daily pnl per trader
- win rate
- average trade size
- trade frequency
- long ratio
- trader activity segments
- profitability segments

## Analysis Performed
The analysis focused on:
- sentiment-based trader performance
- trading behavior under different market conditions
- trader segmentation analysis
- pnl distribution analysis
- behavioral pattern identification

---

# Key Insights & Findings

This section summarizes the major behavioral and performance patterns identified during the analysis of trader activity and market sentiment conditions.

---

## Insight 1 — Traders Performed Better During Fear Conditions

Average daily profitability was highest during Fear and Extreme Fear market conditions, with Fear periods generating average daily PnL above 9,400 compared to approximately 4,600 during Greed periods.

Additionally, Fear conditions showed larger average trade sizes and wider profitability distributions, indicating increased market volatility and stronger trading opportunities during cautious market environments.

This suggests that traders may have benefited from heightened price movements and recovery opportunities during fearful market conditions.

---

## Insight 2 — High Activity Traders Demonstrated Stronger Performance

High-activity traders significantly outperformed low-activity traders across both profitability and consistency metrics.

Highly active traders achieved average daily profitability above 11,600 with a win rate of approximately 44%, compared to only 1,600 average daily profitability and 26% win rate for low-activity traders.

Interestingly, high-activity traders used smaller average trade sizes, suggesting that stronger execution and diversified participation may have contributed more to profitability than aggressive position sizing alone.

---

## Insight 3 — Strong Long Bias Was Linked to Lower Performance

Non-profitable traders exhibited a noticeably stronger long bias compared to profitable traders.

While long positioning increased during Fear and Extreme Fear conditions, traders with excessive long exposure achieved lower profitability and weaker win rates overall.

In contrast, short-biased traders generated higher average profitability and stronger trading consistency, suggesting that more balanced or defensive positioning strategies may have been more effective during the analyzed market conditions.

---

## Insight 4 — Trader Profitability Was Highly Concentrated

The profitability distribution analysis revealed substantial dispersion across all market sentiment conditions, with multiple extreme positive and negative outliers.

Most trader-day profitability values remained concentrated near lower pnl ranges, while a relatively small subset of traders generated disproportionately large profits or losses.

This indicates that trading performance was highly uneven and that a minority of traders contributed significantly to overall market profitability volatility.

---

## Insight 5 — Market Sentiment Influenced Trader Behavior

Trader behavior varied noticeably across sentiment regimes.

Fear conditions were associated with:
- larger average trade sizes
- stronger long positioning
- higher trading activity

Meanwhile, Greed conditions showed comparatively lower profitability and weaker trading consistency.

These behavioral shifts suggest that trader psychology and market sentiment significantly influenced trading decisions, positioning behavior, and overall market participation.

---

# Strategy Recommendations

Based on the behavioral and performance analysis, the following strategy recommendations are proposed to improve trader decision-making and risk management under different market sentiment conditions.

---

## Recommendation 1 — Reduce Aggressive Long Exposure During Fear Conditions

The analysis showed that traders significantly increased long positioning during Fear and Extreme Fear periods. However, traders with stronger long bias generally achieved weaker profitability and lower win rates compared to more balanced or short-biased traders.

Rule of Thumb:
During Fear market conditions, traders should avoid aggressively increasing directional long exposure and instead maintain tighter risk controls, smaller directional bias, and more balanced positioning strategies.

---

## Recommendation 2 — Favor Consistent Trading Activity Over Oversized Positions

High-activity traders achieved substantially higher profitability and stronger win rates despite using smaller average trade sizes than low-activity traders.

Rule of Thumb:
Traders may benefit more from consistent market participation and diversified execution rather than relying on infrequent oversized trades. During volatile market periods, maintaining moderate position sizing with higher execution discipline may improve trading consistency.

These recommendations are intended as behavioral risk-management guidelines derived from historical trading and sentiment patterns observed in the dataset.

---

# Tools & Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab

---

# Repository Structure

```text
trader-performance-vs-market-sentiment/
│
├── trader_sentiment_analysis.ipynb
├── README.md
├── requirements.txt
└── outputs/
```

---

# How to Run

## 1. Clone the Repository

```bash
git clone <repository-link>
```

## 2. Install Required Libraries

```bash
pip install -r requirements.txt
```

## 3. Open the Notebook

```bash
jupyter notebook trader_sentiment_analysis.ipynb
```

---

# Conclusion

This analysis demonstrated that market sentiment plays an important role in influencing trader behavior, trading activity, risk exposure, and profitability outcomes.

The findings suggest that trader psychology, positioning behavior, and activity levels can significantly affect performance during different market sentiment conditions, particularly during Fear and Extreme Fear environments.
