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

Within the assessment category, the dominant AI behavior is not high-level reasoning but quantification and feature localization, which accounts for 58% of all devices. This includes things like measuring anatomical structures, segmenting lesions, or extracting waveform features. Triage algorithms (e.g., flagging abnormal scans for prioritized review) make up about 11%, while “diagnosis” algorithms constitute only 6–7% of devices.


The regulatory pathways for such imaging- and signal-based systems are now well established. However, the FDA has not yet granted marketing authorization to any LLM-based system, whether for "_diagnosis, treatment, prevention, cure, or mitigation_" of disease. Not a single authorized device to date uses an LLM as its core inference engine. While the agency has issued forward-looking guidance acknowledging the unique challenges of genAI and natural-language interfaces, it has not yet reviewed a model whose primary mode of operation is conversational. As a result, developers of LLM-based AI clinicians must look to existing SaMD precedent, general AI/ML regulatory principles, and emerging FDA guidance to understand what evidence will be expected.  The path for conversational diagnostic AI is not yet defined, but the foundational expectations are already visible.

## Core use cases for software as a doctor

If we take seriously the idea of software acting as a doctor, the relevant use cases are not those that simply streamline documentation or assist clinicians on the margins, but the tasks that truly embody the core clinical functions of a physician. These include information gathering (e.g. taking clinical histories and selecting appropriate tests), interpreting symptoms and results, making diagnostic inferences, assessing urgency and triage, recommending treatments, and, at the far end of the spectrum, prescribing autonomously. Each of these functions carries increasing levels of clinical risk, autonomy, and regulatory scrutiny.

### Autonomous prescribing: the endgame

Among all the core doctor functions, prescribing sits in a category of its own. It is where clinical judgment, pharmacology, risk management, and legal responsibility converge. It is also where the potential value of automation is enormous: a huge fraction of primary care encounters involve well-understood conditions with highly protocolized treatment pathways, from hyperlipidemia and hypertension to stable chronic disease management. If an AI system could safely and autonomously manage even a slice of these workflows, the value unlock would be profound.

Today, however, prescribing is tightly gatekept by law. The bill [H.R. 238 (Healthy Technology Act of 2025)](https://www.congress.gov/bill/119th-congress/house-bill/238) is interesting precisely because it touches this boundary: it would amend the [FD&C Act](https://en.wikipedia.org/wiki/Federal_Food,_Drug,_and_Cosmetic_Act) so that AI/ML technologies can, in principle, qualify as a “practitioner licensed by law to administer such drug,” provided two conditions are met:
- The AI system is authorized under state law to prescribe the drug involved.
- It has been approved, cleared, or authorized by the FDA under one of the existing device pathways.

On paper, that sounds like a potential inflection point. In practice, this bill is unlikely to become law in the near term. It has been introduced multiple times by the same sponsor, has never attracted co-sponsors, and has never advanced out of subcommittee. Even if it did pass, it would still face substantial friction at both the state level (no state currently recognizes AI as a prescribing practitioner) and within the FDA.

Still, it is worth paying attention to bills like [H.R. 238](https://www.congress.gov/bill/119th-congress/house-bill/238). They implicitly say that a future in which AI systems are accepted as autonomous prescribing agents is no longer unthinkable. In the meantime, the realistic path is not fully autonomous prescribing, but AI-driven prescription recommendations with human sign-off, especially for low-risk, high-volume conditions where guidelines are clear and a clinician can rapidly confirm or override the AI’s proposal.


## Relevant FDA Frameworks and Guidance Documents

- [IMDRF SaMD Framework](https://www.imdrf.org/working-groups/software-medical-device-samd)
- [FDA’s AI/ML-Based SaMD Action Plan](https://www.fda.gov/news-events/press-announcements/fda-releases-artificial-intelligencemachine-learning-action-plan)
- [FDA's Predetermined Change Control Plans (PCCP)](https://www.fda.gov/medical-devices/software-medical-device-samd/predetermined-change-control-plans-machine-learning-enabled-medical-devices-guiding-principles)
- [FDA's Clinical Decision Support (CDS) Guidance](https://www.fda.gov/media/109618/download)
- [FDA's Good Machine Learning Practice Principles](https://www.fda.gov/medical-devices/software-medical-device-samd/good-machine-learning-practice-medical-device-development-guiding-principles)
- [FDA's Marketing Submission Recommendations for a Predetermined Change Control Plan for Artificial Intelligence-Enabled Device Software Functions](https://www.fda.gov/media/166704/download)
- [Artificial Intelligence-Enabled Device Software Functions: Lifecycle  Management and Marketing Submission Recommendations](https://www.fda.gov/media/184856/download)
