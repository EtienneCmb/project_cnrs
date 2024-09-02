# Neural population coding: combining insights from microscopic and mass signals.
Panzeri, Kayser, _TICS_, 2015
#PopulationCoding #MixedSelectivity #lfp #SignalCorrelation #NoiseCorrelation #Review

---
<br>

## Description
---
### The diverse response selectivity of sensory neurons
- If individual neurons carry separated information about the stimulus, the larger the population, the more information is carried
- In practice, only a small fraction of neurons in a given population are actually carrying information $\rightarrow$ this implies that a **small-dimensional subspace** suffices to represent stimuli
### Benefits of #MixedSelectivity 
- **Question :** how to simply the readout by downstream neurons?
	- **Non-linear** mixture of selectivity (i.e. non-linear encoding) can make the decoding performed by downstream neurons much easier as an linear hyperplan can be used 
### Correlations of spike rates between neurons
- #SignalCorrelation : correlation between trial-averaged neural responses across the different stimuli, between pairs of neurons = quantify the similarity of stimulus tuning
- #NoiseCorrelation : correlation between trial-by-trial variations of responses at a _fixed stimulus_
	- It can increase/decrease/unaffect the information carried by a population
	- It might play a role in probabilistic coding by representing the uncertainty associated to stimulus variables
### Comparisons of stimulus selectivity in mass signals and spiking activity
- Two components in the M/EEG signals are particularly predictive of the firing rate:
	1. The **phase of the low-frequency** (<40Hz)
	2. The **amplitude of the high-frequency** (40-100Hz)
		 - Model of gamma generation suggest that _amplitude in the gamma band reflects local interactions between inibitory and excitatory neurons_  
 - It's unclear how specific aspects in the spiking *map with phase and power of mass signals* (M/EEG; LFP etc.) 
### Insights from the combined observations of single neurons and mass signals
- Local spiking and LFP not only depend on the phase of the LFP oscillations at the same site but also **on the phase coupling between distant sites** $\rightarrow$ direct evidence that large-scale #FC also shapes local activations
<br>

## Reference
---
Panzeri, S., Macke, J.H., Gross, J., and Kayser, C. (2015). Neural population coding: combining insights from microscopic and mass signals. Trends in Cognitive Sciences 19, 162–172. [10.1016/j.tics.2015.01.002](https://doi.org/10.1016/j.tics.2015.01.002).