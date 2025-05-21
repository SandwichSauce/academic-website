---
title: Tracking functional changes in nonstationary signals with evolutionary ensemble bayesian model for robust neural decoding
authors:
- admin
- Yu Qi
- Gang Pan
- Yueming Wang
date: '2022-12-06'
publishDate: '2025-05-20T09:55:05.152930Z'
publication_types:
- paper-conference
publication: '*Advances in Neural Information Processing Systems*'
publication_short: 'NeurIPS'


abstract: Neural signals are typical nonstationary data where the functional mapping between neural activities and the intentions (such as the velocity of movements) can occasionally change. Existing studies mostly use a fixed neural decoder, thus suffering from an unstable performance given neural functional changes. We propose a novel evolutionary ensemble framework (EvoEnsemble) to dynamically cope with changes in neural signals by evolving the decoder model accordingly. EvoEnsemble integrates evolutionary computation algorithms in a Bayesian framework where the fitness of models can be sequentially computed with their likelihoods according to the incoming data at each time slot, which enables online tracking of time-varying functions. Two strategies of evolve-at-changes and history-model-archive are designed to further improve efficiency and stability. Experiments with simulations and neural signals demonstrate that EvoEnsemble can track the changes in functions effectively thus improving the accuracy and robustness of neural decoding. The improvement is most significant in neural signals with functional changes.


# Summary. An optional shortened abstract.
summary: NeurIPS | A novel evolutionary ensemble framework, EvoEnsemble, dynamically adapts to changes in neural signals by evolving decoders over time, significantly improving the accuracy and robustness of neural decoding in nonstationary conditions.

tags:
  - Decoding Algorithm
  - Nonstationary Signals
  - Brain-Computer Interface
  - Cursor Control

featured: true


# Custom links (uncomment lines below)
links:
- name: Paper
  url: https://openreview.net/forum?id=7fU8UPo875w


url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: 'https://github.com/SandwichSauce/academic-website/tree/main/content/publication/2022-neurips-tracking/2022-neurips-tracking-poster.pdf'
url_project: ''
url_slides: 'https://github.com/SandwichSauce/academic-website/tree/main/content/publication/2022-neurips-tracking/2022-neurips-tracking-slides.pdf'
url_source: ''
url_video: 'https://slideslive.com/38991263/tracking-functional-changes-in-nonstationary-signals-with-evolutionary-ensemble-bayesian-model-for-robust-neural-decoding?ref=speaker-113554'




---

Nonstationary signals widely exist in the real world, where the properties and functions can change continuously over time. Neural signals are typical nonstationary signals, where the inherent dynamics in the neural systems, the plasticity of synapses driven by learning and adaptation contribute to the variability of neural encoding of the brain. The nonstationary property of neural signals forms a challenging problem in the brain-computer interfaces (BCIs) field, because the decoding accuracy will degrade over time given changing neural functions and a fixed neural decoder.

Considering the nonstationary of neural signals, the neural encoding model can be presented by:  
**yt = ht(xt) + qt, (1)**  
where *yt* denotes the neural signal we observed at time *t*, the function *ht(·)* is the neural encoding model that changes over time, and *xt* denotes the state to be encoded such as the velocity of a computer cursor, and *qt* is biological or external noises. Typical neural decoders such as OLE and Kalman filters (KF) mostly assume a stationary *ht(·)*, namely *ht(·) ≡ h0(·)*, *(t = 1, 2, 3, ...)*, which can be oversimplified especially for online BCI systems. Recent studies showed that, in online BCI control, neural encoding functions change significantly with the influence of real-time feedback such as the speed of the cursor and errors in control. The functional changes in neural encoding frequently occur over time, even in a single target reaching trial.

**How to cope with the functional changes in the neural system?**  
Ideally, a neural decoder should be capable of adjusting itself along with changes in neural signals. To this end, there are two main types of solutions. The first one is **re-calibration** of neural decoders periodically or manually when the performance degrades to maintain the control accuracy. Brandman et al. proposed a framework for rapid calibration, which removed the traditional open-loop calibration phase and reduced the original 2–5 min calibration interval to 2–5 s with Bayesian parameter updating. However, such a training process can still disturb the BCI users and usually cannot cope with changes in the short term such as single trials.  

Another way is to design an **adaptive or dynamic model**. Wang et al. proposed a framework that used dual state-space models to estimate both kinematics and neural tuning functions. However, this method does not directly model the neural variability. Qi et al. proposed a novel dynamic ensemble Bayesian filter (DyEnsemble) which obtained the state-of-the-art performance with nonstationary neural signals. DyEnsemble constructs a pool of encoding models, and adaptively assembles a decoder from these models online according to neural signals with a recursive Bayesian filter, which allows the neural decoder to adjust its functions to cope with the changes in neural signals. However, DyEnsemble employs a static model pool, only addressing neural changes in a certain range. The ability can be limited given continuous functional changes in long-term neural recordings.

Regarding the encoding changes in neural signals as a **functional tracking problem**, we propose an **evolutionary ensemble Bayesian filter (EvoEnsemble)** to track the neural encoding functions over time by incorporating evolutionary computation in a recursive Bayesian framework. Specifically, EvoEnsemble maintains a population (i.e., a set of candidate functions) to estimate the neural functions, where the changing fitness of the population is dynamically computed by the likelihood given neural signals (observation) over time. In this way, the population evolution can be driven by the changes in neural signals. Meanwhile, the time-varying functions can be tracked by the posterior distribution of the candidate functions with Bayesian model averaging rules.

### The main contributions of this study can be summarized as follows:
1. We propose a new framework that extends evolutionary computation in a Bayesian process to achieve robust state estimation with neural functional changes;
2. We propose a particle-based solution to simultaneously track the functional changes and estimate the state (e.g., the velocity of a cursor) sequentially online;
3. Two strategies of **evolve-at-changes** and **history-model-archive** are proposed to improve the computational efficiency and estimation stability.

**Experiments with simulations and neural signals demonstrate** the superiority of EvoEnsemble against traditional decoders such as Kalman filters, and the improvement is most significant with functional changes in neural signals.
