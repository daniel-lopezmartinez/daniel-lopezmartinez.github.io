---
title: 'From Stochastic Parrots to Software as a Doctor'
date: 2025-12-07
permalink: /posts/2025/12/2025-12-07-llms-as-a-device/
tags:
  - science
---

LLMs have been characterized as [stochastic parrots](https://dl.acm.org/doi/pdf/10.1145/3442188.3445922), probabilistic systems that merely remix text without understanding and predict the next word. But the frontier is shifting. Today, the question is no longer whether LLMs can imitate clinical expertise, but how we transform them into regulated medical devices that can interview patients, form preliminary diagnoses, triage safely, and even prescribe.

## Regulatory context

Any discussion about deploying AI in healthcare must begin with the [U.S. Food and Drug Administration (FDA)](https://www.fda.gov/), the federal agency responsible for ensuring that medical products are safe and effective before they reach patients. The FDA regulates not only physical instruments but also software that meets the statutory definition of a medical device. That is, software “_intended for use in the diagnosis of disease or other conditions, or in the cure, mitigation, treatment, or prevention of disease_.” As the FDA notes in its [AI/ML Action Plan](https://www.fda.gov/news-events/press-announcements/fda-releases-artificial-intelligencemachine-learning-action-plan), medical software that influences real clinical decisions requires rigorous oversight. Because of this statutory framework, any software that interprets symptoms, suggests diagnoses, assesses clinical risk, or prioritizes patients for care is automatically treated as a medical device. The FDA has reaffirmed this by defining [AI-enabled device software functions (AI-DSFs)](https://www.fda.gov/media/184856/download) as any AI system used for a medical purpose, whether standalone Software as a Medical Device (SaMD) or embedded inside another product. This places many uses of LLMs in healthcare squarely within FDA jurisdiction.

A brief caveat: not all clinical software is regulated. The FDA exempts certain [non-device Clinical Decision Support (CDS) tools](https://www.fda.gov/medical-devices/software-medical-device-samd/clinical-decision-support-software-frequently-asked-questions-faqs) when clinicians can independently review the basis for the recommendation and avoid relying solely on the software’s logic. However, LLM-based diagnostic or triage systems do not meet these criteria. Their reasoning is not reviewable in the sense FDA requires, and their outputs directly influence diagnostic assessment or urgency classification, placing them firmly in the category of regulated medical devices.

Over the past decade, the FDA has approved [over one thousand AI/ML–based medical devices](https://www.fda.gov/medical-devices/software-medical-device-samd/artificial-intelligence-enabled-medical-devices) most notably in radiology, cardiology, pathology, dermatology, and physiologic monitoring. A recent [review](https://www.nature.com/articles/s41746-025-01800-1) found that these systems are typically for imaging (84%) and signal-processing (14.5%) applications. From a clinical-function perspective, 84% of authorized devices are used for assessment tasks (detection, diagnosis, monitoring, or risk scoring) whereas only 16% are used for interventional tasks (e.g. treatment guidance or surgical planning).

Within the assessment category, the dominant AI behavior is not high-level reasoning but quantification and feature localization, which accounts for 58% of all devices. This includes things like measuring anatomical structures, segmenting lesions, or extracting waveform features. Triage algorithms (e.g., flagging abnormal scans for prioritized review) make up about 11%, while “diagnosis” algorithms constitute only 6–7% of devices


The regulatory pathways for such imaging- and signal-based systems are now well established. However, the FDA has not yet granted marketing authorization to any LLM-based system, whether for "_diagnosis, treatment, prevention, cure, or mitigation_" of disease. Not a single authorized device to date uses an LLM as its core inference engine. While the agency has issued forward-looking guidance acknowledging the unique challenges of genAI and natural-language interfaces, it has not yet reviewed a model whose primary mode of operation is conversational. As a result, developers of LLM-based AI clinicians must look to existing Software-as-a-Medical-Device (SaMD) precedent, general AI/ML regulatory principles, and emerging FDA guidance to understand what evidence will be expected.  The path for conversational diagnostic AI is not yet defined, but the foundational expectations are already visible.


## Relevant FDA Frameworks and Guidance Documents

- [IMDRF SaMD Framework](https://www.imdrf.org/working-groups/software-medical-device-samd)
- [FDA’s AI/ML-Based SaMD Action Plan](https://www.fda.gov/news-events/press-announcements/fda-releases-artificial-intelligencemachine-learning-action-plan)
- [FDA's Predetermined Change Control Plans (PCCP)](https://www.fda.gov/medical-devices/software-medical-device-samd/predetermined-change-control-plans-machine-learning-enabled-medical-devices-guiding-principles)
- [FDA's Clinical Decision Support (CDS) Guidance](https://www.fda.gov/media/109618/download)
- [FDA's Good Machine Learning Practice Principles](https://www.fda.gov/medical-devices/software-medical-device-samd/good-machine-learning-practice-medical-device-development-guiding-principles)
- [FDA's Marketing Submission Recommendations for a Predetermined Change Control Plan for Artificial Intelligence-Enabled Device Software Functions](https://www.fda.gov/media/166704/download)
- [Artificial Intelligence-Enabled Device Software Functions: Lifecycle  Management and Marketing Submission Recommendations](https://www.fda.gov/media/184856/download)
