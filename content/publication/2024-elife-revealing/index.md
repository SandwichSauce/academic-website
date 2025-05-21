---
title: Revealing unexpected complex encoding but simple decoding mechanisms in motor
  cortex via separating behaviorally relevant neural signals
authors:
- Yangang Li
- admin
- Yu Qi
- Yueming Wang
date: '2024-08-09'
publishDate: '2025-05-20T09:55:05.140646Z'
publication_types:
- article-journal
publication: '*eLife*'

publication_short: 'eLife'

abstract: In motor cortex, behaviorally relevant neural responses are entangled
   with irrelevant signals, which complicates the study of encoding and
   decoding mechanisms. It remains unclear whether behaviorally irrelevant
   signals could conceal some critical truth. One solution is to accurately
   separate behaviorally relevant and irrelevant signals at both
   single-neuron and single-trial levels, but this approach remains elusive
   due to the unknown ground truth of behaviorally relevant signals.
   Therefore, we propose a framework to define, extract, and validate
   behaviorally relevant signals. Analyzing separated signals in three
   monkeys performing different reaching tasks, we found neural responses
   previously considered to contain little information actually encode rich
   behavioral information in complex nonlinear ways. These responses are
   critical for neuronal redundancy and reveal movement behaviors occupy a
   higher-dimensional neural space than previously expected. Surprisingly,
   when incorporating often-ignored neural dimensions, behaviorally
   relevant signals can be decoded linearly with comparable performance to
   nonlinear decoding, suggesting linear readout may be performed in motor
   cortex. Our findings prompt that separating behaviorally relevant
   signals may help uncover more hidden cortical mechanisms.


# Summary. An optional shortened abstract.
summary: eLife | A framework is proposed to separate and analyze behaviorally relevant neural signals, revealing that previously overlooked neural responses encode rich information and suggesting that motor behaviors occupy a higher-dimensional space than expected and can be decoded linearly.

tags:
  - Neuroscience
  - Brain-Computer Interface
  - Behaviorally Relevant

featured: true


# Custom links (uncomment lines below)
links:
- name: Paper
  url: https://elifesciences.org/articles/87881#content


url_pdf: ''
url_code: 'https://github.com/eric0li/d-VAE'
url_dataset: ''
url_poster: 'https://github.com/SandwichSauce/academic-website/tree/main/content/publication/2024-elife-revealing/2024-elife-revealing-poster.pdf'
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

---

Understanding how motor cortex encodes and decodes movement behaviors is a fundamental goal of neuroscience (Kriegeskorte and Douglas, 2019; Saxena and Cunningham, 2019). Here, we define behaviors as behavioral variables of interest measured within a given task, such as arm kinematics during a motor control task; we employ terms like ‘behaviorally relevant’ and ‘behaviorally irrelevant’ only regarding such measured behavioral variables. However, achieving this goal faces significant challenges because behaviorally relevant neural responses are entangled with behaviorally irrelevant factors such as responses for other variables of no interest (Fusi et al., 2016; Rigotti et al., 2013) and ongoing noise (Azouz and Gray, 1999; Faisal et al., 2008). Generally, irrelevant signals would hinder the accurate investigation of the relationship between neural activity and movement behaviors. This raises concerns about whether irrelevant signals could conceal some critical facts about neural encoding and decoding mechanisms.

If the answer is yes, a natural question arises: what critical facts about neural encoding and decoding would irrelevant signals conceal? In terms of neural encoding, irrelevant signals may mask some small neural components, making their encoded information difficult to detect (Moreno-Bote et al., 2014), thereby misleading us to neglect the role of these signals, leading to a partial understanding of neural mechanisms. For example, at the single-neuron level, weakly tuned neurons are often assumed to contain little information and not analyzed (Georgopoulos et al., 1986; Hochberg et al., 2012; Wodlinger et al., 2015; Inoue et al., 2018); at the population level, neural signals composed of lower variance principal components (PCs) are typically treated as noise and discarded (Churchland et al., 2012; Gallego et al., 2018; Gallego et al., 2020; Cunningham and Yu, 2014). So, do these ignored signals truly contain little information, or do they appear that way only because they are obscured by irrelevant signals? And what’s the role of these ignored signals? In terms of neural decoding, irrelevant signals would significantly complicate the information readout (Pitkow et al., 2015; Yang et al., 2021), potentially hindering the discovery of the true readout mechanism of behaviorally rele- vant responses. Specifically, in motor cortex, in what form (linear or nonlinear) downstream neurons readout behavioral information is an open question. Current studies typically use noisy raw signals for decoding behavioral information (Georgopoulos et al., 1986; Hochberg et al., 2012; Wodlinger et al., 2015; Glaser et al., 2020; Willsey et al., 2022). The linear readout is biologically plausible and widely used (Georgopoulos et al., 1986; Hochberg et al., 2012; Wodlinger et al., 2015), but recent studies (Glaser et al., 2020; Willsey et al., 2022) demonstrate nonlinear readout outperforms linear readout. So which readout scheme is the motor cortex more likely to adopt for decoding information from behaviorally relevant signals? Whether irrelevant signals are the culprits for the performance gap observed with raw signals? Unfortunately, all the above issues remain unclear.

