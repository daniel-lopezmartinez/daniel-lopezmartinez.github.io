---
title: "Objective Pain Detection from Brain Signals using fNIRS"
excerpt: "Personalized machine learning on wearable neuroimaging signals to objectively detect pain in non-communicative patients.<br/><img src='/images/blog/2019-09-12-fnirs.jpg' width='300'>"
collection: portfolio
category: mit
order: 5
---


### Overview

This project investigated how brain signals measured with functional near-infrared spectroscopy (fNIRS) can be used to objectively detect the presence of pain, even when patients are unable to communicate. The work was motivated by a core clinical gap: pain assessment today relies almost entirely on self-report, which fails for unconscious, sedated, pediatric, elderly, or cognitively impaired patients.

Developed at MIT in collaboration with Harvard Medical School and Massachusetts General Hospital, the system combines portable neuroimaging with personalized machine learning to enable practical, bedside-compatible pain monitoring.

### Wearable Neuroimaging for Pain Assessment

fNIRS is a non-invasive brain-imaging technique that measures changes in oxygenated and deoxygenated hemoglobin associated with neural activity. Unlike fMRI, fNIRS is lightweight, inexpensive, and suitable for continuous monitoring in clinical settings such as operating rooms.

To maximize clinical feasibility, this work focused exclusively on prefrontal cortex signals, accessed via a small number of sensors placed on the forehead. Prior neuroscience work suggests the prefrontal cortex plays an integrative role in pain perception, making it a promising target for compact, unobtrusive sensing.

Additional short-separation sensors were used to filter out physiological noise from scalp and skin, improving signal quality in real-world conditions.

### Personalized Machine Learning Approach

A key challenge in pain detection is inter-individual variability: people exhibit markedly different neural responses to pain. Rather than training a single population-average classifier, this project introduced a personalized multi-task learning framework.

The pipeline included:
- Time–frequency feature extraction using continuous wavelet transforms
- Hierarchical Bayesian multi-task learning with Dirichlet process priors
- Simultaneous learning of population-level structure and individual-specific pain response patterns

This approach allowed the model to adapt to individual pain phenotypes while still leveraging shared information across participants.

### Experimental Evaluation

The system was evaluated on data collected from 43 participants exposed to controlled noxious and non-noxious stimuli while wearing the fNIRS device. Using only frontal brain signals, the personalized models achieved ~87% accuracy in distinguishing pain vs. no-pain states, substantially outperforming standard single-task classifiers.

These results demonstrated that accurate pain detection is possible using a small number of wearable sensors and appropriately personalized inference.
