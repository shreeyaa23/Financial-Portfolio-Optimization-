# Financial Portfolio Optimization — Blair & Rosen, Inc.

**Author:** Shreya Mishra   
**Location:** Richmond, VA  
**Tools:** Excel Solver | Python (PuLP) | AMPL  

---

## Overview
This project models an investment portfolio optimization problem for **Blair & Rosen, Inc.**, a brokerage firm that designs client portfolios based on risk tolerance.  
Using **Excel Solver**, **Python (PuLP)**, and **AMPL**, the model determines the optimal allocation between an Internet Fund and a Blue-Chip Fund to maximize annual return while staying within investment and risk limits.

---

## Objective
**Goal:** Maximize total annual return from two investment options.

### Constraints
- Total investment ≤ \$50,000  
- Investment in Internet Fund ≤ \$35,000  
- Portfolio risk rating ≤ 240  
- Non-negativity for all decision variables  

---

## Model Formulation

### Decision Variables
- \( x_{internet} \): Amount invested in the Internet Fund (\$)  
- \( x_{bluechip} \): Amount invested in the Blue-Chip Fund (\$)

### Objective Function
\[
\text{Maximize } Z = 0.12x_{internet} + 0.09x_{bluechip}
\]

### Subject To
\[
\begin{aligned}
x_{internet} + x_{bluechip} &\le 50{,}000 \\
x_{internet} &\le 35{,}000 \\
6(x_{internet}/1000) + 4(x_{bluechip}/1000) &\le 240 \\
x_{internet}, x_{bluechip} &\ge 0
\end{aligned}
\]

---

## Methodology

| Platform | Technique | Purpose |
|-----------|------------|----------|
| **Excel Solver** | Linear programming | Baseline optimization model |
| **Python (PuLP)** | Linear optimization with LpMaximize | Automation and reproducibility |
| **AMPL** | Algebraic modeling language | Cross-verification of solution |

---

## Results

| Fund | Optimal Allocation (\$) | Return Rate | Annual Return (\$) |
|------|--------------------------|--------------|--------------------|
| Internet Fund | 20,000 | 12% | 2,400 |
| Blue-Chip Fund | 30,000 | 9% | 2,700 |
| **Total** | **50,000** | — | **5,100** |

**Optimal Strategy:**  
Invest \$20,000 in the Internet Fund and \$30,000 in the Blue-Chip Fund to achieve the maximum annual return of **\$5,100**, maintaining a total risk rating of 240 within the \$50,000 budget.

---

## Tools & Technologies
- **Excel Solver:** Constraint-based optimization  
- **Python (PuLP, pandas):** Model automation and validation  
- **AMPL:** Model definition and solution verification  
- **Google Colab:** Interactive execution and documentation  

---

## Key Insights
- The **Internet Fund** delivers higher returns but increases portfolio risk.  
- The **Blue-Chip Fund** stabilizes returns within the client’s moderate risk profile.  
- The optimal mix demonstrates how **prescriptive analytics** supports data-driven investment recommendations.

---

## Project Type
**Prescriptive Analytics · Linear Optimization · Financial Modeling**

---
