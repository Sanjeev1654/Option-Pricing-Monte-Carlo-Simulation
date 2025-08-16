# Option Pricing Monte Carlo Simulator

## Project Overview
This project implements a Monte Carlo simulator for pricing European options. It uses stochastic modeling to simulate possible paths of the underlying asset's price and estimates the option price based on these simulated outcomes.

## Key Features
- Simulates multiple paths of asset prices using random sampling.
- Computes the expected payoff of options and discounts it to present value.
- Flexible parameters including spot price, strike price, volatility, risk-free rate, and time to maturity.
- Supports both call and put options.

## Mathematical Concepts Used
- Stochastic processes to model random behavior of asset prices.
- Monte Carlo simulation for numerical approximation of option prices.
- Risk-neutral valuation to compute expected discounted payoffs.
- Statistical averaging and variance reduction techniques to improve accuracy.

## Usage
1. Install required libraries (NumPy, Pandas, Matplotlib).
2. Set your parameters for the option (S0, K, T, r, sigma, num_simulations).
3. Run the simulation to get the estimated option price.

## Example
```python
# Example usage
from monte_carlo_simulator import OptionPricingSimulator

simulator = OptionPricingSimulator(S0=100, K=105, T=1, r=0.05, sigma=0.2, num_simulations=100000)
call_price = simulator.simulate_call()
print(f"Estimated Call Option Price: {call_price}")
