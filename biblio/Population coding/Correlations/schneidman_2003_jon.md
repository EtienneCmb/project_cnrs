# Synergy, Redundancy, and Independence in Population Codes
Schneidman, _JoN_, 2003
#PopulationCode #PopulationCoding #Redundant #Redundancy #RedundantCoding #Synergy #Synergistic #SynergisticCoding #InformationBreakdown #Frites #InformationTheory #Methods 

---

## Highlights
---

> [!INFO]
> - The paper introduces a framework to **how much information is contained in interactions between neurons**. They defined three types of correlation :
> 	1. *Activity independence* = Signal Correlation = information between cells
> 	2. *Conditional independence* = Noise correlation = information between cells given the stimulus
> 	3. *Information independence* = synergy of the cells about the stimulus
> - They give an equivalent in #InformationTheory 
> 

## Results
---

### Definitions

- **Encoding** = conversion from stimulus to neural responses
- **Decoding** = procedure that uses neural spike trains to estimate the original stimulus or make a behavioral decision

### Neural encoding

- #MutualInformation $I(S; R)$ ranges between 0 and the minimum of the entropy of the stimulus *S* or the response *R* $\Leftrightarrow$ $I(S; R) \in [0; min(H(S), H(R))]$ 
	- $I = 0$ if no correlation between S and R
	- $I = H(S)$ when each stimulus generates a unique neuronal response
	- $I = H(R)$ when there's no noise
- #MutualInformation appealing because 1) general measure of correlation, 2) no assumption and 3) **as signal flow through the system, information can be lost be is never gained** 

### Population encoding

- For $R_{1}, R_{2}, S$ the neuronal response of two neurons and the stimulus, we can define three types of independence :
	1. **Activity independence** ( #SignalCorrelation ) = information between cells = $I(R_{1}; R_{2}) / min[H(R_{1}), H(R_{2})]$
	2. **Conditional independence** = correlation in a population can occur due to two things *(i)* they behave the same for a given stimulus (aka #SignalCorrelation ) and *(ii)* shared source of noise or shared input like presynaptic neurons projecting to both neurons ( #NoiseCorrelation  = $I(R_{1}; R_{2} | S) / min[H(R_{1}|S), H(R_{2}|S)]$)
	3. **Information independence** = if cells are sensitive to different features of the stimulus, then : $I(S; R_{1}, R_{2}) = I(S; R_{1}) + I(S; R_{2})$ $\Leftrightarrow$ $I(S; R_{1}, R_{2}) - I(S; R_{1}) - I(S; R_{2}) = 0$
		- IRL, the difference is rarely equal to zero. Then, we can define the #Synergy = $Syn(R_{1}, R_{2}) = I(S; R_{1}, R_{2}) - I(S; R_{1}) - I(S; R_{2})$. If it's positive, there's more information in the joint ( #Synergy ). If it's negative, there's redundant information
		- The #Synergy can also be normalized :  $Syn(R_{1}, R_{2}) / I(S; R_{1}, R_{2})$


![[schneidman.png]]

## Reference
---
Schneidman, E., Bialek, W., and Berry, M.J. (2003). Synergy, Redundancy, and Independence in Population Codes. J. Neurosci. _23_, 11539–11553. [10.1523/JNEUROSCI.23-37-11539.2003](https://doi.org/10.1523/JNEUROSCI.23-37-11539.2003).