# The structures and functions of correlations in neural population codes
Panzeri, _Nature reviews in Neuroscience_, 2022
#PopulationCoding #PopulationCode #SignalCorrelation #NoiseCorrelation #Manifolds #FC #HOI #Timescales #Review

---

## Introduction
---

### Beyond individual neurons

> [!WARNING]
> Emerging functions from population of neurons beyond the information provided by individual neurons?


- #PopulationCode two definitions:
	1. **Independent population code** = Amount of information provided by individual neurons + joint representation (e.g. place cells). *Space of neural population activity* (aka #Manifolds I guess) describing the geometry of the encoding of behavioral variables $\Rightarrow$ neglects functional interactions between neurons
	2. **Correlated population code** = Emerging function arising from the functional interactions between neurons of a population that can't be explained by the information carried by individual neurons $\Leftrightarrow$ #NoiseCorrelation 

### Influence of correlations on population code

> [!WARNING]
> How correlations within a population (i.e. structure, organization) are shaping population code?

- **Structured correlated population code** = population code is shaped by the structure of the correlations in a population (e.g. neurons with similar tuning might also engage in similar #NoiseCorrelation ). Can be be based on pairwise interactions of #HOI
- **Three main functions of correlations in a population**:
	1. *Shaping the encoding of information* (increase/decrease/unaffect)
	2. Generate code across *multiple #Timescales*
	3. Facilitate *information transmission and readout* by downstream neurons/areas (linear and non-linear encoding)

## Encoding and correlation structure
---
> [!WARNING]
> Influence of correlations in the information carried by a population of neurons

### Definitions
- Two types of correlations:
	1. #SignalCorrelation = similarity of stimulus tuning of different neurons
	2. #NoiseCorrelation = correlations between single-trial of pairs of neurons
- Here, increase/decrease of amount of information refer to how much we can discriminate two stimuli. The more we can discriminate them, the more information 

![[panzeri_noise_corr.png]]

### Theory
- On the left: #SignalCorrelation and #NoiseCorrelation have the **same sign** $\Rightarrow$ increasing overlaps in distributions $\Rightarrow$ decreasing discriminability $\Rightarrow$ decrease information
- On the right: #SignalCorrelation and #NoiseCorrelation have **opposite signs** $\Rightarrow$ decreasing overlaps in distributions $\Rightarrow$ increasing discriminability $\Rightarrow$ increase information
- Here, the #NoiseCorrelation is stimulus-independent. But in the case of stimulus-dependent #NoiseCorrelation, discriminability and information can change drastically. It can be the **only changing parameter**
- Recent theoretical models suggest that #NoiseCorrelation imposes **fundamental limits on the amount of information that can be encoded** $\Rightarrow$ it's bounding the total information

### Structured correlation
- Heterogeneous populations help decoding stimulus
- #NoiseCorrelation might be more efficient than changes of selectivity $\Rightarrow$ structure of the population matters a lot
- #RedundantCoding in pairs of neurons = *less* information in the joint representation than the sum of individual contributions $I(X1; X2) < I(X1) + I(X2)$
- #SynergisticCoding in pairs of neurons = *more* information in the joint representation than the sum of individual contributions $I(X1; X2) > I(X1) + I(X2)$
- #Redundant hubs preferentially interact with #Redundant hubs and #Synergistic hubs preferentially interact with #Synergistic hubs $\Rightarrow$ #Synergy is used to maximize information encoding and #Redundancy offers a backbone of robustness in case of loss of cells

### Pairwise and Higher order correlations
- Correlations can be removed analytically (see $\Delta I_{diff}$ and $\Delta I_{diag}$ in [[averbeck_2007_nat_rev]])
- #HOI should mainly have information-limiting influence for information encoding

## Correlations and encoding timescales
---
- Timescales are different for *perception* (fast) and *behavioral production* (possibly slow - might require accumulating information). Can be estimated using across-time correlation
	- During decision-making/memory tasks = neurons in frontal lobe showed *persistent* activity
	- Also, some neurons showed *Ramping activity* during the accumulation of sensory evidences
- Setting the optimal timescales might be a function of population codes

## Are codes read out optimally?
---
- The amount of information transmitted and used for behavior depends on properties of encoding and readout
- More complex non-linear encoding could improve readout quality (see [[panzeri_2015_tics]])
- #NoiseCorrelation limit the encoding of information but improve readout by downstream neurons

## Information transmission and behaviour
---

- **Important parameters/biophysical factors influencing readout:**
- *Close inputs in space and time* : Integration time constants of neurons are shorts (~5-10ms). Correlated synaptic inputs (i.e. inputs arriving close in time and space ~ biding-by synchrony) might enhance the propagation to downstream neurons
- *Presynaptic inputs are correlated* : When inputs show consistent encoding ⇒ higher correlation ⇒ better readout
- *Higher order correlation* : #HOI improve readout compared to pairwise correlations

## Using perturbations to probe function
---
- Causal role of correlations within a population requires manipulating neural activity, for example using two-photon optogenetics


<br>

## Reference
---
Panzeri, S., Moroni, M., Safaai, H., and Harvey, C.D. (2022). The structures and functions of correlations in neural population codes. Nat Rev Neurosci _23_, 551–567. [10.1038/s41583-022-00606-4](https://doi.org/10.1038/s41583-022-00606-4).