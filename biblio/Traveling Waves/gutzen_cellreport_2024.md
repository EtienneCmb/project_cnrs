---
tags:
  - TravelingWaves
  - Software
  - Toolbox
  - Python
Title: gutzen_cellreport_2024
Authors: Gutzen, R., De Bonis, G., De Luca, C., Pastorelli, E., Capone, C., Allegra Mascaro, A.L., Resta, F., Manasanch, A., Pavone, F.S., Sanchez-Vives, M.V., Mattia, M., Grün, S., Paolucci, P.S., Denker, M.
Journal: Cell Reports
Year: "2024"
---
# A modular and adaptable analysis pipeline to compare slow cerebral rhythms across heterogeneous datasets

---

> [!tip] Highlights
> Cobrawap = toolbox to identify and characterize travelling waves


## Pipeline
---

- **Stage 1 :** formatting input data, save it as nix / npy
- **Stage 2 :** preprocessing (detrending, filtering, normalization etc.)
- **Stage 3 :** trigger time identification. Basically, identify time stamps where the activity move from Down to Up states (and conversely from Up to Down). Use either a fix threshold or Hilbert-phase
- **Stage 4 :** spatio-temporal clustering of trigger time events. The idea is to group the triggers detected at stage 3 into spatio-temporal clusters (called wavefronts). The detection of the clusters is controlled via a parameter `TIME_SPACE_RATIO`
- **Stage 5 :** characterize the waves (i.e. velocity, planarity etc.). This step can either be estimated at the wave-wise level (5a) or channel-wise (5b)

## Reference
---
Gutzen, R., De Bonis, G., De Luca, C., Pastorelli, E., Capone, C., Allegra Mascaro, A.L., Resta, F., Manasanch, A., Pavone, F.S., Sanchez-Vives, M.V., Mattia, M., Grün, S., Paolucci, P.S., Denker, M., 2024. A modular and adaptable analysis pipeline to compare slow cerebral rhythms across heterogeneous datasets. Cell Reports Methods 4, 100681. [https://doi.org/10.1016/j.crmeth.2023.100681](https://doi.org/10.1016/j.crmeth.2023.100681)