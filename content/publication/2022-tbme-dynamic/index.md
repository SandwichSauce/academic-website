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

In recent decades, brain-machine interfaces (BMIs) have demonstrated great potential for restoring mobility for humans paralyzed by trauma to the neural system, such as spinal cord injuries. Neural activities, recorded intracortically by microelectrodes placed on the motor cortex, could be translated into control signals for external assistive devices, such as computer cursors and robotic limbs.

Recent advances in BMIs have demonstrated the potential for high-performance communication and control. Much effort has been made to establish real-time motor BMIs to link brain and prosthetic limbs, including studies on the brain control of arms and hands for reaching and grasping, the motion of upper and lower limbs, and the degrees of freedom for arm movements. Decoding methods, the mathematical models transforming neuronal signals to behavioral parameters to control external devices, play an important role in BMI. Since Georgopoulos proposed the classical population encoding mechanism, linear decoders have been leading the translation of neural activity into movements, including Wiener filter, population vector algorithm, optimal linear estimation (OLE), and Kalman filter. Nonlinear decoders, which are capable of capturing more complex relationships and noise robustly, obtained superior decoding performance in the offline analysis. There is also evidence that nonlinear methods, especially those involving artificial neural networks, demonstrated higher performance in certain motion tasks, compared with their linear counterparts. Nevertheless, studies suggested that it is not necessarily true that improvements in offline reconstruction will translate to improvements in online control, considering the participant’s learning and compensation abilities. Therefore, although nonlinear models might construct more powerful decoders, linear decoders such as OLE and Kalman filter are still the most popular choice for online control.

One critical barrier to clinical available BMI applications is the unstable performance due to the variability in neural signals. That is, individual neurons can exhibit significant variability in firing properties across different trials in a motor task. In closed-loop BMI control, the variability of neural signals can be even more complicated with the influence of real-time feedback. Because a user will update the control strategy when the output of the decoder does not match the intent, i.e., the user’s adaptation to the decoder, which can apparently change neuronal tuning. Besides, different conditions of neural feedback (e.g., the speed of the cursor) can induce variability in neural response and encoding. If the variability is not properly addressed, it may lead to mistakes in intention interpretation, thus seriously hindering the availability of BMI systems. To improve the robustness of neural decod- ing, some studies transform the original neural activities to a lower-dimensional space using dimension reduction methods such as principal component analysis or factor analysis, where the effect of variability can be suppressed. Other ways to deal with the variability include recording more neurons to mitigate the non-stationarity of single neurons, or using larger datasets and more complex decoders (usually nonlinear) to improve the robustness against variability. However, the unstable performance brought by neural variability is still a challenging problem that has not been well addressed.

This study focuses on the variability of neural encoding associated with brain states in closed-loop BMIs, which leads to shifts in the functional relationship between neural signals and kinematics. To deal with the neural vari- ability, this study proposes a dynamic ensemble Bayesian filter (DyEnsemble) for robust BMI control. Unlike classical Bayesian filters which use fixed models, DyEnsemble learns a pool of models that contains diverse abilities of describing the neural encoding functions in different time slots. Then in each time slot, it seeks a proper ensemble model by dynamically weighting and assembling the models in the pool according to the neural signals. In this way, it improves the robustness against the variability. To dynamically assemble a neural decoder along with signals, there are three main issues to address: 1) how to dynamically weight and assemble models in an online process; 2) how to construct the model pool to cover the variability in neural signals; 3) how to sequentially estimate the kinematic intentions with the DyEnsemble model. For 1), we propose to adaptively tune the weights of models by how much the observation neural signals support each model (i.e., the like- lihood of the model), and assemble the models according to the Bayesian model averaging algorithm. For 2), we construct multiple models of linear, polynomial, and neural networks to cover the functional variability in neural encoding. For 3), we propose a particle-based solution to simultaneously estimate both the model ensemble and the kinematics recursively in time.

The proposed DyEnsemble model extends Bayesian neu- ral decoders by incorporating Bayesian filtering and Bayesian model averaging in a uniform state-space formulation and a particle-based solution. With the dynamic model ensemble pro- cess, DyEnsemble can adapt to changes in neural activities; thus, it can better cover the neural variability to obtain a more robust online BMI control. In closed-loop BMI experiments with a human subject, DyEnsemble achieves significant performance improvement compared with the velocity Kalman filter. In the random target pursuit task, DyEnsemble increases the success
rate by 13.9% and performs more stably over different exper- iment days, which demonstrates superior control accuracy and robustness. Analysis shows that DyEnsemble can adaptively adjust the model weights and incline to proper models along with changes in signals; thus, robust performance can be achieved.