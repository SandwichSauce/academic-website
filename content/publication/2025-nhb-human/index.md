---
title: Human motor cortex encodes complex handwriting through a sequence of stable
  neural states
authors:
- Yu Qi
- admin
- Xinzhu Xiong
- Xiaomeng Yang
- Nai Ding
- Hemmings Wu
- Kedi Xu
- Junming Zhu
- Jianmin Zhang
- Yueming Wang
author_notes:
- "Equal contribution"
- "Equal contribution"
- "Equal contribution"
- ""
- ""
- ""
- ""
- ""
- ""
- ""

date: '2025-04-02'
publishDate: '2025-05-20T09:55:05.165313Z'
publication_types:
- article-journal
publication: '*Nature Human Behaviour*'
publication_short: 'NHB'

abstract: How the human motor cortex (MC) orchestrates sophisticated sequences of fine movements such as handwriting remains a puzzle. Here we investigate this question through Utah array recordings from human MC during attempted handwriting of Chinese characters (n = 306, each consisting of 6.3 +/- 2.0 strokes). We find that MC activity evolves through a sequence of states corresponding to the writing of stroke fragments during complicated handwriting. The directional tuning curve of MC neurons remains stable within states, but its gain or preferred direction strongly varies across states. By building models that can automatically infer the neural states and implement state-dependent directional tuning, we can significantly better explain the firing pattern of individual neurons and reconstruct recognizable handwriting trajectories with 69\% improvement compared with baseline models. Our findings unveil that skilled and sophisticated movements are encoded through state-specific neural configurations.


# Summary. An optional shortened abstract.
summary: Nat Hum Behav | The human motor cortex encodes complex handwriting by transitioning through neural states, each with distinct directional tuning, enabling accurate reconstruction of written characters.

tags:
  - Neuroscience
  - Motor Cortex
  - Brain-Computer Interface
  - Handwriting



featured: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ''
  focal_point: ""
  preview_only: false


# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- Handwriting

# Custom links (uncomment lines below)
links:
- name: Paper
  url: https://www.nature.com/articles/s41562-025-02157-x


url_pdf: ''
url_code: 'https://zenodo.org/records/14865736'
url_dataset: ''
url_poster: 'https://github.com/SandwichSauce/academic-website/tree/main/content/publication/2025-nhb-human/2025-nhb-human-poster.pdf'
url_project: ''
url_slides: ''
url_source: ''
url_video: 'https://github.com/SandwichSauce/academic-website/tree/main/content/publication/2025-nhb-human/2025-nhb-human-video.mp4'

---

<!-- This work is driven by the results in my [previous paper](/publication/conference-paper/) on LLMs.

{{% callout note %}}
Create your slides in Markdown - click the *Slides* button to check out the example.
{{% /callout %}}

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/). -->

---

🔶 Neural Encoding of Fine Motor Control: A Study on Handwriting 🔶

---

## 🧠 Human Fine Motor Control

Humans excel at controlling **sophisticated fine movements**, such as:
- ✍️ Writing  
- ⌨️ Typing  
- 🎼 Musical performance  

### 🔁 Hierarchical Decomposition of Movements

These complex motor behaviors are often **decomposed into simpler units**:
- **Word** → sequence of **letters**
- **Letter** → sequence of **strokes**
- **Stroke** → complex **movement trajectory**

👉 This decomposition:
- **Reduces complexity**
- **Shortens the time scale** of each movement unit
- **Aligns with neural characteristics** of the **motor cortex (MC)**:
  - Neurons in MC show **simple tuning** to movement features
  - Tuning varies over **long time scales**

> ❓ However, it remains unclear whether **primitive units** exist during fine movements, and how such units are **encoded in the motor cortex**.

---

## ✍️ Handwriting as a Model of Fine Motor Control

Handwriting is a **learned fine motor skill**, developed through **years of practice**.

### 🧪 Experimental Design

- **Neural recording**: Single-unit activity from human **motor cortex (MC)**
- **Technology**: Two **96-channel Utah microelectrode arrays**
- **Recording site**: **Left hand knob area** of the **precentral gyrus**
- **Task**: Attempted **writing of Chinese characters**
  - ➕ Highly complex characters: **> 3500 common characters**
  - 🖋️ Composed of **32 stroke types**

---

## 🔍 Key Findings

### 1. **Stable Neural Tuning States**

- During handwriting, **neuronal directional tuning alternates** between a **few stable states**
- Each state corresponds to the writing of **multiple small fragments** of a character

### 2. **Dynamic Transitions Between States**

- Neuronal tuning **clearly changes across states**
- Suggests **state-based representation** of motor components
- Challenges the assumption of **static tuning during continuous movement**

---

## 🧮 Computational Modeling

### 🔄 State-Based vs. Stable Tuning Models

| Model Type             | Description                                           | Performance Improvement |
|------------------------|-------------------------------------------------------|--------------------------|
| **State-based model**  | Decomposes writing into a **sequence of neural states** | 🔼 +229% spiking activity explanation<br>🔼 +69% handwriting decoding accuracy |
| **Stable tuning model**| Assumes **unchanging neural tuning**                 | 🔽 Lower performance     |

> 🧠 State-based models better capture the **temporal dynamics** of neuronal tuning during fine motor behaviors like handwriting.

---

## ✅ Conclusion

This study demonstrates that:
- **Fine movements**, like handwriting, involve **alternating stable neural tuning states**
- These states encode **modular movement fragments**
- Modeling the writing process as a sequence of tuning states:
  - Enhances our understanding of **motor cortex encoding**
  - Improves decoding accuracy in brain-computer interface applications

