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


Humans are superb at controlling sophisticated fine movements, such as writing, typing, and musical performance. These sophisticated motoric behaviors are often decomposed into a sequence of simpler movements. For example, a word is decomposed into a sequence of letters, a letter can be further decomposed into strokes, and even a stroke may involve a complex movement trajectory. Such decomposition can reduce the complexity and shorten the time scale of each movement unit, which is of particular importance for the motor cortex (MC), since neurons in the MC generally show relatively simple tuning to movement features, and the tuning varies over relatively long time scales. It remains unclear, however, if primitive units exist during fine movement and how such units may be encoded in the MC. 

Handwriting, a skill developed through years of deliberate practice, serves as an example of sophisticated fine motor control in humans. This study investigated the neural basis of handwriting by recording single-unit neural activity from human MC with two 96-channel Utah microelectrode arrays in the left hand knob area of the precentral gyrus. We studied attempted writing of Chinese characters, which are highly complex (> 3500 frequent characters composed by 32 types of strokes) and pose a great challenge for motor control. We identified that, during the writing of a character, the directional tuning of neurons alternates among a few stable states, each encoding the writing of multiple different small fragments of a character. Furthermore, the neuronal tuning during handwriting clearly changes across states. Computational models that decompose the writing process into a sequence of states better explain spiking activity from individual neurons (229% change) and better decode the handwriting based on the neural population (69% change, Fig. 1h), compared to a model that assumes stable neuronal tuning throughout the writing of a Chinese character.
