---
title: "Detecting Real World Driving Induced Affective State Using Physiological Signals"
collection: talks
type: "Talk"
permalink: /talks/2019-09-03-acii-seaixi
venue: "International Conference on Affective Computing and Intelligent Interaction (ACII), SEAIxI Workshop"
date: 2019-09-03
location: "Cambridge, UK"
---

I delivered an oral presentation at the [International Conference on Affective Computing and Intelligent Interaction (ACII 2019)](https://acii-conf.net/2019/) in Cambridge, UK, during the [International Workshop on Social and Emotion AI for Industry (SEAIxI)](https://acii-conf.net/2019/workshop-information/). The presentation summarized our work on detecting real world, driving induced affective states using physiological signals, based on our [paper](https://ieeexplore.ieee.org/document/8925190) presented at the conference.

The talk addressed a central challenge in affective computing for automotive applications: emotional and cognitive states during daily driving fluctuate rapidly, affect safety, and vary substantially across individuals and contexts. Unlike controlled driving simulators, real world driving introduces unpredictable environmental events, making affect detection significantly more difficult. We proposed a multi view, multi task machine learning framework capable of modeling these variations by leveraging two unobtrusively captured physiological signals commonly available in wearables: electrodermal activity (EDA) and heart rate (HR).

Using three public datasets of real world driving (MIT DriveDB, HciLab, and AffectiveROAD), we demonstrated that combining physiological features with a personalized learning strategy improves affective state inference. The method integrates multi view learning, to automatically assess the relative importance of different physiological modalities, with multi task learning, to account for inter drive variability by grouping drives into latent physiological profiles via spectral clustering.

Results showed that this personalized, multi task approach consistently outperformed standard single task models and provided interpretable insight into which signals contributed most to stress detection. In particular, the analysis highlighted the prominence of EDA features in distinguishing high versus low stress segments across datasets, in line with prior findings in affective computing and real world driving research.

The presentation at ACII 2019 emphasized the implications of this approach for emotion aware automotive interfaces, including systems that adapt tone of voice, provide timely assistance, or mitigate stress and fatigue during everyday driving. By improving robustness and interpretability, the work contributed to the development of socially and emotionally intelligent in vehicle systems capable of supporting safety, comfort, and well being in real world settings.
