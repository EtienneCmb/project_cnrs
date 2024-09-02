---
tags:
  - GNN
  - Review
  - DeepNet
  - MessagePassing
  - GCN
  - GAT
  - GRN
  - RNN
Title: "Graph neural networks: A review of methods and applications"
Authors: Zhou J, Cui G, Hu S, Zhang Z, Yang C, Liu Z, Wang L, Li C, Sun M
Journal: AI Open
Year: "2020"
---

# Graph neural networks: A review of methods and applications

---

> [!tip] Highlights
> - #GNN capture the dependence of graph via #MessagePassing  between the nodes of the graph
> - Three well known variants : Graph Convolutional Network ( #GCN ), Graph Attentional Network ( #GAT ) and Graph Recurrent Network ( #GRN )


## Introduction
---

Categorization of #GNN into four groups :
1. Recurrent GNN ( #GRN )
2. Convolutional GNN ( #GCN )
3. Graph autoencoders
4. Spatial-temporal GNN

## GNN pipelines
---

> [!success] GNN pipeline
> [[zhou_gnn_review_ai_open#1. Graph structure|Graph structure]] $\Rightarrow$ [[zhou_gnn_review_ai_open#2. Graph type and scale|Graph type and scale]] $\Rightarrow$ [[zhou_gnn_review_ai_open#3. Design loss function|Design loss function]] $\Rightarrow$ [[zhou_gnn_review_ai_open#4. Build model|Build model]]

![[Pasted image 20231020162520.png]]
### 1. Graph structure

- *Structural scenario :* implicit structure like molecules,  (e.g. #SC) 
- _Non-structural scenario :_ build the graph from the data (e.g. #FC  )

### 2. Graph type and scale

- Directed / Undirected
- Homogeneous (all #FC ) / Heterogeneous ( #SC and #FC ). Different links but same nodes
- Static / Dynamic

### 3. Design loss function

> The type of the loss function depends on the [[zhou_gnn_review_ai_open#Tasks|task]] and [[zhou_gnn_review_ai_open#Training|training]] settings

#### Tasks

- _Node-level :_ node classification / node regression / node clustering
- _Edge-level :_ link prediction
- _Graph-level :_ graph classification / graph regression / graph matching

#### Training

- _Supervised settings :_ with data labels
- _Semi-supervised settings :_
	- #Transductive : predict label of given unlabeled nodes
	- #Inductive : predict label of not given unlabeled nodes
- _Unsupervised setting_

### 4. Build model

> [[zhou_gnn_review_ai_open#Propagation module|Propagation module]] $\Rightarrow$ [[zhou_gnn_review_ai_open#Sampling module|Sampling module]] $\Rightarrow$ [[zhou_gnn_review_ai_open#Pooling module|Pooling module]]

#### Propagation module

> [!success] Purpose
> Propagate information to neighbor nodes

Propagation can be performed by :
1. Convolution
2. #RNN
3. Skip connection : very deep layers can also propagate noise and perform an over-smoothing. In that case, it might help to skip some connections
#### Sampling module

> [!success] Purpose
> - The more layers $\Rightarrow$ The larger the number of neighbors
> - $\Rightarrow$ Computational explosion
> - $\Rightarrow$ Sampling = sub-selection

- *Node sampling :* subset of each node's neighborhood (e.g. 2-50 neighbors)
- *Layer sampling :* subselect nodes instead of neighbors
- _Subgraph sampling :_ sample multiple subgraph

#### Pooling module

> [!success] Purpose
> - Decompose into small and very specific features
> - Pooling = try to find more generic features that will also help to generalize

- *Direct pooling :* pool information directly from nodes (e.g. max / mean / sum / attention)
- _Hierarchical pooling :_ pool information from nodes by considering hierarchical information
## Reference
---
Zhou J, Cui G, Hu S, Zhang Z, Yang C, Liu Z, Wang L, Li C, Sun M (2020) Graph neural networks: A review of methods and applications. AI Open 1:57–81.
