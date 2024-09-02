---
tags:
  - Video
  - GNN
  - Tutorial
  - RNN
  - DeepNet
Title: Understanding Graph Neural Networks
Authors: DeepFindr
Link: https://youtu.be/fOctJB4kVlM?si=KUdjgk0Tkf8ku3om
Year: "2020"
---
# Understanding Graph Neural Networks

---


> [!success] Definition
> The goal of a #GNN is to learn embeddings by combining the information of nodes and neighbors

## Message passing layers
---

> [!tip] Highlights
> - Collect information and update node state using neighbors states
> - This requires an _aggregate_ function (mean, max, neural net, RNN)
> - The larger the number of message passing layers, the more each node will incorporate information provided by distant nodes

![[Pasted image 20231018114053.png]]

- **Step 1** : node yellow collects information about blue neighbor nodes. Then yellow node's state is updated by incorporating neighbor's states. Similarly, node 4 collect information from green node 5
- **Step 2** : node yellow continues to collect information about node surrounding nodes except that now, it will have access to some of the information coming from the green node
- **And so on**

### Aggregate and update

![[Pasted image 20231018114539.png]]

State of a node $u$ at $k + 1$ us _updated_ by considering it's own state ($h_{u}^{(k)}$) and the *aggregated* information collected from neighbors.   

![[Pasted image 20231018114919.png]]
## Reference
---
- [[https://youtu.be/fOctJB4kVlM?si=KUdjgk0Tkf8ku3om|Part 1]] : Introduction
- [[https://www.youtube.com/watch?v=ABCGCf8cJOE|Part 2]] : GNN and it's variants
- [[https://www.youtube.com/watch?v=0YLZXjMHA-8|Part 3]] : PyTorch application