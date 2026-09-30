# Central-Bank-Exchange-Rates-1914-to-today

<img width="590" height="222" alt="image" src="https://github.com/user-attachments/assets/9c8f1e5e-c2e7-4a27-8e40-5a7cdced85c9" />
<img width="367" height="316" alt="image" src="https://github.com/user-attachments/assets/2412e80d-725b-458a-a32c-2650785626c7" />



🌍 FX Volatility Regimes: Decoding Emerging Market Crises 📉📈
“Not predicting tomorrow's exact exchange rate, but modeling the storm: tracking when a currency slips from calm seas into a crisis regime, how long it stays, and how contagion spreads globally.” ⚡

🗺️ Pipeline Architecture & Roadmap
This project acts as an end-to-end macro-financial time-series lab. Here is how the notebook processes over two decades of global financial data:
📥 1. Data Ingestion & Kagglehub Integration
Automated Sync: Pulls massive historical archives directly using kagglehub (allratestoday/central-bank-exchange-rates).
Dynamic Environment Setup: Automatically checks and installs econometric powerhouses like arch (for volatility modeling) and hmmlearn (for regime detection) on the fly.
🇪🇺 2. Choosing the Ultimate Backbone (ECB.csv)
The Audit: Scans 120 global institutions (central banks, tax authorities, and composites).
The Winner: Selects the European Central Bank (ECB) dataset as the clean backbone—delivering consistent daily reference rates since 1999 across 41 currencies under a unified quoting standard.
🧹 3. Data Hygiene & Anomaly Wrangling
Redenomination Splicing: Corrects massive structural shocks like Turkey dropping zeros off the Lira (TRY/TRL), preventing false "99.9% appreciation" spikes.
Peg Detection: Empirically filters out currency pegs (e.g., currencies with <2% annualized volatility against their anchor like EUR or USD) since policy-driven pegs add zero value to a free-market volatility study.
Gap Quarantine: Identifies and isolates major publication gaps (like Iceland's 9-year ISK blackout during the 2008 banking crisis) so missing data never corrupts log-return calculations.
📊 4. Econometric Transformation & Standardization
USD Base Conversion: Harmonizes all series into units of currency per $1 USD using the ECB's daily EUR/USD fix, exposing the classic "Dollar Factor" during global risk-off events.
Log-Returns Engine: Transforms non-stationary price paths into stationary continuous compounding returns:
r 
t
​	
 =ln( 
P 
t−1
​	
 
P 
t
​	
 
​	
 )
🤖 5. Advanced Modeling & Regime Detection
GARCH Volatility Modeling: Captures time-varying volatility clusters and financial shock persistence (tested heavily on volatile pairs like TRY).
Hidden Markov Models (HMM): Unsupervised machine learning models that automatically classify market states into "Calm Regimes" versus "Crisis Regimes".
Contagion Mapping: Measures cross-currency correlation matrices to see how financial panics ripple across emerging and developed markets.
💡 Quick Tech Stack Used
Python 🐍
Pandas & NumPy (Data wrangling)
Matplotlib & Seaborn (Macro visualization)
Statsmodels (Stationarity & ADF tests)
Arch & Hmmlearn (Econometrics & Regime shifting)
