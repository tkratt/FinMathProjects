##[Black-Scholes Option Pricing Model](Black-Scholes.ipynb)

This project implements and evaluates the Black-Scholes option pricing model by comparing theoretical prices to real-world market data for MSFT call options. The notebook explores multiple methods of volatility estimation and measures model accuracy using Mean Squared Error (MSE).

---

## Project Overview

The workflow of the project includes:

1. **Theoretical Modeling**
   - Implements the Black-Scholes formula for European call and put options.
   - Visualizes how option prices change with respect to stock price and volatility.

2. **Real Market Data**
   - Fetches MSFT options data using the [Polygon.io API](https://polygon.io/).
   - Selects $510 strike call contracts for analysis.

3. **Volatility Estimation Techniques**
   - **Historical Volatility**
   - **GARCH(1,1) Model** using the `arch` package
   - **Implied Volatility** via numerical root-finding

4. **Model Comparison & Evaluation**
   - Compares real vs. theoretical prices
   - Records residuals and calculates Mean Squared Error (MSE)
   - Best MSE: **0.64**, using a hybrid of GARCH and historical volatility

---

## Key Insight

Although the Black-Scholes model is designed for **European options**, we applied it to **American options** as a challenge. Despite its limitations (e.g., American options can be exercised early), the model performed reasonably well.

---

## Future Work

- Implement a **binomial option pricing model** for more accurate American option pricing.
- Explore more robust volatility forecasting models (e.g., EGARCH, Heston).

---

## Files

| File | Description |
|------|-------------|
| `Black-Scholes.ipynb` | Main Jupyter Notebook containing code, analysis, and results |

