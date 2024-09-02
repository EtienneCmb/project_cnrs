# Statistical methods for dissecting interactions between brain areas
Semedo, _Current Opinion in Neurobiology_, 2020
#FC #Interactions #Communication #Statistics #Multivariate

---

<br>

## Highlights
---

> [!INFO]
> - The paper present methods to better understand the interactions between brain areas
> - In particular, they use multivariate regression to try to predict the activity of a target neuron as a linear combination of neurons from the source area
> - The important point raised by authors is that you can better interpret how brain areas interact

<br>

## Description
---

### Problematic

- Most research focused on how areas behave in isolation
- In the end, little is known about how regions are interacting, even with neighboring areas

### Anatomy

- The brain response to identical stimuli might change depending on the context
- Hence, *anatomy is cable, the wiring, but it does not tell us what information is conveyed*

### On the use of multivariate methods

- When used as univariate methods, they can inform us on which areas are communicating
- They can disentangle or elucidate what aspect of activity are related across areas

Let `y` be the activity of a target neuron and $x_{1}, ..., x_{n}$ the activity of `n` neurons. They try to model the target activity of `y` as a linear combination of the `n` source neurons :

$y = \beta_{1}x_{1} + \beta_{2}x_{2} + \beta_{3}x_{3}$

If there are multiple target neurons, one can repeat the fitting of the regression to include each time of a different neuron (as shown below).

The striking point of this method is that it becomes possible to **interpret the "regression space"**. For example, #CommunicationSubspace i.e. a partial proportion of neurons in the source region are interacting with the target region (see #CommunicationSubspace in [[semedo_2019_neuron]]).


![[semedo_curop_2020.png]]

### Pitfalls

- Changes in across-area correlation can either be due to actual changes in the *across-are interaction* or *local modifications*. For example, an independent input to the source region can increase its noise and reduce the connectivity with another region
<br>

## Reference
---
Semedo, J.D., Gokcen, E., Machens, C.K., Kohn, A., Yu, B.M., 2020. Statistical methods for dissecting interactions between brain areas. Current Opinion in Neurobiology 65, 59–69. [https://doi.org/10.1016/j.conb.2020.09.009](https://doi.org/10.1016/j.conb.2020.09.009)