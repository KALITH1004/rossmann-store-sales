# Bayesian Network-Based Query System for Retail Sales Analysis

<p align="center">
  <strong>Liang Yirui (Loey), Chen Qianqi (Kiki), Li Minghao (Aiur)</strong>
</p>

<p align="center">
  Beijing Normal-Hong Kong Baptist University (BNBU)
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/pgmpy-Bayesian%20Network-blue">
  <img src="https://img.shields.io/badge/NetworkX-Graph%20Modeling-green">
  <img src="https://img.shields.io/badge/Gradio-Interactive%20UI-orange">
  <img src="https://img.shields.io/badge/Kaggle-Rossmann%20Dataset-20BEFF?logo=kaggle&logoColor=white">
</p>

## 1. Overview

This project develops a Bayesian Network-based probabilistic query system for retail sales analysis using the Rossmann Store Sales dataset.

By integrating domain knowledge, data-driven structure learning, and probabilistic inference, the system models dependencies among sales, customer traffic, promotions, holidays, store operations, and competition distance.

An interactive Gradio interface enables users to specify evidence and explore conditional probability distributions under different business scenarios.

## 2. Methodology

| Component | Description |
| :--- | :--- |
| **Data Preprocessing & EDA** | Data cleaning, correlation analysis, feature selection, and variable discretization. |
| **Preset DAG** | Construction of a Directed Acyclic Graph based on retail business knowledge. |
| **Structure Learning** | Constrained Hill Climbing with the Akaike Information Criterion (AIC). |
| **Parameter Learning** | Maximum Likelihood Estimation (MLE) for Conditional Probability Distributions (CPDs). |
| **Model Validation** | Analysis of local independence, active trails, and V-structures. |
| **Probabilistic Inference** | Clique Tree-based Belief Propagation for conditional probability queries. |
| **Interactive Query System** | Gradio-based interface for evidence selection and probability visualization. |

### Workflow

```text
Rossmann Store Sales Dataset
            ↓
Data Preprocessing & EDA
            ↓
Domain Knowledge-Based DAG
            ↓
Hill Climbing + AIC
            ↓
Maximum Likelihood Estimation
            ↓
Bayesian Network Validation
            ↓
Clique Tree & Belief Propagation
            ↓
Interactive Gradio Query System
```

## 3. Key Features

- Domain knowledge-guided Bayesian Network construction.
- Data-driven graph structure optimization.
- Conditional probability estimation and graphical model validation.
- Evidence-based retail sales analysis.
- Interactive probabilistic queries and visualization.

## 4. Dataset

The project uses the [Rossmann Store Sales Dataset](https://www.kaggle.com/competitions/rossmann-store-sales/data), containing historical retail sales records and store-level information.

The Bayesian Network models nine variables:

`Sales`, `Customers`, `Promo`, `Open`, `DayOfWeek`, `StateHoliday`, `SchoolHoliday`, `CompetitionDistance`, and `Assortment`.

## 5. Getting Started

Install the required dependencies:

```bash
pip install pandas numpy matplotlib seaborn plotly networkx pgmpy scipy gradio jupyter
```

Download the dataset from Kaggle and organize the files as follows:

```text
.
├── BN_Group5.ipynb
├── data/
│   ├── train.csv
│   └── store.csv
└── README.md
```

Launch Jupyter Notebook:

```bash
jupyter notebook BN_Group5.ipynb
```

Run the notebook sequentially to construct the Bayesian Network, perform probabilistic inference, and launch the interactive query interface.


## Acknowledgements

This project uses the Rossmann Store Sales dataset from Kaggle and open-source tools including pgmpy, NetworkX, and Gradio.
