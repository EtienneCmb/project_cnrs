---
tags:
  - GNN
  - Neuroscience
  - Integration
  - Classification
  - MachineLearning
  - ML
  - DeepNet
  - Morphology
  - StructuralConnectivity
  - FunctionalConnectivity
  - FC
  - SC
  - HOI
  - Biomarkers
  - Prediction
Title: Graph Neural Networks in Network Neuroscience
Authors: Bessadok, A., Mahjoub, M. A. & Rekik, I.
Journal: IEEE
Year: "2022"
Link: http://arxiv.org/abs/2106.03535
---
# Graph Neural Networks in Network Neuroscience

---

> [!tip] Highlights
> GNN can be used for three main tasks :
> 1. **Brain graph prediction :** cross-modalities prediction, cross-resolution or cross-time
> 2. **Brain graph integration :** combine the data of all subjects into a single fingerprint graph
> 3. **Brain graph classification :** classify brain states or identify biomarkers

![[Pasted image 20231017211953.png]]
_Description of every possibility for studying rain graph using GNN_

![[Pasted image 20231017212049.png]]
## Brain graph construction
---

> [!tip] Highlights
> Three main types of brain graph
> 1. **Morphological brain graphs:** estimated using cortical measures like sulcal depth, cortical thickness etc. For each ROI, we average the values of the cortical attributes. The graph is obtained by taking the absolute difference between pairs of brain regions
> 2. **Functional brain graph :** #FC 
> 3. **Structural brain graph :** #SC 


## GNN and Neuroscience
---

### Brain graph prediction

> [!tip] Highlights
> The main goal is to train the model on some data ( #Morphology , #FC, #SC etc.) and predict unseen data. Three main prediction types
> 1. **Cross-modality prediction :** try to predict the activity of one modality using another modality ([[Pasted image 20231017212049.png|A-1]] : one-to-one mapping like #SC $\Rightarrow$ #FC ) or predict multiple modalities ([[Pasted image 20231017212049.png|A-2]] : one-to-many). _What about many-to-one?_ 
> 2. **Cross-resolution prediction :** generate predictions to generate higher-resolution brain graph ([[Pasted image 20231017212049.png|B]])
> 3. **Cross-time prediction :** try to predict graph evolution based on unseen time points ([[Pasted image 20231017212049.png|C]]). This can be particularly useful to track disease progress

### Brain graph integration

> [!tip] Highlights
> The main goal is to train the model using uni or multi-modal population recordings to build a graph fingerprint ([[Pasted image 20231017212049.png|C]]). This can be used to then infer the most representative edges or nodes.

### Brain graph classification

> [!tip] Highlights
> As the name suggests, the goal is two perform classification 🤯 and identify most discriminative graphs. Two main types of classification:
> 1. **Brain state classification:** differentiate two conditions (e.g. healthy vs. disordered [[Pasted image 20231017212049.png|F]]). Brain states classification can be performed using three groups :
> 	- _Embedding-based :_ classification using the lower-dimensional embedding
> 	- _Graph-based :_ classification using the full model without passing by the embedding. In this model, each node represents an ROI
> 	- _Population-based :_ same as graph-based except that here, the nodes of the graph are subjects
> 2. **Identification of discriminative biomarkers :** for example, a sub-network might be different between the two populations ([[Pasted image 20231017212049.png|E]])


Brain graph don't learn #HOI $\Rightarrow$ some papers have investigated to replace nodes by simplicial complex

## To check
---

SC & FC : 83
RNN & GNN : 87
Biomarkers : 93, 94, 95
## Reference
---
Bessadok, A., Mahjoub, M. A. & Rekik, I. Graph Neural Networks in Network Neuroscience. Preprint at [http://arxiv.org/abs/2106.03535](http://arxiv.org/abs/2106.03535) (2022).