One approach to address the above issues is to accurately separate behaviorally relevant and irrelevant signals at both single-neuron and single-trial levels and then analyze noise-free behaviorally relevant signals, which enables us to gain a more accurate and comprehensive understanding of the underlying neural mechanisms. However, this approach is hampered by the fact that the ground truth of behaviorally relevant signals is unknown, which makes the definition, extraction, and validation of behaviorally relevant signals a challenging task. As a result, methods of accurate separation remain elusive to date. Existing methods for extracting behaviorally relevant patterns at the single-trial level mainly focus on the latent population level (Sani et al., 2021; Hurwitz, 2021; Zhou, 2020) rather than the single-neuron level, and they extract neural activities based on assumptions about specific neural properties, such as linear or nonlinear dynamics (Sani et al., 2021; Hurwitz, 2021). Although these methods have shown promising results, they fail to capture other parts of behaviorally relevant neural activity that do not meet their assumptions, thereby providing an incomplete picture of behaviorally relevant neural activity. Some studies (Kobak et al., 2016; Rouse and Schieber, 2018) are able to extract behaviorally relevant neural signals at the single-neuron level, but they utilize trial-averaged responses, thereby losing the single-trial information. To overcome these limitations and obtain accu- rate behaviorally relevant signals at both single-neuron and single-trial levels, we propose a novel framework that defines, extracts, and validates behaviorally relevant signals by simultaneously consid- ering such signals’ encoding (behaviorally relevant signals should be similar to raw signals to preserve the underlying neuronal properties) and decoding (behaviorally relevant signals should contain behav- ioral information as much as possible) properties (see Methods and Figure 1). This framework estab- lishes a prerequisite foundation for the subsequent detailed analysis of neural mechanisms.

Here, we conducted experiments using datasets recorded from the motor cortex of three monkeys performing different reaching tasks, where the behavioral variable is movement kinematics. After signal separation by our approach, we first explored how the presence of behaviorally irrelevant signals affects the analysis of neural activity. We found that behaviorally irrelevant signals account for a large amount of trial-to-trial neuronal variability, and are evenly distributed across the neural dimensions of behaviorally relevant signals. Then, we explored whether irrelevant signals conceal some facts of neural encoding and decoding. For neural encoding, irrelevant signals obscure the behavioral infor- mation encoded by neural responses, especially for neural responses with a large degree of nonlin- earity. Surprisingly, neural responses that are usually ignored (weakly tuned neurons and neural signals composed of small variance PCs) actually encode rich behavioral information in complex nonlinear ways. These responses underpin an unprecedented neuronal redundancy and reveal that movement behaviors are distributed in a higher-dimensional neural space than previously thought. In addition, we found that the integration of smaller and larger variance PCs results in a synergistic effect, allowing the smaller variance PC signals that cannot be linearly decoded to significantly enhance the linear decoding performance, particularly for finer speed control. This finding suggests that lower variance PC signals are involved in regulating precise motor control. For neural decoding, irrelevant signals complicate information readout. Strikingly, when uncovering small neural components obscured by irrelevant signals, linear decoders can achieve comparable decoding performance with nonlinear decoders, providing strong evidence for the presence of linear readout in motor cortex. Together, our findings reveal unexpected complex encoding but simple decoding mechanisms in the motor cortex. Finally, our study also has implications for developing accurate and robust brain-machine interfaces (BMIs) and, more generally, provides a powerful framework for separating behaviorally relevant and irrelevant signals, which can be applied to other cortical data to uncover more neural mechanisms masked by behaviorally irrelevant signals.