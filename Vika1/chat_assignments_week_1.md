📅 Week 1: Stock Data Foundations & Time Series Math
🎯 Objectives
✅ Fetch real stock data (2 tickers, daily prices)
✅ Explore and visualize time series structure
✅ Compute returns, moving averages, and volatility
✅ Document math concepts in notebook & README

🧠 Math to Learn
{Sjá Math_vika_1.png}


🛠 Mini‑Assignment (Code in Python)
1️⃣ Fetch Data

Use yfinance (easy option):

python

import yfinance as yf
data = yf.download(['AAPL','MSFT'], start='2023-01-01', end='2024-01-01')
2️⃣ Explore & Plot

Plot closing prices over time for both tickers.

3️⃣ Compute Returns

Calculate daily simple returns and log returns.

Plot histogram of returns.

4️⃣ Moving Average

Compute a 20‑day moving average for each stock.

Plot price with the moving average overlaid.

5️⃣ Rolling Volatility

Compute a 20‑day rolling standard deviation of returns.

Plot rolling volatility.

6️⃣ Document

Add markdown in notebook explaining each metric and what the plots show.

Update your README.md with:

Objectives of Week 1

Formulas you used

Key observations (e.g., volatility spikes, moving average trends)

✅ Commit to GitHub

week_1_stock_data.ipynb

Updated README.md

Optional: notes/week1_video_notes.md

🎥 Video Lectures
Watch these and take notes (quiz coming in 2 weeks):

📈 Time Series Analysis for Stock Prices (freeCodeCamp)
https://www.youtube.com/watch?v=5rM1fXzpH4c

📊 Stock Returns and Volatility Explained (Quantopian)
https://www.youtube.com/watch?v=2dD5nM-3shM


✏️ Extra Practice (from the worksheet I gave you)
If you’d like more hands-on:

Use the 15‑day sample dataset I created earlier. (week_1_learning.md og Stock_Math_Practice_Dataset.csv)

Compute returns, MA, and volatility manually to check understanding.

✅ When you finish:
Push to GitHub, share your notebook link or screenshots here, and I’ll review and give you feedback!

🔥 You’re all set — dive in and let me know when you’re ready for a check‑in or help on any step! 📈💻