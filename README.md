# Trader Sentiment Analysis — Hyperliquid × Fear & Greed Index

Been curious for a while about whether market sentiment actually *changes* 
how traders behave — not just what they trade, but how well they do it. 
This project is my attempt to answer that properly, with real data.

---

## What I looked at

Two datasets:
- **Hyperliquid trade history** — 211,000+ trades across 32 accounts, 
  spanning May 2023 to May 2025
- **CNN Fear & Greed Index** — daily sentiment scores over the same period

Merged them by date and went digging.

---

## What I found

Honestly some of it surprised me:

- The **best single trading day** (+$616K) happened during a *Fear* market, 
  not Greed. The worst day (-$419K) was during Greed.
- Traders using **Extreme Greed** conditions had an 11x profit factor and 
  89% win rate — but traded far less frequently than Fear periods.
- **Extreme Fear** had the most daily trades (1,500+) but the worst 
  risk-adjusted returns. Panic trading is expensive.
- A Random Forest model trained on sentiment + trade features hit 
  **AUC = 0.95** predicting win/loss — with a 10% lift over baseline.

---

## What's inside

- Sentiment vs. performance breakdown across all 5 F&G categories
- Statistical significance tests (Kruskal-Wallis, Mann-Whitney, Chi-square)
- K-Means clustering → 4 trader archetypes (Precision Snipers, 
  High-Freq Grinders, Whale Scalpers, Sentiment Specialist)
- Random Forest classifier with 5-fold cross-validation
- Z-score anomaly detection on daily PnL and trade volume
- 6 data-backed strategy recommendations

---

## Stack

Python, Pandas, Scikit-learn, Scipy, Matplotlib, Seaborn

---

## View the report

Open `index.html` in your browser — all charts are local so it works offline.
