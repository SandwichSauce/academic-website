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
# Coping with Neural Signal Nonstationarity in Brain-Computer Interfaces: The EvoEnsemble Approach

## 🔄 Background: Nonstationary Neural Signals

- **Nonstationarity** is a common characteristic in real-world signals.
- **Neural signals** are inherently nonstationary due to:
  - Internal neural dynamics
  - Synaptic plasticity driven by **learning** and **adaptation**
- This variability poses a **major challenge** to brain-computer interfaces (BCIs):
  - A fixed decoder may fail as **neural encoding functions evolve**
  - Leads to **degradation in decoding accuracy over time**

---

## 📘 Neural Encoding as a Time-Varying Function

The neural encoding process can be formulated as:

$$
y_t = h_t(x_t) + q_t
$$

Where:
- \( y_t \): observed neural signal at time \( t \)
- \( x_t \): the state to be encoded (e.g., cursor velocity)
- \( h_t(\cdot) \): time-varying neural encoding function
- \( q_t \): noise term (biological or external)

Most traditional decoders (e.g., OLE, Kalman Filter) assume a **stationary** encoding function:

$$
h_t(\cdot) \equiv h_0(\cdot), \quad \forall t \in \{1, 2, 3, \ldots\}
$$

However, in **online BCI systems**, studies have shown that:
- \( h_t(\cdot) \) changes significantly over time
- These changes are influenced by **real-time feedback** (e.g., cursor velocity, control errors)
- Encoding function variability can occur **even within a single trial**

---

## ❓ Challenge: How to Handle Functional Changes?

### 🛠️ 1. Re-calibration-Based Solutions
- Periodic/manual **recalibration** of decoders
- **Brandman et al.**: Fast Bayesian recalibration (2–5s)
  - Eliminates open-loop phase
  - Still **interrupts user experience**
  - **Not responsive** to **short-term** signal changes

### ⚙️ 2. Adaptive/Dynamic Model-Based Solutions

#### a. Dual State-Space Models (Wang et al.)
- Estimate both kinematics and tuning functions
- **Does not directly model neural variability**

#### b. DyEnsemble (Qi et al.)
- **Dynamic ensemble Bayesian filter**
- Maintains a **static model pool**
- Assembles decoder online via **Bayesian filtering**
- Handles **limited nonstationarity**
- Limited under **long-term continuous changes**

---

## 🌱 Proposed Solution: EvoEnsemble

We propose the **Evolutionary Ensemble Bayesian Filter (EvoEnsemble)**, treating neural functional changes as a **functional tracking problem**.

### 🧠 Key Ideas
- Maintains a **population** of candidate functions
- Uses **evolutionary computation** to adapt over time
- Computes fitness via **signal likelihood**
- Tracks time-varying functions using **Bayesian model averaging**

---

## 📌 Main Contributions

1. ✅ **Novel Bayesian-Evolutionary Framework**  
   - Extends evolutionary computation for robust state estimation with neural functional drift

2. 🔁 **Online Functional and State Tracking**  
   - Particle-based method to estimate both neural functions and latent states (e.g., cursor velocity)

3. ⚡ **Efficiency and Stability Strategies**  
   - **Evolve-at-changes**: trigger evolution only when changes are detected  
   - **History-model-archive**: maintain stable models for reuse

---

## 🧪 Experimental Results

- Conducted on **simulations** and **real neural signals**
- EvoEnsemble **outperforms traditional decoders** (e.g., Kalman Filter)
- Shows **significant improvement** especially under **nonstationary conditions**
