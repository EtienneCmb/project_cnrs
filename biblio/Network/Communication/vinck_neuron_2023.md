---
tags:
  - CTC
  - Review
  - Communication
  - CFC
  - FC
  - FeedForward
  - FeedBack
  - PredictiveCoding
  - PredictionError
  - Resonance
  - CTR
  - NonLinear
  - Timescales
  - Hierarchy
  - LFP
---
# Principles of large-scale neural interactions
Vinck, _Neuron_, 2023

---

## Highlights
---

> [!INFO] What **mechanisms** underlie flexible inter-areal communication in the cortex?
> 1. **CTC is not a viable mechanism**. They propose that #Resonance and #NonLinear integration are alternatives to consider
> 3. **Feedforward in $\gamma$ and feedback in $\alpha / \beta$ are questioned**. Instead they propose that :
> 	- #FeedForward propagation of #PredictionError are supported by non-linear amplification of aperiodic transient 
> 	- #FeedBack via #Resonance for information encoding 


## Origin of the #LFP signal
---

- Reminder to check this before : [[neuron]]
- Enregistrement du milieu extra-cellulaire
	1. Un spike provoque la libération des neuro-transmetteurs au niveau de la synapse $\Rightarrow$ courant extra-cellulaire
	2. Charges s'accumulent sur le neuron d'après $\Rightarrow$ courant extra-cellulaire
- Donc le LFP **capture à la fois la cause des spikes et la conséquence des spikes**


## Destruction of #CTC
---

- **CTC :** effective communication occurs when pre-synaptic inputs arrive at excitable phase of a receiver $\Rightarrow$ #Synchronization 
- Two definitions :
	- *CTC-1 :* phase synchronization
	- *CTC-2 :* coherence without phase shift
-  Main arguments :
	- Small values of coherence (0.09)
	- **Coherence is a consequence of linear signal transmission** (see Schneider, Vinck et al. *Neuron*) : larger coherences are obtained for inputs with strong power combine to strong inter-areal connection weight (model). The receiver gets a copy of sender's power and noise which produces a coherence between the two without necessarily a peak in receiver's PSD (I don't get why...). _It reflects the coherence between the sender and its own copy_
	- #FeedForward : originates from L3/L5 and terminate in L4 (Granular layer); #FeedBack : originates from L2/L6 and terminate in both supra and infragranular layers
	- Inter-areal projections are mainly supported by excitatory neurons (_long-range_) while inhibitory neurons mostly project locally $\Rightarrow$ **it's necessary to dissociate cell types**

![[Pasted image 20230919111817.png]]


## Alernatives to CTC: #Resonance and #NonLinear transformations
---

- Starting point of alternatives: **linear signal transfer** and **integration**. #Resonance might be used or integration to amplify specific input

### Communication through resonance

> [!ERROR]
> - Alternative to the #CTC
> - #CTR : communication is facilitated when the sending population shifts its energy (i.e. PSD) toward the receiver's resonance peak. Not so far from Kohn's idea of #CommunicationSubspace ([[kohn_2020_trends]])


![[Pasted image 20230919133204.png]]


### Information transfer and non-linear integration

- He proposes that 

## #Hierarchy, #FeedForward and #FeedBack 
---


## Reference
---
Vinck, M., Uran, C., Spyropoulos, G., Onorato, I., Broggini, A.C., Schneider, M., and Canales-Johnson, A. (2023). Principles of large-scale neural interactions. Neuron _111_, 987–1002.