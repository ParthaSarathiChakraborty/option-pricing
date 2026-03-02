# option-pricing


🔷 Multi-Model Option Pricing & Market Benchmarking

👤 Author: Partha Sarathi Chakraborty | Quantitative Analyst / Researcher



## 📌 Project Overview

This project implements a multi-model derivatives pricing framework to evaluate how well classical option pricing models replicate real market prices.

# Using SPY option chain data, I built and benchmarked three pricing engines:

  •	Black–Scholes (Analytical Model)
	
  •	CRR Binomial Tree (Lattice Model)
	
  •	Monte Carlo Simulation (Stochastic Model)

# The models are compared against market mid-prices to analyze:

  •	pricing accuracy
	
  •	model assumptions
	
  •	volatility structure
	
  •	and real-world deviations (volatility skew & microstructure effects)



## 🎯 Research Objective

The core objective of this project is to answer:

How accurately do classical option pricing models explain real market prices, and where do their assumptions break down?

This mirrors a typical quant research / derivatives desk task:
	•	building pricing models
	•	validating against market data
	•	identifying model risk

⸻

## 📊 Data & Methodology

📈 Data Source
	•	SPY option chain (via Yahoo Finance API)

🧮 Data Preparation
	•	Constructed mid prices from bid/ask
	•	Filtered illiquid options
	•	Computed:
	•	time to maturity (T)
	•	moneyness (K / S)
	•	implied volatility (IV)

⚙️ Assumptions
	•	European options
	•	Constant risk-free rate
	•	No dividends (simplified)
	•	Lognormal price dynamics (GBM)



## 🧠 Model Framework

1️⃣ Black–Scholes Model

Closed-form analytical solution under:
	•	constant volatility
	•	lognormal returns
	•	no arbitrage

**Used as the baseline pricing model**

⸻

2️⃣ CRR Binomial Tree

Discrete-time lattice approximation:
	•	converges to Black-Scholes as steps → ∞
	•	allows intuitive understanding of price evolution

Used for numerical validation and comparison

⸻

3️⃣ Monte Carlo Simulation

Simulated terminal prices under risk-neutral GBM:

S_T = S_0 \cdot e^{(r - \frac{1}{2}\sigma^2)T + \sigma \sqrt{T} Z}

Features:
	•	antithetic variance reduction
	•	convergence diagnostics
	•	statistical error estimation

Used for stochastic pricing and convergence analysis

⸻

## 📈 Key Results

🔹 Model Convergence

	•	Black-Scholes ≈ Binomial ≈ Monte Carlo
	•	All models converge under same volatility assumption



## 🔹 Market Benchmarking (MAE)

Model	Mean Absolute  |  Error

Black–Scholes	       | ~0.05

Monte Carlo	         | ~0.05

Binomial Tree	       | ~0.003


⸻

## 🔹 Error Behavior
	•	Best fit near ATM options
	•	Larger deviations in deep ITM / OTM regions
	•	Reflects volatility skew & liquidity effects

⸻

## 🔹 Monte Carlo Convergence
	•	Error decreases as O(1/√N)
	•	Confirms unbiased estimator under risk-neutral measure

⸻

## 📊 Volatility Analysis

The project reveals:
	•	Market exhibits volatility smile / skew
	•	Constant volatility assumption is violated
	•	OTM puts have higher IV → reflects crash risk hedging demand

⸻

🔍 Key Insights
	•	Analytical, lattice, and simulation models agree under identical assumptions
	•	Real market prices deviate due to:
	•	volatility skew
	•	liquidity & microstructure noise
	•	discrete strike grid
	•	Model error = model assumptions + market effects

⸻

## ⚠️ Limitations
	•	Constant volatility assumption
	•	European option framework
	•	Static interest rate
	•	No dividend adjustment
	•	No transaction costs or slippage

⸻

## 🚀 Extensions & Future Work

This framework can be extended with:

  •	Heston Stochastic Volatility Model
	
  •	Local Volatility Surface Calibration
	
  •	SABR Model
	
  •	American Option Pricing (LSMC)
	
  •	GPU-accelerated Monte Carlo

⸻

## 💼 Real-World Applications

This type of system can be used in:

  •	Quant trading desks

  •	Derivatives pricing teams
	
  •	Risk management
	
  •	Volatility trading strategies
	
  •	Model validation frameworks

⸻

```bash
option-pro/
│
├── data/                 # option chain data
├── notebooks/            # main research notebook
├── models/               # BS, Binomial, MC functions
├── visuals/              # IV smile & error plots
├── reports/              # PDF report
└── README.md
```

⸻

## 📎 Outputs Included

  •	✔ IV Smile Plot
	
  •	✔ Pricing Error vs Strike
	
  •	✔ Model Comparison Metrics
	
  •	✔ Monte Carlo Convergence Graph
	
  •	✔ Full Technical Report (PDF)

⸻

## 🧠 Topics used:

  •	Quantitative modeling
	
  •	Derivatives pricing
	
  •	Time-series data analysis
	
  •	Numerical methods (lattice, simulation)
	
  •	Volatility modeling
	
  •	Model validation against market data

⸻

I designed and implemented a full multi-model derivatives pricing system and benchmarked it against real SPY option prices to analyze model accuracy and volatility structure.

⸻

🔗 Connect
	•	GitHub: your link
	•	LinkedIn: your link
	•	Email: your email

⸻

⭐ If you found this useful

Feel free to ⭐ the repository or reach out for discussion.
