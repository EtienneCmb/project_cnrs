# Large-scale signal and noise correlations configure multi-task coding in human brain networks
Ito, Murray, _Biorxiv_, 2022
#PopulationCoding #NoiseCorrelation #SignalCorrelation #FC #fMRI #GraphTheory 

---

<br>

## Highlights
---

> [!INFO]
> They used the #PopulationCoding framework using fMRI signals during resting-state and cognitive tasks. They combined this framework with #GraphTheory measures. They looked at whether #FC could be interpreted through the lens of information coding

<br>

## Description
---
### Introduction
- Two forms of correlated activity:
	1. #SignalCorrelation (SC) = similarity of task selectivity (or tuning curves) of a pair of neural units (**Mean across task-responses**)
	2. #NoiseCorrelation (NC) = correlation of trial-to-trial variability for the same task/stimulus (**Variability across task-responses**)

### Estimation of SC / NC
Let's:
```python
data.shape = (n_trials, n_roi, n_times)
```

1. #SignalCorrelation :
	1. Mean across trials `(n_roi, n_times)`
	2. Pairwise correlations across time-points: `(n_pairs,)`
2. #NoiseCorrelation : (not 100% sure)
	1. Single-trial correlation: `(n_trials, n_pairs)`
	2. Mean over trials `(n_pairs,)`
<br>

## Reference
---
Ito, T., and Murray, J.D. (2022). Large-scale signal and noise correlations configure multi-task coding in human brain networks (Neuroscience) [10.1101/2022.11.23.517699](https://doi.org/10.1101/2022.11.23.517699).