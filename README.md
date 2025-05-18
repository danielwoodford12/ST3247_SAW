# EDIT RESULTS, TECH, AND REFERENCES PLEASE
# Structured Sampling of 2D Walk Spaces via Monte Carlo Methods

This project implements advanced Monte Carlo sampling techniques to estimate the **connective constant (μ)** for *self-avoiding walks* (SAWs) on a 2D square lattice. Using **Sequential Monte Carlo (SMC)**, **pivot-based recursive sampling**, and probabilistic estimators, we achieved **<0.1% error** compared to theoretical benchmarks for walk lengths up to **L = 2560**.

---

## 🔍 Background

A *self-avoiding walk* is a lattice path that does not revisit the same point. These walks are used to model polymer chains in statistical physics, and their growth rate is captured by the **connective constant** μ:

\[
\mu = \lim_{n \to \infty} C_n^{1/n}
\]

where \( C_n \) is the number of self-avoiding walks of length \( n \). For 2D square lattices, μ is known to be approximately:

\[
\mu \approx 2.63815853035
\]

Our goal was to **estimate μ empirically** by simulating long walks and applying **recursive estimators** based on sampled counts.

---

## 💡 Key Methods

- **Sequential Monte Carlo (SMC):**  
  Used to extend walks iteratively with importance sampling and resampling, incorporating mutation steps to maintain diversity.

- **Pivot-Based Recursive Sampling:**  
  Employed to generate diverse SAWs and recursively estimate growth ratios \( C_n / C_{n-1} \).

- **Log-space Estimation:**  
  Used log-domain summation (log-sum-exp) to prevent underflow in recursive calculations over large walks.

- **Degeneracy Reduction:**  
  Introduced pivot mutations during resampling to reduce particle duplication and improve convergence.

---

## Methods
-Naive Monte Carlo
-Rosenbluth Method
-Sequential Monte Carlo (SMC)
-Pivot-Based 

## 📊 Results

- Achieved **μ̂ ≈ 2.6397** using SMC with pivot mutations for L ≈ 2000–2560  
- **Relative error** compared to known μ:  
  \[
  \frac{|2.6397 - 2.6382|}{2.6382} \approx 0.057\%
  \]
- Demonstrated reliable convergence at longer lengths where exact enumeration becomes infeasible
- Validated estimates against OEIS benchmark values for short-length SAWs

---

## Technologies

- **Languages:** Python
- **Libraries:** NumPy, matplotlib, SciPy (for numerical support)

---

## Future Work

- Explore Domb-Joyce-style energy weighting to enable multicanonical sampling  
- Extend to 3D lattice SAWs  
- Apply methods to simulate polymers with repulsion or attraction constraints

---

## References

- Madras, N., & Slade, G. (1996). *The Self-Avoiding Walk*.  
- OEIS A001411 – Number of self-avoiding walks  
- Lawler, G. F. (2004). *The connective constant of the square lattice*
