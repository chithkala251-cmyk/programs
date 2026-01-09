# Trader Behavior Insights Using Bitcoin Fear & Greed Index

## Project Overview
This project analyzes the relationship between **market sentiment** and **trader behavior**
using historical trading data from Hyperliquid and the Bitcoin Fear & Greed Index.

The objective is to understand how different sentiment regimes (Fear, Greed, Extreme Fear, Extreme Greed)
impact trader performance, risk-taking, and profitability, and to uncover behavioral patterns
that can inform smarter trading and risk management strategies.

---

## Datasets Used

### 1. Historical Trader Data (Hyperliquid)
Contains trader-level execution data including:
- Account ID
- Trade size
- Execution price
- Direction (Buy/Sell)
- Closed PnL
- Execution timestamp

> **Note:** Raw trading data is not included in this repository due to file size constraints.

### 2. Bitcoin Fear & Greed Index
Provides daily market sentiment classification:
- Extreme Fear
- Fear
- Neutral
- Greed
- Extreme Greed

**Data sources:**
- Historical Trader Data: Provided as part of the assignment
- Fear & Greed Index: https://alternative.me/crypto/fear-and-greed-index/

---

## Approach & Methodology

1. **Data Cleaning & Inspection**
   - Inspected all available timestamp columns
   - Identified the correct execution timestamp (`timestamp ist`)
   - Removed misleading or unused time fields

2. **Timestamp Alignment**
   - Converted intraday trade timestamps to calendar dates
   - Aligned trader data with daily market sentiment

3. **Data Integration**
   - Merged trader executions with sentiment labels using trade date

4. **Feature Engineering**
   - Created profitability indicator
   - Calculated aggregated trader performance metrics

5. **Trader Segmentation**
   - Segmented traders into:
     - Top 20% (high performers)
     - Average traders
     - Bottom 20% (low performers)

6. **Analysis**
   - Compared performance across sentiment regimes
   - Analyzed behavioral differences between trader groups

---

## Key Insights

- Top traders remain consistently profitable across all market sentiment conditions.
- Bottom traders incur significant losses during Greed phases, indicating poor risk management.
- Extreme Greed amplifies both gains and losses, especially for less skilled traders.
- Market sentiment strongly influences trader behavior and outcomes.

---

## Tools & Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook (Google Colab)

---

## How to Run the Notebook

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
3. Download the datasets from the provided links

4. Update dataset paths in the notebook if required

5. Run all cells sequentially
