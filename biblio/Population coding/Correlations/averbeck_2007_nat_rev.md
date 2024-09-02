---
tags:
  - PopulationCoding
  - NoiseCorrelation
  - SignalCorrelation
  - ProbabilisticCoding
  - Synchronization
  - BindingBySynchrony
---
# Neural correlations, population coding and computation
Averbeck, Pouget, _Nature Reviews_, 2007
#PopulationCoding #NoiseCorrelation #SignalCorrelation #ProbabilisticCoding #Synchronization #BindingBySynchrony

---

<br>

## Highlights
---

> [!INFO]
> This review focus on the impact of correlations within a population of neurons. Empirical studies and theoretical work have proved that **correlations within a population can either increase or decrease the amount of information encoded in the population.** 

<br>

## Description
---
### Problematic 
- **Neurons are noisy :** Hard to understand #PopulationCoding because even when presenting the same stimulus twice, the pattern of activity _never occur twice_. Therefore, the coding has to be #ProbabilisticCoding 
- Even if patterns of activity of single neurons are not completely reproducible, there's the presence of correlation between the "noise" of pairs of neurons
- Two approaches have been used to study the impact of this correlation in the noise:
	1. **Encoding :** i.e. whether adding correlation in a population can increase/decrease the amount of information in the population
	2. **Decoding :** this approach asks the question of how much we can decode from a population with/without correlation
### Definitions
- **Population code =** tuning curve + noise
	- _Tuning curve =_ across-trials average of responses to a set of stimulus
	- _Noise =_ Trial-to-trial variability in the responses
- #NoiseCorrelation = the trial-to-trial variability is correlated across neurons. For example, if for the same stimulus, there's variability in the response of a first neuron, the same variability happens in an other neuron
- #SignalCorrelation = correlation in the average response (i.e. similar tuning curve). For example, the firing rate of two neurons increase with the pitch of the voice

### The "Encoding" perspective $\Delta I_{shuffled}$  
#### Method
How much correlations in a population can affect the amount of information in a population code can be estimated using: $\Delta I_{shuffled} = I- I_{shuffled}$ where :
- I = total information contained in the population **with** correlation
- $I_{shuffled}$ = total information contained in the population **without** correlation. In practice, this one is simply computed by shuffling the trials
- The maximum amount of information is **bounded by the total information encoded by sensory systems** (retina, cochlea etc...)

Noise correlation can either **increase or decrease the amount of information, but the effect is small**

#### Link with binding-by-synchrony
- Binding-By-synchrony ( #Synchronization #CTC ) = {Milner; Malsburg; Singer; Fries}
- **Definition :** Number of synchronous spikes across pairs of neurons depends on whether the pair represents the same stimulus
- It means that a lot of information is contained in the interactions $\leftrightarrow$ $\Delta I_{shuffled} > 0$ because _shuffling removes synchronous spikes_
- Findings go against those the binding-by-synchrony hypothesis because the shuffling removes only small amount of information

### The "Decoding" perspective $\Delta I_{diag}$
- **Question :** whether downstream neurons have to know about correlations to extract all the available information
- **Method :** train an optimized decoder on the shuffled data and applied it to the untouched data containing the correlations = $\Delta I_{diag} = I - I_{diag}$

<br>

## Reference
---
Averbeck, B.B., Latham, P.E., and Pouget, A. (2006). Neural correlations, population coding and computation. Nature Reviews Neuroscience _7_, 358–366. [10.1038/nrn1888](https://doi.org/10.1038/nrn1888).