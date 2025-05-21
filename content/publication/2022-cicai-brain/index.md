---
title: A brain-controlled mahjong game with artificial intelligence augmentation
authors:
- Xiaodi Wu
- Yu Qi
- admin
- Kedi Xu
- Junming Zhu
- Jianmin Zhang
- Yueming Wang
date: '2022-08-27'
publishDate: '2025-05-20T09:55:05.125376Z'
publication_types:
- paper-conference
publication: '*CAAI International Conference on Artificial Intelligence*'
publication_short: 'CICAI'

abstract: Brain-computer interface (BCI) provides a direct pathway from the brain
   to external devices, which have demonstrated potential in rehabilitation
   and human-computer interaction. One limitation of current BCI lies in
   the low precision and stability in control, thus the user scenario and
   the interaction process play an important role in BCI applications. We
   propose to leverage the ability of artificial intelligence (AI) to
   improve the easy-of-use of BCIs. We designed a brain-controlled mahjong
   game with AI augmentation. As the user plays the game, an AI system
   continuously monitors the game and suggests several optimal candidate
   options, and the user directly selects from the candidates rather than
   from all the mahjong tiles in hand. This design enables the mahjong game
   with easy control, thus improving the user experience. Our system is
   evaluated by a human subject with an invasive BCI system. Results
   demonstrate that the subject can fluently control the system to play the
   mahjong game.


# Summary. An optional shortened abstract.
summary: CICAI | An AI-augmented brain-computer interface is developed for a mahjong game, enabling easier and more precise control by allowing users to select from AI-suggested options, thus improving usability and user experience in a real BCI application.

tags:
  - Brain-Computer Interface
  - Decoding Algorithm
  - Mahjong Game

featured: true


# Custom links (uncomment lines below)
links:
- name: Paper
  url: https://link.springer.com/chapter/10.1007/978-3-031-20503-3_47


url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: 'https://github.com/SandwichSauce/academic-website/tree/main/content/publication/2022-cicai-brain/2022-cicai-brain-video.mov'


---

Brain-computer interface (BCI) establishes a pathway from the brain to external devices such as computers and neuroprosthetics. Especially, BCI provides a novel way of human-computer interaction, which gives rise to new applications such as BCI typewriters and BCI games.

The challenge of current BCIs lies in the limited bandwidth and low precision in control. In continuous control tasks, the state-of-the-art non-invasive BCIs could mind-control a robotic arm to continuously track and follow a computer cursor. Invasive BCIs demonstrated higher bandwidth compared with non-invasive ones, while the control performance is far behind natural motor controls. Meanwhile, the nonstationary property of neural signals leads to unstable BCI control. With the limitations of BCI systems, the system design and the user interaction process play an important role in leveraging the performance of BCIs. To improve the easy-of-use of BCI systems, efforts have been made. Several studies design special typewriter interfaces to facilitate BCI-based interactions. The Berlin Brain-Computer Interface presents the novel mental typewriter Hex-o-Spell which uses an appealing visualization based on hexagons, and improves the bandwidth of BCI systems. Some approaches design games specifically tailored to the characteristics of direct brain-to-computer interaction. Besides, a few studies involve AI language model to improve performance of BCI communication system.

Inspired by studies mentioned above, this study proposes an artificial intelligence augmentation approach to improve the human-computer interaction with a BCI system. We propose a BCI mahjong game with artificial intelligence assistance to improve the easy-of-use of BCI system. As the user plays the game, an AI system helps suggest optimal candidate options. Instead of directly choosing a tile from the tiles in hand, which usually requires delicate operations, the user can choose from the candidate options. In this way, the difficulty of operation can be highly reduced. A user can play the mahjong game with easy control, such that improves the user experience.