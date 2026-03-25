# 📊 Quantum Derivative Pricing

A hybrid classical + quantum computing project for pricing financial derivatives using traditional models and quantum algorithms such as Amplitude Estimation.

---

## 🚀 Project Overview

This project demonstrates how quantum computing can enhance financial modeling by comparing:

**Classical pricing methods:**
- Black-Scholes Model
- Monte Carlo Simulation

**Quantum approach:**
- Amplitude Estimation for faster convergence

The goal is to explore quantum advantage in derivative pricing, particularly for probabilistic simulations.

---

## 📂 Project Structure
```
Quantum-Derivative-Pricing/
│
├── classical/
│   ├── black_scholes.py        # Analytical option pricing model
│   ├── monte_carlo.py          # Simulation-based pricing
│
├── quantum/
│   ├── amplitude_estimation.py # Quantum pricing approach
│
├── notebooks/
│   └── quantum_pricing.ipynb   # Experimentation & visualization
│
├── main.py                     # Entry point to run models
├── requirements.txt            # Dependencies
└── README.md                   # Project documentation
```

---

## 🧠 Concepts Used

### Classical Finance
- Black-Scholes Formula
- Risk-neutral valuation
- Monte Carlo simulations

### Quantum Computing
- Quantum circuits
- Probability amplitude encoding
- Amplitude Estimation (AE)

---

## ⚙️ Installation

**Clone the repository:**
```bash
git clone https://github.com/your-username/Quantum-Derivative-Pricing.git
cd Quantum-Derivative-Pricing
```

**Create virtual environment (recommended):**
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

**Install dependencies:**
```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

**Run full pipeline:**
```bash
python main.py
```

**Run Jupyter Notebook:**
```bash
jupyter notebook notebooks/quantum_pricing.ipynb
```

---

## 📈 Methods Comparison

| Method | Type | Speed | Accuracy |
|---|---|---|---|
| Black-Scholes | Analytical | Fast | High (assumptions apply) |
| Monte Carlo | Classical | Slow | Improves with simulations |
| Quantum AE | Quantum | Faster (theoretical) | High |

---

## 🔬 Key Insights

- Classical Monte Carlo requires **O(N)** simulations
- Quantum Amplitude Estimation reduces complexity to **O(√N)**
- Quantum advantage becomes significant for large-scale simulations

---

## 🛠️ Tech Stack

- Python
- NumPy
- SciPy
- Qiskit (for quantum simulations)
- Matplotlib / Jupyter

---

## 📊 Example Output

- Option price comparison across methods
- Convergence plots (Monte Carlo vs Quantum)
- Probability distribution visualization

---

## ⚠️ Limitations

- Quantum algorithms are simulated (no real quantum hardware)
- Noise and hardware constraints not fully modeled
- Requires understanding of both finance and quantum computing

---

## 🔮 Future Improvements

- Integration with real quantum hardware (IBM Q)
- Support for exotic options
- Variance reduction techniques
- Hybrid quantum-classical optimization

---

## 🤝 Contributing

Contributions are welcome!
Feel free to fork the repo and submit a pull request.

---

## 📜 License

This project is licensed under the MIT License.

---

## 🤝 Connect with Me
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Rupajiet%20Bhattacharjee-blue?logo=linkedin)](https://www.linkedin.com/in/rupajiet-bhattacharjee-60932769)  
[![GitHub](https://img.shields.io/badge/GitHub-rupajietishere-black?logo=github)](https://github.com/rupajietishere)