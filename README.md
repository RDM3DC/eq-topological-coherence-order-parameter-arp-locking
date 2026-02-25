# Topological Coherence Order Parameter (ARP Locking)

**ID:** `eq-topological-coherence-order-parameter-arp-locking`  
**Tier:** derived  
**Score:** 92  
**Units:** OK  
**Theory:** PASS  

## Equation

$$
\Psi = \frac{1}{N_p} \sum_{p=1}^{N_p} \cos\!\left(\frac{\Theta_p}{\pi_a}\right)
$$

## Description

Scalar order parameter for the ARP Z\u2082 locking phase transition. Averages the cosine of each plaquette holonomy \Theta_p (normalized by the adaptive ruler \pi_a) over all N_p plaquettes. \Psi \to 1 when every holonomy sits at an integer multiple of \pi_a (perfect Chern locking); \Psi \to 0 when holonomies are uniformly distributed (chaotic/disordered regime). Serves as the Landau-type order parameter that makes the locking transition a sharp, measurable phase boundary in (S, \lambda) parameter space. Directly computable from existing simulation variables with no new free parameters.

## Assumptions

- \Theta_p is the signed plaquette holonomy from the Phase-Lift framework (LB Plaquette Holonomy equation)
- \pi_a is the adaptive angular ruler from the companion ODE \dot{\pi}_a = \alpha_\pi S - \mu_\pi(\pi_a - \pi_0)
- N_p is the number of plaquettes in the ARP lattice (fixed topology, typically L^2 for square lattice)
- Locked regime: \Theta_p \approx 2n\pi_a for integer n, so cos(\Theta_p/\pi_a) \approx 1 and \Psi \to 1
- Chaotic regime: \Theta_p uniformly distributed on (-\pi, \pi], so \langle\cos(\Theta_p/\pi_a)\rangle \to 0 by cancellation
- \Psi is dimensionless and bounded: \Psi \in [-1, 1], with \Psi > 0 indicating partial locking

## Repository Structure

```
images/       # Visualizations, plots, diagrams
derivations/  # Step-by-step derivations and proofs
simulations/  # Computational models and code
data/         # Numerical data, experimental results
notes/        # Research notes and references
```

## Links

- [TopEquations Leaderboard](https://rdm3dc.github.io/TopEquations/leaderboard.html)
- [TopEquations Main Repo](https://github.com/RDM3DC/TopEquations)
- [Certificates](https://rdm3dc.github.io/TopEquations/certificates.html)

---
*Part of the [TopEquations](https://github.com/RDM3DC/TopEquations) project.*
