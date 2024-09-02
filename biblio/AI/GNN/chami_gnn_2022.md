---
tags:
  - AI
  - GNN
  - Review
  - Transductive
  - Inductive
Title: "Machine Learning on Graphs: A Model and Comprehensive Taxonomy."
Authors: Chami, I., Abu-El-Haija, S. & Perozzi, B.
Journal: Journal of Machine Learning Research
Year: "2022"
---
 
# Machine Learning on Graphs: A Model and Comprehensive Taxonomy.

---

## Subdivisions of Graph Representation Learning (GRL)
---



> [!tip] Ultimate goal
> - **Learn Embeddings** = low-dimensional continuous vector representations of graph-structured data ( $\approx$ dimensionality reduction)
> 	-  *Positional Embeddings* : the low-dimensional space keeps track of the global relative position of the nodes in the graph (i.e. preserve distances) (examples : random walk, matrix factorization). Mostly used for unsupervised tasks like link prediction or clustering.
> 	- *Structural Embeddings :* learn local structural information about nodes. Cluster of nodes with similar features in the network should have similar embeddings. Mainly used for classification tasks (nodes or graph classification)

### Classes of GRL

- **Unsupervised GRL :** learn a low-dimensional Euclidian representation that preserves the structure of an input graph (like node to node distance). Inputs are _graph structure's_
- **Supervised GRL :** low-dimensional Euclidian representation that is then used for node, edge and graph classification. Inputs are *nodes features* (i.e. signals on nodes)

### Types of learning

- **Inductive :** train model on training data $\Rightarrow$ extract general rules $\Rightarrow$ predict unlabeled data. This type of learning is able to generalize
	- *Example :* once trained on a graph, it can be used to classify new graphs
- **Transductive :** train model on all (labeled and unlabeled data) $\Rightarrow$ try to predict unlabeled data
	- *Example :* once trained on a graph, it can predict new links (friendship between people of a social network). But can't generalize to new nodes.

[Source](https://www.quora.com/What-is-the-difference-between-inductive-and-transductive-learning)

### Taxonomy of Graph Embedding Models

![[Pasted image 20231016132412.png]]
_Encoder-Decoder model to summarize all the existing GNN. Z is the embedding. Upper branch for classification and lower branch tries to fit the weights to match input adjency matrix_

Graph encoder network $\Rightarrow$ graph decoder network $\Rightarrow$ classification network

## Graph representation learning methods
---

![[Pasted image 20231016153111.png]]
### Unsupervised Graph Embedding

#### Shallow embedding methods

> [!success] Definition
> $$
> 	Z = ENC(\Theta^{E})
> $$


- Learns structure in the data
- Similar to dimensionality reduction method like PCA but support non-linear inputs
- Subdivided into _distance-based_ that measures dissimilarities using measures of distances (embeddings stays closed to the input graph in terms of distance) and _product-based_ which measure similarities
#### Auto-encoding methods

> [!success] Definition
> $$
> 	Z = ENC(W; \Theta^{E})
> $$


- Incorporates adjacency matrix
- he models are trained by minimizing a reconstruction error 
#### Graph neural networks

> [!success] Definition
> $$
> 	Z = ENC(X, W; \Theta^{E})
> $$

### Supervised Graph Embedding
#### Shallow embedding methods
- Similar to the unsupervised shallow embedding methods, with a decoding step to allow predictions on nodes or graph
#### Graph regularization methods

> [!success] Definition
> $$
> 	Z = ENC(X, \Theta^{E})
> $$

- Similar to shallow embedding methods, except that the embedding is learned from the node's features
#### Graph neural networks

## Reference
---
Chami, I., Abu-El-Haija, S. & Perozzi, B. Machine Learning on Graphs: A Model and Comprehensive Taxonomy.