# 🚀 Quantum Derivative Pricing

## 📌 Overview
This project implements **derivative pricing models** using both classical and quantum-inspired techniques. It focuses on comparing **Black-Scholes**, **Monte Carlo simulation**, and **Quantum Amplitude Estimation (QAE)** to evaluate computational efficiency and accuracy.

---

## 🎯 Problem Statement
Derivative pricing is computationally expensive, especially with Monte Carlo simulations. This project explores whether **quantum algorithms** can provide speedups in probabilistic estimation tasks used in finance.

---

## 🧠 Implementations

### 🔹 Classical Models
- **Black-Scholes Model**
  - Closed-form analytical solution
  - Baseline for accuracy

- **Monte Carlo Simulation**
  - Simulates multiple price paths
  - Used for complex/non-analytic derivatives

---

### 🔹 Quantum Approach
- **Quantum Amplitude Estimation (QAE) (Simulated)**
  - Quadratic speedup over classical Monte Carlo
  - Implemented using quantum simulation frameworks

---

## 📊 Results & Comparison

| Method              | Accuracy        | Speed            | Notes |
|--------------------|----------------|------------------|------|
| Black-Scholes      | High           | Very Fast        | Analytical solution |
| Monte Carlo        | Medium-High    | Slow             | Depends on iterations |
| Quantum (Simulated)| Medium-High    | Faster (theoretical) | Requires quantum hardware |

> ⚡ Quantum methods show **quadratic speedup potential** in estimation tasks.

---

## 📈 Visualizations Included
- Option payoff curves
- Monte Carlo convergence plots
- Error vs iterations comparison
- Quantum vs classical estimation trends

---

## 🛠 Tech Stack
- Python
- NumPy
- Matplotlib
- Qiskit (Quantum Simulation)

---

## 📂 Project Structure

```
Quantum-Derivative-Pricing/
│
├── classical/
│   ├── black_scholes.py
│   ├── monte_carlo.py
│
├── quantum/
│   ├── amplitude_estimation.py
│
├── notebooks/
│   └── quantum_pricing.ipynb
│
├── main.py
├── requirements.txt
└── README.md
```

---

## ▶️ How to Run

```bash
git clone https://github.com/rupajietishere/Quantum-Derivative-Pricing
cd Quantum-Derivative-Pricing
pip install -r requirements.txt
python main.py
```

---

## 🧪 Example Usage

```python
S = 100   # Asset price
K = 100   # Strike price
T = 1     # Time to maturity
r = 0.05  # Risk-free rate
sigma = 0.2  # Volatility
```

---

## 💡 Key Insights
- Monte Carlo accuracy improves with more simulations but increases computation time.
- Quantum Amplitude Estimation reduces required samples significantly.
- Real-world quantum advantage depends on hardware maturity.

---

## 🔮 Future Improvements
- American Options pricing
- Heston Model (stochastic volatility)
- Real quantum hardware execution
- GPU acceleration for Monte Carlo

---

## 🎯 Use Cases
- Quantitative Finance
- Risk Modeling
- Algorithmic Trading
- Financial Engineering Research

---

## 🙌 Conclusion
This project demonstrates how **quantum computing concepts can be applied to financial problems**, highlighting both current limitations and future potential.

---

## 📬 Contact
Feel free to connect or reach out for collaboration!
