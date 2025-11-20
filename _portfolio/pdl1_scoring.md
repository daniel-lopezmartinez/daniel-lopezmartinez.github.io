---
title: "AI-Assisted PD-L1 Scoring for Immunotherapy Decision Support"
excerpt: "Developed computer vision models to automatically quantify PD-L1 expression in immunohistochemistry slides.<br/><img src='/images/blog/2023-pathology-slides.jpg' width='300'>"
collection: portfolio
category: tempus
---

PD-L1 (Programmed Death–Ligand 1) is a protein expressed on tumor cells and certain immune cells, and its expression level is a critical biomarker for determining whether a patient is likely to benefit from anti-PD-1 / anti-PD-L1 immunotherapy. In clinical practice, PD-L1 expression is measured on immunohistochemistry (IHC) slides using the _Tumor Proportion Score (TPS)_ (the percentage of tumor cells showing membranous staining). This quantification is performed manually by pathologists and is known to be challenging, subjective, and variable, especially near low cutoffs such as the 1% threshold used for several cancer types.

At Tempus, I worked on building a deep-learning–based PD-L1 scoring system to assist pathologists in producing more consistent and reproducible assessments. Using whole-slide images (WSIs) of PD-L1–stained tissue, we trained computer vision models to identify tumor regions, detect PD-L1 staining, and estimate TPS in a fully automated pipeline.
