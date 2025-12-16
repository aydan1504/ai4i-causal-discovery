# AI4I Causal Discovery

This repository contains a qualitative causal discovery analysis of the **AI4I 2020 Predictive Maintenance dataset**.
Multiple causal discovery algorithms are applied to continuous sensor variables in order to compare constraint-based,
score-based, and optimization-based approaches.

The goal is not prediction, but **exploratory causal structure analysis** under different modeling assumptions.

---

## Dataset

- **Name:** AI4I 2020 Predictive Maintenance Dataset  
- **Source:** UCI Machine Learning Repository  
- **Type:** Industrial sensor data (continuous variables)

### Selected Variables

The analysis focuses on the following five continuous variables:

- Air temperature [K]  
- Process temperature [K]  
- Rotational speed [rpm]  
- Torque [Nm]  
- Tool wear [min]  

All variables are standardized before applying causal discovery methods.

---

## Methods

The following causal discovery algorithms are implemented and compared:

- **PC (Peter–Clark)** – constraint-based, conditional independence testing  
- **DirectLiNGAM** – functional causal model with non-Gaussian noise  
- **GES (Greedy Equivalence Search)** – score-based search using BIC-like scoring  
- **NOTEARS** – continuous optimization with acyclicity constraint  
- **FCI (Fast Causal Inference)** – constraint-based method allowing latent confounders  

Each method produces a causal graph or skeleton under its respective assumptions.

---

## Implementation

All experiments are implemented in a single Jupyter notebook:

AI4I_Causal_Discovery.ipynb

The notebook includes:
- Data loading and preprocessing
- Causal discovery for each algorithm
- Graph visualization using NetworkX
- Short qualitative observations for each method

---

## Evaluation

Since the AI4I dataset does not provide ground-truth causal structure, results are evaluated **qualitatively**.
Observed dependencies that appear consistently across multiple algorithms are considered more robust.

No accuracy-based metrics (e.g., F1-score) are reported.

---

## Requirements

Main Python libraries used:
- `causal-learn`
- `lingam`
- `notears`
- `scikit-learn`
- `networkx`
- `matplotlib`

All required installations are included inside the notebook.

---

## Usage

To reproduce the experiments:

1. Open `AI4I_Causal_Discovery.ipynb`
2. Mount Google Drive (dataset path can be adjusted)
3. Run the notebook cells sequentially

---

## License

This project is released under the **MIT License**.

---

## Academic Context

This repository accompanies a Master's-level project on causal discovery and is intended for
educational and research purposes.
