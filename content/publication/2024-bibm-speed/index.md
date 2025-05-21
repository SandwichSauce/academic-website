---
title: Speed-enhanced Subdomain Alignment for Long-term Stable Neural Decoding in
  Brain-computer Interfaces
authors:
- Jiyu Wei
- Dazhong Rong
- admin
- Qinming He
- Yueming Wang
date: '2024-01-01'
publishDate: '2025-05-20T09:55:05.159083Z'
publication_types:
- paper-conference
publication: '*2024 IEEE International Conference on Bioinformatics and Biomedicine*'


publication_short: 'BIBM'

abstract: Brain-computer interfaces (BCIs) offer a means to convert neural signals into control signals, providing a potential restoration of movement for people with paralysis. Despite their promise, BCIs face a significant challenge in maintaining decoding accuracy over time due to neural nonstationarities. While current recalibration techniques address this issue to a degree, they either fail to adequately exploit the limited labeled data, fail to perform conditional alignment in regression tasks, or overlook the signal correlation between data from two days. This paper proposes a novel Speed-enhanced Subdomain Alignment (SeSA) framework, integrating semi-supervised learning with domain adaptation techniques in regressive neural decoding. Specifically, SeSA carries out two alignments (i.e., global alignment and conditional speed alignment) to achieve recalibration. Our comprehensive set of experiments, both qualitative and quantitative, substantiate the superior recalibration performance and robustness of our proposed SeSA.


# Summary. An optional shortened abstract.
summary: BIBM | This paper proposes SeSA, a semi-supervised domain adaptation framework that improves BCI recalibration by aligning both global and speed-specific neural features, achieving robust decoding across days despite neural nonstationarities.

tags:
  - Decoding Algorithm
  - Domain Adaptation
  - Brain-Computer Interface

featured: false


# Custom links (uncomment lines below)
links:
- name: Paper
  url: https://ieeexplore.ieee.org/document/10822151


url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

---

---

🔶 Recalibration of Neural Decoders in Brain-Computer Interfaces: The SSAR Framework 🔶

---

## 1. 🔍 Background and Motivation

**Brain-computer interfaces (BCIs)** enable communication between neural activity and external devices by **decoding neural signals into intentional commands**.

BCIs show great potential in:
- Restoration
- Rehabilitation
- Assistive technologies for individuals with disabilities

### 💡 Advancements

- Various **neural decoding algorithms** have achieved impressive accuracy:
  - Population Vector (PV)
  - Kalman Filter
  - KRSRL
  - DyEnsemble
  - EvoEnsemble
- Evolution in **neuron population recording** enables more complex interactions with the external world

### ⚠️ Core Challenge: Neural Signal Variability

Despite advancements, BCIs face a persistent challenge:  
**Neural signal instability over time**, caused by:
- Electrode drift
- Neuronal turnover
- Synaptic plasticity

This results in:
- **Unstable decoding performance**
- **Limited long-term usability** of BCIs

---

## 2. 🛠️ Existing Recalibration Strategies

### ✅ Supervised Recalibration
- Common approach: **daily retraining** of decoders
- Limitation: high cost of **labeled data acquisition** in real-world settings

### ✅ Semi-Supervised Learning (SSL)
- Introduced to reduce labeling effort
- **Limitation**: rarely leverages **historical data**, missing cross-day patterns

### ✅ Unsupervised Domain Adaptation (UDA)
- Techniques: CCA, ADAN, CycleGAN, WDGRL, DA-DCF
- **Limitation**:
  - Ignores available **few labeled data**
  - Fails to achieve **optimal performance**

---

## 3. ⚡ Opportunity: Semi-Supervised Domain Adaptation (SSDA)

SSDA has recently gained attention due to its **low-cost and high-performance** characteristics.

### 🧱 Limitation in BCI Applications
- Most SSDA methods are for **classification tasks**
- **Not suitable** for **regression-based neural decoding**
- **Currently, no SSDA-based method** exists for BCI recalibration

---

## 4. 🧪 Observations from Neural Signal Patterns

To better understand neural signal changes across days, we conducted **preliminary experiments** based on:
- Speed
- Direction of ground-truth velocity

### 🧭 Key Findings

- Ideal feature distributions should be:
  - **Radial in shape**
  - Consistent between **features and labels**
- **Cross-day decoding results**:
  - **Direction decoding**: relatively stable
  - **Speed decoding**: significant deviation

### 🔄 Implications for UDA
- UDA methods using **global alignment** correct direction shifts reasonably well
- But **fail to handle speed drift**, as similar-speed samples may be **far apart** in feature space
- Existing **conditional alignment methods** are classification-specific and **not compatible** with regression tasks

---

## 5. 🚀 Proposed Framework: SSAR

We propose three **key factors** for effective regression-based BCI recalibration:
1. 🌐 **Global alignment**
2. ⚙️ **Conditional speed alignment**
3. 🔗 **Feature-label consistency**

### 🧠 SSAR: Speed-Enhanced Subdomain Adaptation Regression

A novel framework that integrates **domain adaptation** and **semi-supervised learning** for **regression tasks**.

#### 🧩 Core Components

- **Speed-enhanced Subdomain Alignment (SeSA)**  
  - Performs both **global** and **conditional speed alignment**  
  - Aligns data points with **similar labels**

- **Contrastive Consistency Constraint (CCC)**  
  - Enhances SeSA using **contrastive learning**  
  - Enforces **consistency between features and labels**

---

## 6. 🎯 Contributions

- 🔍 **Empirical Insight**:  
  We reveal that lacking **conditional speed alignment** limits UDA performance, and propose **three key factors** for effective recalibration.

- 🧠 **Novel Method**:  
  We introduce **SSAR**, the **first framework** combining **semi-supervised learning** and **subdomain adaptation** for **regression-based BCI recalibration**.

- 📊 **State-of-the-Art Results**:  
  Extensive qualitative and quantitative experiments demonstrate that SSAR achieves **superior recalibration performance** compared to existing methods.
