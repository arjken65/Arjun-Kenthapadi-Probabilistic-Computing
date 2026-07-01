# Probabilistic_Computing

This repository collects the notebooks I use for the probabilistic computing course at the University of California Santa Barbara.

The main goal is to make the algorithms visible. Instead of treating sampling, Markov chains, annealing, and p-bits as black boxes, each notebook walks through the core idea with simple code, numerical experiments, and plots. The notebooks are meant to be read, modified, and rerun while learning the material.

## What is in this repository?

The examples move from basic probability ideas to Monte Carlo methods, Markov chain Monte Carlo, and probabilistic computing models.

| Notebook | Main idea |
| --- | --- |
| `law_of_large_number.ipynb` | A toy simulation showing how sample averages stabilize as the number of trials grows. |
| `CLT.ipynb` | A graphical demonstration of the Central Limit Theorem using repeated coin-toss experiments. |
| `fundamental_theorem_of_simulation.ipynb` | Monte Carlo area estimation using the Fundamental Theorem of Simulation idea. |
| `FTS_example.ipynb` | Another FTS-style example with visualization. |
| `inverse_sampling_theorem.ipynb` | Sampling from a desired distribution using inverse transform sampling. |
| `accept_reject_example.ipynb` | Accept-reject sampling for a nontrivial target function, including the normalization check. |
| `importance_sampling.ipynb` | Comparing standard Monte Carlo with importance sampling for integral estimation. |
| `monte_carlo_integration_high_dimensional.ipynb` | Monte Carlo integration in high dimensions and why grid-based Riemann sums become expensive. |
| `autocorrelation.ipynb` | Autocorrelation of random sequences and how dependence shows up in samples. |
| `simple_markov_chain.ipynb` | Evolution of a simple Markov-chain distribution over time. |
| `MH_algorithm.ipynb` | Metropolis-Hastings sampling for a one-dimensional target distribution. |
| `MH_arc_circle.ipynb` | Metropolis-Hastings on a two-dimensional state space inside an upper semicircle. |
| `systematic_scan_gibbs.ipynb` | Gibbs sampling for a bivariate Gaussian using systematic scan updates. |
| `parallel_tempering_SK.ipynb` | Parallel tempering for the Sherrington-Kirkpatrick spin-glass model. |
| `bayesian_networks.ipynb` | Sampling and checking a small Bayesian network: Cloud, Sprinkler, Rain, and Grass. |
| `three_pbits.ipynb` | A three-pbit frustrated triangle and convergence to the equilibrium distribution. |
| `graph_coloring_Potts_model.ipynb` | Graph coloring using a Potts-model view and annealed Gibbs sampling. |
| `TSP_population_annealing.ipynb` | Population annealing applied to a small Traveling Salesman Problem example. |
| `Monty_hall.ipynb` | Monte Carlo simulation of the Monty Hall problem. |

## Suggested order

If you are going through the material for the first time, I suggest this order:

1. Start with `law_of_large_number.ipynb` and `CLT.ipynb`.
2. Move to simulation and sampling: `fundamental_theorem_of_simulation.ipynb`, `inverse_sampling_theorem.ipynb`, `accept_reject_example.ipynb`, and `importance_sampling.ipynb`.
3. Study Markov chains and MCMC: `simple_markov_chain.ipynb`, `MH_algorithm.ipynb`, `MH_arc_circle.ipynb`, and `systematic_scan_gibbs.ipynb`.
4. Then look at the probabilistic computing examples: `three_pbits.ipynb`, `graph_coloring_Potts_model.ipynb`, `parallel_tempering_SK.ipynb`, and `TSP_population_annealing.ipynb`.

## How to run the notebooks

The notebooks are written in Python and mainly use NumPy and Matplotlib. A few notebooks also use `joblib` for parallel execution and IPython display tools for animations.

```bash
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter joblib
jupyter lab
```

Then open any notebook and run the cells from top to bottom.

## Notes

These notebooks are teaching material, not a packaged software library. I keep the code direct on purpose so the connection between the equations, the algorithm, and the plots stays easy to see.

Some notebooks include generated figures or animations, so a few files are larger than plain source notebooks. If a plot or animation does not show correctly on GitHub, open the notebook locally and rerun the cells.

## Course context

This repository supports the probabilistic computing course at UCSB. The examples are intended to help students build intuition for:

- Monte Carlo estimation
- sampling from nontrivial distributions
- Markov chains and convergence
- Metropolis-Hastings and Gibbs sampling
- annealing-based algorithms
- probabilistic bits and energy-based models
- simple probabilistic graphical models

I will keep updating the notebooks as the course material grows and as I clean up more examples.
