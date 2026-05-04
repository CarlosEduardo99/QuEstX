# QuEstX: Large-Scale NISQ Circuit Fidelity Prediction

This repository contains the source code, datasets, and experimental frameworks described in the paper **"Large-Scale NISQ Circuit Fidelity Prediction using Graph Transformer to Explore the Technological Frontier"**.

The project extends the **QuEst** framework, utilizing a **Graph Transformer** architecture to predict quantum circuit fidelity through the **PST (Probability of Successful Trial)** proxy in large-scale regimes.

## 🚀 Overview

The core objective of this study is to evaluate the generalization capabilities of the QuEst model beyond its original constraints (10 qubits and 4 gate types), exploring regimes of up to 18 qubits and 13 different logic gates.

### Key Contributions:
*   **Progressive Replication:** Re-implementation of the original QuEst environment using Python 3.12.2 and the current Qiskit API, achieving $R^{2} \ge 0.93$ across real IBM backends.
*   **Novel Datasets (D1 & D2):** Generation of PST-labeled datasets for circuits with up to 10 qubits and 13 gate types (D1), and 15–18 qubits (D2).
*   **Scalability Analysis:** Controlled experiments identifying the "native ceiling" for larger circuits and highlighting the bottleneck of fixed one-hot qubit-index encoding.

## 📊 Experimental Results

| Experiment | Dataset | Description | $R^{2}$ Result |
| :--- | :--- | :--- | :--- |
| **E1** | D0 | Successful replication of the baseline model | $0.984$ |
| **E2** | D1 | Gate-set expansion (13 types) absorbed by the GT | $0.950$ |
| **E3.2** | D2 | Native training ceiling (15–18 qubits) | $0.796$ |

## 🛠️ Tech Stack
*   **Language:** Python 3.12.2
*   **Quantum Framework:** Qiskit (Circuit-to-DAG conversion and FakeBackend simulations)
*   **Deep Learning:** PyTorch Geometric (Graph Transformer with Multi-head Self-attention)

## 🔮 Future Work
Planned extensions include the creation of **Dataset D3** (covering up to 50 qubits) and the implementation of **continuous positional encoding** to overcome current representational limitations as we approach the quantum advantage threshold.
