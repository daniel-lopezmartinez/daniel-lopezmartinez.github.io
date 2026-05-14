---
title: "Detection of Real-World Driving-Induced Affective State Using Physiological Signals"
excerpt: "Multi-view multi-task machine learning for detecting driver stress and affective states from physiological signals during real-world driving."
collection: portfolio
category: mit
order: 7
image: /images/blog/2019-09-03-cambridge-SEAIXI-talk.jpg
---

### Overview

This project developed a machine learning framework for detecting drivers' affective states (stress, workload) from physiological signals during real-world driving. Unlike controlled driving simulators, real-world driving introduces unpredictable events that make affect detection significantly more challenging. The work was conducted at the [Affective Computing group](https://www.media.mit.edu/groups/affective-computing/overview/) at the [MIT Media Lab](https://www.media.mit.edu/), in collaboration with [Neska El-Haouij](https://www.media.mit.edu/people/neska/overview/) and [Rosalind Picard](https://www.media.mit.edu/people/picard/overview/).

I presented this work as an [oral presentation](/talks/2019-09-03-acii-seaixi) at the [International Conference on Affective Computing and Intelligent Interaction (ACII 2019)](https://acii-conf.net/2019/) in Cambridge, UK.

### Methodological Approach

The project introduced a multi-view multi-task machine learning framework that combines:

1. **Multi-view learning (MVL):** Automatically learns the relative importance of different physiological signal modalities (electrodermal activity and heart rate) using multiple kernel learning.
2. **Multi-task learning (MTL):** Accounts for inter-drive variability by grouping drives into latent physiological profiles via spectral clustering, with each profile corresponding to a distinct learning task.

This personalized approach enables the model to handle the substantial variability in physiological responses across different drivers and driving contexts while maintaining interpretability of the learned models.

### Datasets and Results

The approach was evaluated on three publicly available datasets of real-world driving:
- **MIT DriveDB** — driving in the greater Boston area
- **HciLab** — driving in Stuttgart, Germany
- **AffectiveROAD** — driving in Tunisia

Results demonstrated that accounting for drive-specific differences through multi-task learning significantly improved affective state recognition:
- MIT DriveDB: 93% accuracy (vs. 85% single-task baseline)
- HciLab: 71% accuracy (vs. 64% single-task baseline)
- AffectiveROAD: 83% accuracy (vs. 70% single-task baseline)

Analysis of the learned kernel weights revealed that electrodermal activity features played a more important role than heart rate data in classification performance across all datasets.

### Contributions and Impact

This work contributed to the development of empathic automotive user interfaces — systems with social-emotional intelligence that can adapt their interaction style (e.g., tone of voice, timing of assistance) based on the driver's current affective state, ultimately improving driving safety, comfort, and well-being.

The approach addressed key requirements for real-world deployment: improved performance through personalization, interpretability of model decisions, and the ability to work with unobtrusively acquired physiological signals available in wearable devices.

### Publication

D. Lopez-Martinez, N. El-Haouij, and R. Picard, "Detection of Real-world Driving-induced Affective State Using Physiological Signals and Multi-view Multi-task Machine Learning," in *International Conference on Affective Computing and Intelligent Interaction (ACII)*, Cambridge, UK, 2019. [[IEEE]](https://ieeexplore.ieee.org/document/8925190) [[arXiv]](https://arxiv.org/abs/1907.09929)
