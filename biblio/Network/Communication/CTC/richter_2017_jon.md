# Top-down beta enhances bottom-up gamma
Richter et al. 2017, JoN
#FarCondition #Fries #CTC #Coherence #Jackknife

---

## Highlights

> [[@richter2017top]] : Cross-frequency correlation between top-down (TD) $7a \rightarrow V1$ GC in the beta band and bottom-up (BU) $V1 \rightarrow V4$ in the gamma band

## Description


- The two monkeys are implanted in the left hemisphere.
- The task is the [[far_close_task#Far condition]] where the two stimuli are presented on opposite sides of the screen. Stimulus presented on the top-left corner refers to the _attend-contra_ condition and the stimulus presented in the bottom-right corner to the _attend-ipsi_ condition
- They retrieved the results of [[bastos_2015_neuron]] with the top-down $7a \rightarrow V1$ GC in the beta band and bottom-up (BU) $V1 \rightarrow V4$ in the gamma band
- They then asked the question whether the TD and BU GC, occurring in different frequency bands where correlated. To this end, they used a Jackknife correlation (see after). They found that the stronger $V1 \rightarrow V4_{\gamma}$ the stronger $7a \rightarrow V1_{\beta}$ and conversely
- They then looked at whether the $GC_{\beta}$ was driving the $GC_{\gamma}$ or if it was in the opposite direction. They found that indeed, it's the top-down GC that is preceding the bottom-up GC by 100ms

![[richter_jon.png]]
_(A) GC for $7a \rightarrow V1$ in the $\beta$ band increases for the trials where GC $V1 \rightarrow V4$ is strong in the gamma band (and conversely for the right panel) (B) Correlation between the two GC, either per bin or across all epochs_

## Method

### Jackknife approach

> **Jackknife approach :** Every across-trials methods (e.g. transfer entropy, coherence etc.) are nice because they a a nice SNR however, this prevent for further post-hoc across-trials analysis. The idea here is to compute the across-trials metric by ignoring each individual trial and see the influence of each individual trials. After that, it becomes possible to bin the metric according to the influence of individual trials (e.g. median split)

