---
title: Dynamic ensemble bayesian filter for robust control of a human brain-machine
  interface
authors:
- Yu Qi
- admin
- Kedi Xu
- Feixiao Ren
- Hongjie Jiang
- Junming Zhu
- Jianmin Zhang
- Gang Pan
- Yueming Wang
date: '2022-06-13'
publishDate: '2025-05-20T09:55:05.146696Z'
publication_types:
- article-journal
publication: '*IEEE Transactions on Biomedical Engineering*'
publication_short: 'TBME'

abstract: 'Objective: Brain-machine interfaces (BMIs) aim to provide direct brain
   control of devices such as prostheses and computer cursors, which have
   demonstrated great potential for motor restoration. One major limitation
   of current BMIs lies in the unstable performance due to the variability
   of neural signals, especially in online control, which seriously hinders
   the clinical availability of BMIs. Method: We propose a dynamic ensemble
   Bayesian filter (DyEnsemble) to deal with the neural variability in
   online BMI control. Unlike most existing approaches using fixed models,
   DyEnsemble learns a pool of models that contains diverse abilities in
   describing the neural functions. In each time slot, it dynamically
   weights and assembles the models according to the neural signals in a
   Bayesian framework. In this way, DyEnsemble copes with variability in
   signals and improves the robustness of online control. Results: Online
   BMI experiments with a human participant demonstrate that, compared with
   the velocity Kalman filter, DyEnsemble significantly improves the
   control accuracy (increases the success rate by 13.9\% in the random
   target pursuit task) and robustness (performs more stably over different
   experiment days). Conclusion: Experimental results demonstrate the
   superiority of DyEnsemble in online BMI control. Significance:
   DyEnsemble frames a novel and flexible dynamic decoding framework for
   robust BMIs, beneficial to various neural decoding applications.'


# Summary. An optional shortened abstract.
summary: IEEE Trans on Biomedical Engineering | A dynamic ensemble Bayesian filter (DyEnsemble) is proposed to improve the robustness of online brain-machine interface (BMI) control by adaptively combining multiple neural decoding models to handle neural signal variability, showing significantly better accuracy and stability than conventional methods.

tags:
  - Brain-Computer Interface
  - Decoding Algorithm
  - Cursor Control

featured: true


# Custom links (uncomment lines below)
links:
- name: Paper
  url: https://ieeexplore.ieee.org/document/9795216


url_pdf: ''
url_code: 'https://zenodo.org/records/14865736'
url_dataset: ''
url_poster: 'https://github.com/SandwichSauce/academic-website/tree/main/content/publication/2022-tbme-dynamic/2022-tbme-dynamic-poster.pdf'
url_project: ''
url_slides: 'https://github.com/SandwichSauce/academic-website/tree/main/content/publication/2022-tbme-dynamic/2022-tbme-dynamic-slides.pdf'
url_source: ''
url_video: 'https://github.com/SandwichSauce/academic-website/tree/main/content/publication/2022-tbme-dynamic/2022-tbme-dynamic-video.mp4'



---

🔶 Brain-Machine Interfaces (BMIs): Challenges and a Dynamic Decoding Solution 🔶

---

## 🚀 Motivation: Restoring Mobility with BMIs

- BMIs have shown great promise for **restoring mobility** in **paralyzed individuals** (e.g., spinal cord injury).
- Intracortical microelectrodes in **motor cortex (MC)** can record **neural activity**, which is translated into control signals for:
  - 🖱️ Computer cursors  
  - 🤖 Robotic limbs

---

## 💡 Advances in Motor BMIs

### 🔄 Real-Time Brain Control of Movement
- Reaching, grasping, limb motion, and multi-DOF arm control
- Real-time BMI systems have become **increasingly sophisticated**

### 🧮 Importance of Decoding Methods
- Decode neural signals → behavioral parameters → device control
- **Linear decoders** (classical and popular):
  - Population Vector Algorithm
  - Wiener Filter
  - Optimal Linear Estimation (OLE)
  - Kalman Filter  
- **Nonlinear decoders**:
  - Capture complex signal-behavior relationships
  - Often based on **artificial neural networks**
  - Show **superior offline performance**

> ⚠️ **Key Concern**: Offline improvements ≠ Online performance  
> 🧠 Due to user adaptation and neural dynamics, **linear decoders** still dominate **online BMI control**

---

## ⚠️ Key Challenge: Neural Variability

### 📉 Source of Performance Instability
- **Trial-to-trial neural variability** (even for same task)
- **Real-time feedback** in closed-loop systems:
  - User adapts control strategy → alters neural tuning
  - Feedback properties (e.g., cursor speed) influence encoding

### 🧪 Effects
- Misinterpretation of intent  
- Degradation in BMI control performance

### 🧰 Current Mitigation Strategies
- **Dimensionality reduction** (e.g., PCA, FA)
- **Record more neurons** to smooth variability
- **Use larger datasets & complex decoders**

> 🚫 Variability is **still an unsolved issue** in robust online BMI decoding

---

## 🆕 Proposed Solution: **DyEnsemble** — A Dynamic Ensemble Bayesian Filter

### 🎯 Objective:
Robust BMI decoding under **neural variability**

### 🔧 Key Idea:
Learn a **pool of diverse models** and **dynamically assemble** them online to adapt to signal changes.

---

## ⚙️ DyEnsemble Framework

### ✅ Core Innovations:
1. **Dynamic weighting & assembly** of models (Bayesian model averaging)
2. **Diverse model pool** covering functional variability:
   - Linear models
   - Polynomial models
   - Neural networks
3. **Sequential estimation** using particle filtering:
   - Estimate **kinematics** and **model ensemble weights** in time

### 🧠 Dynamic Adaptation:
- For each time slot, adaptively assign weights to models based on:
  - **Likelihood** of current neural observation
- Dynamically select the **best-fit combination** of models

---

## 📊 Experimental Validation

### 👤 Human Closed-Loop BMI Experiments

**Task**: Random target pursuit  
**Comparison baseline**: Velocity Kalman Filter (vKF)

### 🚀 Results:
| Metric                       | DyEnsemble vs vKF      |
|-----------------------------|------------------------|
| ✅ Success rate             | **+13.9%**             |
| 📅 Across experiment days   | **More stable**        |
| ⚙️ Adaptive model weights  | **Track neural changes** |

> 🔍 **Key Insight**: DyEnsemble tracks signal variation and dynamically adjusts decoding strategy → **Higher control accuracy & robustness**

---

## 📌 Conclusion

- Neural variability remains a **major bottleneck** in practical BMI systems
- **DyEnsemble**:
  - Combines **Bayesian filtering** + **model averaging** in a unified framework
  - Offers **robust and adaptive decoding**
  - Demonstrates **superior performance** in human experiments

> 🎯 A promising step toward **clinically viable** and **stable BMI control**

