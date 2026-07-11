# 📈 S&P 500 Trading Post-Mortem: Risk Management & Technical Analytics

## 📊 Executive Summary
Este proyecto presenta un análisis técnico e histórico de la acción del precio del índice S&P 500 (SPCFD) durante el tercer trimestre, evaluando la interacción entre medias móviles exponenciales (EMA 20), osciladores de momentum (RSI) y la gestión de riesgo activa (Stop Loss y Trailing Stops). 

El objetivo principal es documentar el análisis "Post-Mortem" de una operación para refinar algoritmos de entrada y comprender el impacto de las divergencias bajistas sobre los soportes dinámicos.

---

## 🔍 Case Study 1: Breakout & Momentum (July 12)
* **Close Price:** $4,472.15
* **EMA (20):** $4,389.14
* **RSI (14):** 67.17

### Technical Assessment:
1. **Trend:** Strong bullish regime with the price trading significantly above the upward-sloping EMA 20.
2. **Momentum:** High velocity approaching overbought territory ($RSI \approx 70$). 
3. **Risk Strategy:** Buying the immediate breakout presented a high probability of buying the local top due to the price being extended 83 points from its mean. The optimal execution strategy was a delayed entry on a structure retest ($4,440 - $4,450).

---

## 📉 Case Study 2: Dynamic Support Failure & RSI Divergence (August 26)
* **Close Price:** $4,470.60
* **EMA (20):** $4,440.01
* **RSI (14):** 58.45

### The Technical Dilemma & Execution:
* **Hypothesis:** Entry via a Limit Order at the EMA 20 ($4,435) assuming a dynamic support rebound.
* **The Flaw:** The operational setup implemented an excessively tight Stop Loss (10 points / 0.22%), underestimating the asset's daily ATR (Average True Range), which fluctuates between 30 and 50 points.
* **Market Outcome:** The bearish RSI divergence correctly predicted institutional exhaustion. Sellers breached the EMA 20, triggering the defensive Stop Loss at $4,360 before establishing a structural bottom near $4,300.

---

## 🛠️ Key Takeaways & Risk Mitigation Rules
1. **Divergence vs. Moving Averages:** A clear bearish RSI divergence during a multi-month high invalidates dynamic exponential averages as blind entries. Execution must shift to a confirmation trigger (waiting for an engulfing bullish candle close).
2. **Mathematical Risk-to-Reward Ratio (R:R):** Premature profit-taking due to psychological bias damages the expectancy of the trading system. 
3. **Advanced Management:** Implementation of **Trailing Stops** and **Break-Even** adjustments after a 1:1 yield generation to secure risk-free exposure ($0 risk capital).
