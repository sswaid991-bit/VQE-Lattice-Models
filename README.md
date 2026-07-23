# Ground-State Computation of Quantum Lattice Models via VQE
## A Systematic Cross-Model Benchmark

[![Python](https://img.shields.io/badge/Python-3.11-blue.svg)]()
[![Qiskit](https://img.shields.io/badge/Qiskit-0.46.2-purple.svg)]()
[![License](https://img.shields.io/badge/License-MIT-green.svg)]()
[![Platform](https://img.shields.io/badge/Platform-Windows%2011-lightgrey.svg)]()

This repository contains the complete implementation accompanying the research paper:

> **Ground-State Computation of Quantum Lattice Models via VQE: A Systematic Cross-Model Benchmark**

The project presents a rigorous benchmark of the **Variational Quantum Eigensolver (VQE)** using a **Hamiltonian Variational Ansatz (HVA)** across three canonical one-dimensional quantum lattice Hamiltonians:

- Transverse Field Ising Model (TFIM)
- Heisenberg Spin Chain
- Fermi-Hubbard Model

All simulations were performed using **Qiskit's exact statevector simulator** and validated against **Exact Diagonalization (ED)**.

---

# Authors

**Saleh Swaid**

Department of Physics

School of Science

University of Management and Technology (UMT)

Lahore 54770, Pakistan

Email:
sswaid991@gmail.com

**M. Imran Jamil**

Department of Physics

School of Science

University of Management and Technology (UMT)

Lahore, Pakistan

**Arslan Hashim**

Department of Physics

School of Science

University of Management and Technology (UMT)

Lahore, Pakistan

---

# Abstract

Variational Quantum Eigensolver (VQE) is one of the most promising quantum algorithms for computing molecular and condensed-matter ground-state energies on Noisy Intermediate-Scale Quantum (NISQ) devices.

This work presents a systematic benchmark of Hamiltonian Variational Ansatz (HVA)-based VQE across three representative quantum lattice Hamiltonians of increasing physical complexity:

- Transverse Field Ising Model (TFIM)
- Antiferromagnetic Heisenberg Model
- Spinful Fermi-Hubbard Model

Exact statevector simulations are used throughout and validated against Exact Diagonalization references for systems of up to **12 qubits**.

The benchmark demonstrates:

- Machine-precision accuracy for TFIM.
- Chemical-accuracy-level performance for the Heisenberg model.
- High-accuracy solutions for the Hubbard model despite its substantially larger optimization landscape.

The study further shows that **the number of variational parameters—not circuit depth—is the dominant factor governing VQE computational cost** for strongly correlated fermionic systems.

---

# Repository Structure

```
VQE-Lattice-Models
│
├── notebooks
│   ├── TFIM.ipynb
│   ├── Heisenberg.ipynb
│   └── Hubbard.ipynb
│
├── figures
│
├── paper
│
├── README.md
├── requirements.txt
├── LICENSE
└── CITATION.cff
```

---

# Software Environment

| Component | Version |
|------------|---------|
| Python | 3.11.14 |
| Qiskit | 0.46.2 |
| Qiskit Nature | 0.7.0 |
| Qiskit Aer | 0.13.1 |
| Qiskit Algorithms | 0.3.1 |
| NumPy | 1.23.5 |
| SciPy | 1.15.3 |
| Matplotlib | 3.10.7 |

Operating System

- Windows 11 Pro

---

# Models Included

## 1. Transverse Field Ising Model (TFIM)

- 12 qubits
- Critical point (J = h = 1.0)
- Hamiltonian Variational Ansatz
- Exact benchmark

---

## 2. Heisenberg Spin Chain

- 12 qubits
- Isotropic antiferromagnetic interaction
- Hamiltonian Variational Ansatz
- Exact benchmark

---

## 3. Spinful Fermi-Hubbard Model

- 6 lattice sites
- 12 qubits
- Half-filling
- Jordan-Wigner mapping
- Warm-start initialization
- Hamiltonian Variational Ansatz

---

# Benchmark Results

| Metric | TFIM | Heisenberg | Hubbard |
|--------|------|------------|----------|
| Qubits | 12 | 12 | 12 |
| Parameters | 12 | 24 | 270 |
| Circuit Depth | 79 | 222 | 76 |
| Optimizer Iterations | 689 | 2954 | 400 |
| Fidelity | 1.000000 | 0.999279 | 0.997233 |
| Relative Error | <10⁻¹⁰% | 0.00993% | 0.252% |
| Runtime | 18.45 s | 210.94 s | 4.17 h |

---

# Main Scientific Findings

✔ Machine precision was achieved for the TFIM benchmark.

✔ The Heisenberg model reached sub-chemical accuracy with fidelity above 0.999.

✔ The Hubbard model reproduced the exact ground state with only 0.252% relative error.

✔ Circuit depth alone is **not** a reliable predictor of VQE computational cost.

✔ Optimization complexity is primarily driven by the number of variational parameters and repeated gradient evaluations.

---

# Running the Code

Clone the repository

```bash
git clone https://github.com/sswaid991-bit/VQE-Lattice-Models.git
```

Install dependencies

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook

```bash
jupyter notebook
```

Run any notebook

- TFIM.ipynb

- Heisenberg.ipynb

- Hubbard.ipynb

---

# Reproducibility

All numerical results reported in the accompanying manuscript can be reproduced directly from the notebooks included in this repository.

The implementation follows exactly the simulation settings used in the paper.

---

# Citation

If you use this repository in your research, please cite the accompanying paper.

A formal citation file (`CITATION.cff`) is included in this repository.

---

# License

This project is released under the MIT License.

---

# Contact

Saleh Swaid

Department of Physics

University of Management and Technology (UMT)

Lahore, Pakistan

Email:

sswaid991@gmail.com

---

## Acknowledgements

The authors acknowledge the Department of Physics, School of Science, University of Management and Technology (UMT), Lahore, Pakistan, for providing research facilities and academic support throughout this work.
