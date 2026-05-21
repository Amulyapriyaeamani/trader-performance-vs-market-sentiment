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

## Insight 1 — Fear Conditions Generated Higher Profitability

Trader profitability was strongest during Fear and Extreme Fear conditions. Fear periods produced the highest average daily PnL (~9,426), compared to ~4,659 during Greed periods.

Fear regimes also showed:
- higher trade frequency
- larger trade sizes
- wider PnL dispersion

This suggests that volatile market conditions created stronger trading opportunities.

**Evidence Pointer:**  
- Sentiment-wise PnL table  
- `PnL Distribution by Market Sentiment` boxplot

---

## Insight 2 — High-Activity Traders Outperformed Low-Activity Traders

High-activity traders significantly outperformed low-activity traders, achieving:
- ~7x higher average daily PnL
- higher win rates (~44% vs ~27%)
- smaller average trade sizes

This suggests that consistent execution was more effective than oversized trades.

**Evidence Pointer:**  
- Trader activity segmentation table  
- Profitability group comparison

---

## Insight 3 — Strong Long Bias Was Linked to Lower Performance

Non-profitable traders showed a stronger long bias (~59%) compared to profitable traders (~48%).

Long positioning increased during Fear conditions, but excessive long exposure was associated with:
- lower profitability
- weaker win rates
- higher downside volatility

**Evidence Pointer:**  
- Long ratio comparison tables  
- `PnL Distribution by Position Bias` boxplot

---

## Insight 4 — Profitability Was Concentrated Among a Small Group of Traders

Trader performance showed extreme dispersion across the dataset.

While most trader-day PnL values remained relatively low, a small subset of traders generated disproportionately large profits and losses:
- max daily PnL > 533k
- min daily PnL < -175k

This indicates highly uneven profitability distribution across traders.

**Evidence Pointer:**  
- `daily_metrics.describe()` summary  
- PnL distribution boxplots

---

## Insight 5 — Market Sentiment Influenced Trading Behavior

Trader behavior varied noticeably across sentiment regimes.

Fear conditions showed:
- higher trade frequency
- larger trade sizes
- stronger long positioning
- higher average profitability

This suggests that market sentiment strongly influenced participation and risk-taking behavior.

**Evidence Pointer:**  
- Sentiment-wise trade count table  
- Long ratio and trade size comparison tables

---

# Strategy Recommendations

## Recommendation 1 — Reduce Aggressive Long Exposure During Fear Conditions

Fear periods showed the strongest long bias (~0.59–0.62), while traders with excessive long exposure generally achieved weaker profitability and lower win rates.

### Rule of Thumb:
During Fear-driven markets:
- avoid concentrated long exposure
- maintain balanced positioning
- apply tighter risk controls

**Supporting Evidence:**  
- Non-profitable trader long ratio: ~0.592  
- Profitable trader long ratio: ~0.483

---

## Recommendation 2 — Prioritize Consistent Execution Over Oversized Trades

High-activity traders achieved significantly stronger profitability despite using smaller average trade sizes.

### Rule of Thumb:
During volatile markets:
- favor consistent trade execution
- maintain moderate position sizing
- avoid infrequent oversized positions

This may improve trading consistency while reducing concentration risk.

**Supporting Evidence:**  
- High-activity trader PnL: ~11,618  
- Low-activity trader PnL: ~1,662

---

**Limitation**: Results are based on historical correlations and do not imply causation. Market volatility may be a confounding factor in sentiment-linked performance.

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
pip install pandas numpy matplotlib seaborn jupyter
```

## 3. Download the Datasets

Download both datasets from the links provided in the README and place them in the project directory.

## 4. Open the Notebook

```bash
jupyter notebook trader_sentiment_analysis.ipynb
```

## 5. Run All Cells

Execute the notebook cells sequentially to reproduce the analysis, charts, and findings.

---

# Conclusion

This analysis demonstrated that market sentiment plays an important role in influencing trader behavior, trading activity, risk exposure, and profitability outcomes.

The findings suggest that trader psychology, positioning behavior, and activity levels can significantly affect performance during different market sentiment conditions, particularly during Fear and Extreme Fear environments.
