# Financial Portfolio Optimization — Blair & Rosen, Inc.

## Project Overview
This project models an investment portfolio optimization problem for Blair & Rosen, Inc., a brokerage firm that designs client portfolios based on risk tolerance.  
Using **Excel Solver**, **Python (PuLP)**, and **AMPL**, the model determines the optimal allocation between an Internet Fund and a Blue-Chip Fund to maximize annual return while staying within the client’s investment and risk limits.

---

## Objective
**Goal:** Maximize total annual return from two investment options.  
**Constraints:**
- Total investment ≤ $50,000  
- Investment in Internet Fund ≤ $35,000  
- Total portfolio risk rating ≤ 240  
- Non-negativity for all decision variables  

---

## Model Formulation

### Decision Variables
- `x_internet`: amount invested in the Internet Fund ($)  
- `x_bluechip`: amount invested in the Blue-Chip Fund ($)

### Objective Function
\[
\text{Maximize } Z = 0.12x_{internet} + 0.09x_{bluechip}
\]

### Constraints
\[
\begin{align*}
x_{internet} + x_{bluechip} &\le 50,000 \\
x_{internet} &\le 35,000 \\
6(x_{internet}/1000) + 4(x_{bluechip}/1000) &\le 240 \\
x_{internet}, x_{bluechip} &\ge 0
\end{align*}
\]

---

## Methodology
| Platform | Technique | Purpose |
|-----------|------------|----------|
| Excel Solver | Linear programming | Baseline optimization model |
| Python (PuLP) | Linear optimization using `LpMaximize` | Automation and reproducibility |
| AMPL | Algebraic modeling language | Cross-verification of the solution |

---

## Results
| Fund | Optimal Allocation ($) | Return Rate | Annual Return ($) |
|------|-------------------------|--------------|-------------------|
| Internet Fund | 20,000 | 12% | 2,400 |
| Blue-Chip Fund | 30,000 | 9% | 2,700 |
| **Total Return** | — | — | **5,100** |

**Optimal Strategy:**  
Invest $20,000 in the Internet Fund and $30,000 in the Blue-Chip Fund to achieve the maximum return of **$5,100 per year**, while maintaining a risk rating of 240 within the total budget of $50,000.

---

## Tools and Technologies
- **Excel Solver:** Constraint-based linear optimization  
- **Python:** PuLP, pandas  
- **AMPL:** Model definition and solution validation  
- **Google Colab:** Interactive execution and documentation  

---

## Key Insights
- The Internet Fund offers higher returns but greater risk; the Blue-Chip Fund stabilizes the overall portfolio.  
- The optimal mix balances return potential with moderate risk tolerance.  
- Demonstrates how prescriptive analytics can guide data-driven investment recommendations.  


---

## Author
**Shreya Mishra**  
Business Intelligence & Data Analyst  
MBA in Business Analytics | Excel | Power BI | SQL | Python | AMPL | Optimization Modeling  
Richmond, VA  
