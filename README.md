# Quantum Ripple Carry Adder (QRCA) in NISQ Environment

## Overview

This project presents the implementation and analysis of a **Quantum Ripple Carry Adder (QRCA)** in a **Noisy Intermediate-Scale Quantum (NISQ)** environment using Qiskit. The objective is to investigate the impact of realistic quantum noise on arithmetic circuit performance and evaluate the reliability of quantum addition under different noise models.

The QRCA circuit is simulated on both ideal and noisy quantum backends, and its performance is quantified using standard error metrics such as Error Rate (ER), Normalized Mean Error Distance (NMED), and Mean Relative Error Distance (MRED).

---

## Features

- Quantum Ripple Carry Adder (QRCA) implementation
- Simulation using Qiskit Aer
- NISQ-aware noisy quantum execution
- Support for multiple quantum noise models:
  - Bit Flip Noise
  - Phase Flip Noise
  - Depolarizing Noise

- Performance comparison between ideal and noisy environments
- Error analysis using standard approximate-computing metrics
- Visualization of experimental results

---

## Background

Quantum arithmetic circuits are fundamental building blocks for quantum algorithms. Among them, the Quantum Ripple Carry Adder (QRCA) provides a straightforward reversible implementation of binary addition by propagating carry bits sequentially through the circuit.

Although QRCA requires fewer resources compared to some advanced adder architectures, its performance can degrade significantly in NISQ devices due to gate errors, decoherence, and measurement noise. This project investigates these effects through simulation-based analysis.

---

## Technologies Used

- Python
- Qiskit
- Qiskit Aer
- NumPy
- Matplotlib
- IBM Quantum Platform

---

## Methodology

### Step 1: Circuit Construction

The QRCA circuit is designed using reversible quantum gates including:

- CNOT Gate
- Toffoli Gate (CCX)
- X Gate

### Step 2: Input Encoding

Classical binary numbers are encoded into quantum states.

### Step 3: Ideal Simulation

The circuit is executed on an ideal quantum simulator to obtain reference outputs.

### Step 4: Noise Injection

Different noise models are applied to emulate NISQ hardware behavior.

### Step 5: Performance Evaluation

Experimental outputs are compared with expected outputs using multiple error metrics.

---

## Noise Models

### Bit Flip Noise

Simulates unintended flips between quantum states:

|0⟩ ↔ |1⟩

---

### Phase Flip Noise

Introduces phase errors without changing measurement probabilities:

|1⟩ → −|1⟩

---

### Depolarizing Noise

Randomly applies Pauli operations:

- X
- Y
- Z

with a specified probability.

---

## Error Metrics

### Error Rate (ER)

Measures the probability of obtaining an incorrect output.

[
ER = \frac{Number\ of\ Incorrect\ Outputs}{Total\ Outputs}
]

---

### Normalized Mean Error Distance (NMED)

Measures the average deviation between noisy and correct outputs normalized to the maximum output range.

---

### Mean Relative Error Distance (MRED)

Measures relative computational error with respect to the correct output.

---

## Experimental Workflow

1. Generate QRCA circuit.
2. Encode input operands.
3. Execute on ideal simulator.
4. Apply selected noise model.
5. Execute noisy simulation.
6. Collect measurement outcomes.
7. Calculate ER, NMED, and MRED.
8. Compare performance across noise models.

---

## Results

The project evaluates the impact of different quantum noise models on QRCA performance.

| Noise Model  | Error Rate (ER) | NMED         | MRED         |
| ------------ | --------------- | ------------ | ------------ |
| Ideal        | 0.000           | 0.000        | 0.000        |
| Depolarizing | 36.93 %         | 0.067        | 0.201        |
| Bit Flip     | 81.52 %         | 0.167        | 0.502        |
| Phase Flip   | Experimental    | Experimental | Experimental |

Replace the table values with your obtained simulation results.

---

## Applications

- Quantum Arithmetic Circuits
- Quantum Computing Research
- NISQ Benchmarking
- Quantum Error Analysis
- Quantum Algorithm Development
- Approximate Quantum Computing

---

## Future Work

- Larger-bit QRCA implementations
- Execution on real IBM Quantum hardware
- Error mitigation techniques
- Hardware-aware transpilation
- Comparative study with:
  - Quantum Carry Lookahead Adder (QCLA)
  - Vedral-Barenco-Ekert Adder
  - Thapliyal Adder

---

## Installation

Clone the repository:

```bash
git clone https://github.com/MAnkan2006/QRCA-in-NISQ-Environment.git
cd QRCA-in-NISQ-Environment
```

Install required dependencies:

```bash
pip install qiskit qiskit-aer numpy matplotlib
```

---

## Usage

Run the simulation:

```bash
python qrca.py
```

The program will:

- Construct the QRCA circuit
- Execute ideal simulation
- Execute noisy simulations
- Compute error metrics
- Generate performance results

---

## Repository

GitHub Repository:

https://github.com/MAnkan2006/QRCA-in-NISQ-Environment

---

## Author

**Ankan Mandal**

B.Tech, Computer Science and Engineering
National Institute of Technology Durgapur

GitHub: https://github.com/MAnkan2006

---

## Citation

If you use this work in your research, please cite:

```text
Ankan Mandal.
"Quantum Ripple Carry Adder (QRCA) in NISQ Environment."
GitHub Repository, 2026.
```

---
