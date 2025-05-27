# EDIT RESULTS, TECH, AND REFERENCES PLEASE
# Structured Sampling of 2D Walk Spaces via Monte Carlo Methods

This project implements advanced Monte Carlo sampling techniques to estimate the **connective constant (μ)** for *self-avoiding walks* (SAWs) on a 2D square lattice. 

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

## Methods
-Naive Monte Carlo
-Rosenbluth 
-Sequential Monte Carlo (SMC)
-Pivot-Based Recursive Formulation

## 📊 Results

- **μ̂ ≈ 2.64029** using SMC with pivot mutations (L = 2300) 
- **μ̂ ≈ 2.63694** using pivot-based recursive formulation (L = 20,480)
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
