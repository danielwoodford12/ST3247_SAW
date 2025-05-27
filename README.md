# EDIT RESULTS, TECH, AND REFERENCES PLEASE
# Structured Sampling of 2D Walk Spaces via Monte Carlo Methods

This project implements different Monte Carlo sampling techniques to estimate the **connective constant (μ)** for *self-avoiding walks* (SAWs) on a 2D square lattice. 

---

## Background

A *self-avoiding walk* is a lattice path that does not revisit the same point. These walks are used to model polymer chains in statistical physics, and their growth rate is captured by the **connective constant** μ:

$$
\mu = \lim_{n \to \infty} C_n^{1/n}
$$

where $\( C_n \)$ is the number of self-avoiding walks of length $\( n \)$. For 2D square lattices, mu (μ) is known to be approximately:

$$
\mu \approx 2.63815853035
$$

Our goal was to **estimate μ empirically** by simulating long walks.

---

## Methods
- Naive Monte Carlo
- Rosenbluth 
- Sequential Monte Carlo (SMC)
- Pivot-Based Recursive Formulation

## Results

### Estimates
- **μ̂ ≈ 2.64029** using SMC with pivot mutations (L = 2300) 
- **μ̂ ≈ 2.63694** using pivot-based recursive formulation (L = 20,480)

### Relative Error of Estimates

#### For $\( \hat{\mu}_2 = 2.64029 \)$:

$\[
\text{Relative Error} = \left| \frac{2.64029 - 2.6381585}{2.6381585} \right| \approx 0.000807
\]$

---

#### For $\( \hat{\mu}_1 = 2.63694 \)$:

$\[
\text{Relative Error} = \left| \frac{2.63694 - 2.6381585}{2.6381585} \right|\approx 0.000462
\]$

--- 

## Technologies

- **Languages:** Python
- **Libraries:** NumPy, PyLab, Numba, 

---

## Future Work

- Implement more intelligent parallelization
- Reattempt with improved computational capabilities and longer runtimes
- Explore Domb-Joyce-style energy weighting to enable multicanonical sampling  
- Extend to 3D lattice SAWs  
- Apply methods to simulate polymers with repulsion or attraction constraints

---

## References

- A. D. Sokal. (1997). *Monte Carlo methods and statistical mechanics: Foundations and new algorithms*
- Nathan Clisby and Iwan Jensen. (2012). *A new transfer-matrix algorithm for exact enumerations: self-avoiding polygons on the square lattice*
- M. Tabrizi. (2015). *Rosenbluth Algorithm Studies of Self-avoiding Walks*
- OEIS A001411 – Number of self-avoiding walks
- Arnaud Doucet, Nando de Freitas, and Neil Gordon. *An Introduction to Sequential Monte Carlo Methods*
- Lawler, G. F. (2004). *The connective constant of the square lattice*
