---
title: "ML-Enabled Phone-Based ECG Signal Quality Assessment (University of Oxford, 2011)"
excerpt: "Automated assessment of ECG signal quality using signal quality indices and classifier fusion for mobile and low-resource healthcare."
collection: portfolio
category: undergraduate
order: 2
---

### Overview

This project focused on automated assessment of electrocardiogram (ECG) signal quality to determine whether recordings are diagnostically acceptable when acquired in noisy, ambulatory, or low-resource settings. The work was conducted during an undergraduate research appointment at the Oxford Institute of Biomedical Engineering (IBME), University of Oxford, in collaboration with Gari Clifford.

I co-presented this work with Prof. Clifford as an oral presentation at the Computing in Cardiology Conference (CinC) 2011, held in Hangzhou, China.

### Methodological Focus

The project introduced a framework for automatically classifying ECG recordings as clinically acceptable or unacceptable based on a combination of signal quality indices (SQIs) and machine-learning–based data fusion.

We designed SQIs capturing complementary aspects of ECG quality, including:
- Spectral and frequency-domain characteristics
- Higher-order statistical moments
- Beat-detection agreement across algorithms
- Multi-lead consistency metrics in 12-lead ECGs

These features were combined using classifiers such as support vector machines (SVMs) and multi-layer perceptrons (MLPs) to produce robust acceptability decisions under varying noise conditions.

### Data Fusion and Robustness

A central contribution of this work was demonstrating that classifier fusion across heterogeneous SQIs substantially improves robustness compared to relying on any single quality metric. By aggregating evidence from multiple leads and feature families, the system was able to tolerate common acquisition artifacts such as motion noise, electrode misplacement, and poor skin contact.

The algorithms were designed to be lightweight and computationally efficient, enabling near real-time execution on mobile or embedded devices.

### PhysioNet / CinC Challenge 2011

This work formed part of the PhysioNet/Computing in Cardiology Challenge 2011, which focused on ECG quality assessment for consumer and ambulatory monitoring scenarios.

Our team placed 2nd in Event 1 of the challenge. On held-out test data, the proposed approach achieved up to ~95% accuracy in distinguishing acceptable from unacceptable ECG recordings.

The broader goal of the challenge—and of this work—was to enable automated ECG triage, providing immediate feedback to non-expert users (e.g., detecting poor signal quality or electrode placement issues and prompting re-acquisition when necessary).

### Contributions and Impact

This project demonstrated that reliable, automated ECG quality assessment is feasible even in challenging acquisition environments, and that data-fusion–based approaches are critical for robustness.

The results informed:
- Design of mobile and point-of-care ECG systems
- Signal-quality–aware clinical pipelines
- User-feedback mechanisms for self-acquired biosignals

More broadly, the work contributed to early foundations of real-time physiological signal triage, a theme that later reappears in my work on multimodal sensing, healthcare AI, and robust model evaluation under real-world noise.