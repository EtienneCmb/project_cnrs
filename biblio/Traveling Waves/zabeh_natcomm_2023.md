---
tags:
  - TravelingWaves
  - Monkey
  - LFP
  - Beta
  - Reward
  - ReinfocementLearning
  - TW
  - GithubCode
---
# Beta traveling waves in monkey frontal and parietal areas encode recent reward history
Zabeh, _Nature communications_, 2023

---

## Highlights
---

> [!INFO]
> - Presence of beta #TW in the frontal and parietal cortex
> - #TW strength correlates with monkey's behavior: stronger #TW when the reward was expected than when it wasn't


## Method
---

#GithubCode : https://github.com/erfanzabeh/WaveMonk
### Estimation of the TW

- Filter the data in a particular frequency band
- Compute Hilbert transform to extract phase information
- Try to explain the phases by fitting a regression using $(x, y)$ positions of the electrodes : $\phi(x, y, t) = k_{x}x + k_{y}y + \phi_{ref}(t)$
- This fitting leads to **the direction of the plane that best describes the propagation** of the #TW in the $(x, y)$ axes
### Consistency of the TW

- **Phase Gradient Directionality :** pearson corelation between the phase of the #TW (at each time point) and the predicted phase from the best fitting planar wave model 
- Not 100% sure, but I guess it's like the distance from the plane if all vectors were perfectly aligned?

## Reference
---

Zabeh, E., Foley, N. C., Jacobs, J. & Gottlieb, J. P. Beta traveling waves in monkey frontal and parietal areas encode recent reward history. _Nat Commun_ **14**, 5428 (2023).