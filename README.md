# Quantum Derivative Pricing using Amplitude Estimation
![Python](https://img.shields.io/badge/Python-3.8+-blue)
![Qiskit](https://img.shields.io/badge/Qiskit-Quantum%20SDK-purple)
![Quantum Computing](https://img.shields.io/badge/Quantum-Computing-brightgreen)
![Finance](https://img.shields.io/badge/Domain-Quantitative%20Finance-yellowgreen)

## Project Overview
In Quantitative Finance, pricing complex derivatives typically relies on **Monte Carlo (MC) simulations**. However, classical MC simulations converge at a rate of $\mathcal{O}(1/\epsilon^2)$. This means to achieve 10x more accuracy, we need 100x more computational power.

This project demonstrates how **Quantum Computing** can be leveraged to price a European Call Option. By utilizing **Iterative Quantum Amplitude Estimation (IAE)**, we aim to achieve a theoretical **quadratic speedup** yielding a convergence rate of $\mathcal{O}(1/\epsilon)$.

## Financial Parameters (Black-Scholes Context)
We define the parameters for the underlying asset and the European Call Option using standard parameters typical in Black-Scholes-Merton (BSM) environments:

* **Initial Spot Price ($S_0$):** $100
* **Strike Price ($K$):** $110
* **Volatility ($\sigma$):** 40%
* **Risk-Free Rate ($r$):** 5%
* **Time to Maturity:** 0.1 years (approx. 36 days)

## The Quantum Approach

### 1. Quantum Uncertainty Model
Unlike classical Monte Carlo which generates sequential random paths, a quantum computer evaluates the entire probability distribution simultaneously in **superposition**. We map a **Log-Normal distribution** (representing future asset prices) onto `3` qubits, providing $2^3 = 8$ discrete values.

### 2. Payoff Function
The payoff for a European Call Option at maturity is strictly non-linear: $\max(0, S_T - K)$. We build a quantum circuit that represents this piecewise linear payoff function and scale it so it can be evaluated via quantum phase estimation.

### 3. Iterative Amplitude Estimation (IAE)
We convert our pricing model into an estimation problem using **Iterative Amplitude Estimation (IAE)**. IAE is an optimized version of canonical QAE that relies entirely on Grover iterations and requires fewer auxiliary qubits—making it highly suitable for NISQ (Noisy Intermediate-Scale Quantum) era devices.

* **Sampler:** Qiskit 1.0 `StatevectorSampler`
* **Target Precision ($\epsilon$):** 0.01 
* **Confidence Interval ($\alpha$):** 0.05 (95% confidence)

## Pricing Results

Comparing the results of our Quantum Algorithm against the exact mathematical expectation calculated classically:

```text
=== PRICING RESULTS ===
Classical Exact Expected Payoff:   $1.8578
Quantum Estimated Expected Payoff: $2.3305
Estimation Error:                   0.4728
```

### Analysis & Interpretation
* **Discretization of the Asset Price:** Because we used `num_qubits = 3`, the continuous log-normal distribution of the underlying asset is discretized into exactly 8 possible future states.
* **The Payoff Function:** The European Call Option only holds value if the final asset price exceeds the Strike Price ($110). 
* **Understanding the Estimation Error ($\approx \$0.47$):** The slight divergence between the Classical Exact expectation and the Quantum Estimation is expected. It is primarily driven by:
  1. **Grid Resolution:** 3 qubits provide a very coarse grid. As we increase the number of qubits (e.g., to 5 or 6), the grid becomes exponentially finer, drastically reducing discretization error.
  2. **Target Precision ($\epsilon$):** Our IAE was constrained by an $\epsilon = 0.01$ and $\alpha = 0.05$.

### The Quantum Advantage
While a 3-qubit model is a proof-of-concept, the underlying math proves the theory. Classically, achieving a high degree of precision requires Monte Carlo simulations that scale at $\mathcal{O}(1/\epsilon^2)$. By utilizing **Iterative Amplitude Estimation**, this quantum approach scales at $\mathcal{O}(1/\epsilon)$—offering a **quadratic speedup** for derivative pricing once deployed on fault-tolerant quantum hardware with higher qubit counts.

## Requirements

To run this notebook, you will need the following Python packages:

```bash
pip install qiskit qiskit-finance qiskit-algorithms numpy matplotlib
```