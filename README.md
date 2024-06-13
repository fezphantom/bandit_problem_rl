# bandit_problem_rl
### README

# Bandit Algorithms for Non-Stationary Environments

## Overview

This project implements and evaluates various bandit algorithms in both stationary and non-stationary environments. The main objective is to compare the performance of different methods in adapting to changes in reward distributions, both gradual and abrupt.

## Contents

- `k_armed_bandit.ipynb`: Main Python file containing implementations of different bandit algorithms,experiments and plots.
- `README.md`: This readme file.
- `results/`: Directory containing result files and plots.
- `requirements.txt`: List of required Python packages.

## Requirements

To install the required packages, run:
```
pip install -r requirements.txt
```

## Bandit Algorithms

### Implemented Methods

1. **Greedy with Non-Optimistic Initial Values**: Initializes action values to 0 and uses the incremental implementation of the simple average method.
2. **Epsilon-Greedy**: Explores with a probability epsilon and exploits the current best option otherwise.
3. **Optimistic Initial Values**: Initializes action values to a higher value to encourage exploration initially.
4. **Gradient Bandit**: Uses a preference-based method with different learning rates to balance exploration and exploitation.

### Non-Stationary Modifications

1. **Gradual Changes**:
   - Drift change: `μt = μt-1 + ϵt` where `ϵt` is `N(0, 0.001^2)`.
   - Mean-reverting change: `μt = κμt-1 + ϵt` where `κ = 0.5` and `ϵt` is `N(0, 0.01^2)`.

2. **Abrupt Changes**:
   - At each time step, with a probability of 0.005, permute the means corresponding to each of the reward distributions.

## Running Experiments

1. **Stationary Environment**

2. **Non-Stationary Environment**

## Evaluation

1. **Stationary Environment**:
   - Average accumulated reward over time.
   - Proportion of time the optimal action is taken.

2. **Non-Stationary Environment**:
   - Distribution of the average reward attained after a large number of steps (10,000 or 20,000).
   - Box plots to present the terminal reward distributions.


## Results

The results of the experiments, including plots of average rewards and optimal action percentages, can be found in the `results/` directory. The performance of different algorithms is evaluated based on their adaptability to non-stationary environments.

## References

- Duran-Martin et al., "Bandits for Non-Stationary Environments" (2022): [Paper](https://proceedings.mlr.press/v151/duran-martin22a/duran-martin22a.pdf)
- Chang et al., "Reinforcement Learning for Non-Stationary Environments" (2023): [Paper](https://proceedings.mlr.press/v232/chang23a/chang23a.pdf)

## Contact

For any queries, please contact [Your Name] at [Your Email].

---

This readme provides a comprehensive guide to understand and replicate the results of the bandit algorithm experiments for both stationary and non-stationary environments.