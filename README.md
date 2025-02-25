# CRV Token Governance Centralization Analysis

This repository contains the dataset, retrieved from Dune Analytics on **12/02/2025**, of CRV token balances. It also includes a Jupyter Notebook that computes the **Nakamoto Coefficient** and **Gini Coefficient**, two key metrics used to assess governance centralization within the Curve Finance ecosystem.

## 📊 **Overview**

In decentralized finance (DeFi) ecosystems, token distribution plays a crucial role in governance decentralization. This project analyzes CRV token balances to measure the concentration of voting power using:

1. **Nakamoto Coefficient** – Measures the minimum number of entities needed to collude to gain more than 50% control of the voting power.
2. **Gini Coefficient** – A statistical measure of inequality that reflects the distribution of token ownership, ranging from 0 (perfect equality) to 1 (perfect inequality).

---

## 🧑‍🔬 **Methodology**

Below are the core steps of the methodology followed:

### 1. **Data Collection**
- The CRV token balance data was collected using Dune Analytics as of **12/02/2025**.
- The data consists of wallet addresses and their corresponding token holdings.
- System account holdings were removed from the dataset.
  
### 2. **Calculating the Nakamoto Coefficient**
- This coefficient measures the minimum number of addresses holding more than 50% of the total token supply.
- Formula:

```
N = min { k | Σ(i=1 to k) S_i > (1/2) Σ(j=1 to n) S_j }
```

Where:
- `S_i` is the share of tokens held by the `i-th` largest address.
- `N` is the smallest number of addresses that hold the majority of the tokens.

### 3. **Calculating the Gini Coefficient**
- Measures inequality of the token distribution.
- Formula:

```
G = (Σ(i=1 to n) Σ(j=1 to n) |x_i - x_j|) / (2 * n^2 * x̄)
```

Where:
- `x_i` and `x_j` are token balances for addresses `i` and `j`.
- `x̄` is the mean of all balances.

---


