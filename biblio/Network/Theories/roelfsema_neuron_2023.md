# Solving the binding problem: Assemblies form when neurons enhance their firing rate—they don’t need to oscillate or synchronize.
Roelfsema, _Neuron_, 2023
#CTC #BindingBySynchrony #Communication #Review #BBS #BBRE

---

## Highlights
---

> [!INFO]
> **Binding problem =** objects representations are highly distributed. What are the mechanisms that binds them together into a coherent representation?
> 1. By using the LFP signal, oscillations are bounding distant firing rates (Fries, Singer etc.)
> 2. Increase of firing 
> 
> Roelfsema is clearly in favor of 2.


## The binding problem
---

- There's a hierarchical decomposition of inputs
- **Binding problem = how to glue the distributed and fragmented representations of objects across many areas into a unified perception of object against the background?**

### Binding by synchrony #BBS 

- *Solution 1:* Von der Malsburg, Schneider and Wolf Singer proposed that distributed representations are coordinated through the synchronization of LFP signals ( #BBS,  #BindingBySynchrony ), which also allows having communication channels occurring at different frequencies. This theory has then by Fries with the #CTC
- *Doubts about #BBS:*
	- Gamma synchrony is a local phenomenon $\Rightarrow$ long-range synchrony is almost zero
	- Synchrony at lower frequencies vary a lot across subjects and is not related to binding
	- Synchronicity doesn't increase the efficiency of postsynaptic integration

![[roelfsema_neuron_2023_BBS.png]]

### Binding by firing rate enhancement #BBRE 

- *Solution 2:* coordination of firing rates across brain regions ( #BBRE binding by firing rate enhancement).
- Dual role of firing rates:
	1. It reflects the tuning of neurons to features and *base grouping during the feedforward processing* (feature decomposition, see below)
	2. During the feedback incremental grouping, *neurons coding for the "to-be-grouped" features enhance their firing rates* above other neurons representing background objects

![[roelfsema_neuron_2023_BBRE.png]]

## Grouping features
---

- When we see a scene (e.g. a zebra and a lion), we need to group and associate he features belonging to each object of the scene
- Both #BBS and #BBRE propose that there's an _incremental grouping_ that consists in tagging each feature on whether it belongs to the zebra or the lion
- Work on Artificial Neural Networks proposed that a *Feed-forward pass decomposes the features from low level features like basic shapes to more abstract features*. Then, a *Feed-back pass put labels to specific object categories* 

## Open questions
---

> [!WARNING]
> $Sync_{\gamma}$ = weak and $Sync_{LowFreq}$ = unrelated to binding. **What about #CFC with low-frequencies regulating distributed gamma computations?**



## Reference
---
Roelfsema, P.R. (2023). Solving the binding problem: Assemblies form when neurons enhance their firing rate—they don’t need to oscillate or synchronize. Neuron _111_, 1003–1019. [10.1016/j.neuron.2023.03.016](https://doi.org/10.1016/j.neuron.2023.03.016).