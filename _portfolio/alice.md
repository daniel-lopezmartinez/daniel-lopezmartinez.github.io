---
title: "Scalable Trust, Safety, and Quality Infrastructure for LLM-Based Shopping Assistants"
excerpt: "Scalable evaluation framework to assess factual accuracy, safety, and quality across millions of LLM-generated shopping answers.<br/><img src='/images/blog/rufus.jpg' width='300'>"
collection: portfolio
category: amazon
order: 1
---

### Overview

This project focuses on building the large-scale evaluation and quality infrastructure supporting [Rufus](https://www.aboutamazon.com/news/retail/amazon-rufus), Amazon’s generative shopping assistant. As generative models became deeply integrated into the shopping experience, ensuring factual accuracy, relevance, and safety at scale became a first-order product and trust requirement.

I led the development of systems to automatically produce actionable quality metrics and root-cause analyses across millions of LLM-generated shopping responses per week, spanning diverse query types such as product recommendations and factoid questions. Rather than relying solely on manual review, the framework combines automated defect detection with human-in-the-loop annotation to balance scale, precision, and reliability.


### Red-Teaming and Adversarial Evaluation

To complement offline evaluation and human annotation, I developed an automated red-teaming framework designed to systematically surface failure modes in large language models. Rather than relying on manual prompt crafting, the approach generates synthetic prompts that are explicitly optimized to elicit responses that violate predefined constraints such as factual correctness, safety, or policy compliance.


This approach, described in the patent [Systems for Generation of Prompts for Evaluation of Language Models](/publication/2025-llm-red-teaming-patent), enables scalable, repeatable adversarial testing and integrates directly with production evaluation pipelines, allowing red-teaming signals to continuously inform quality metrics, root-cause analysis, and model iteration.


### Medical-Specific Trust & Safety Evaluation

As part of the broader Trust & Safety evaluation framework, I led the development of Amazon’s first medical-specific safety evaluation system. While medical queries represented a relatively small fraction of overall traffic, they carried disproportionately high risk, requiring strict guarantees. This work focused on detecting and preventing unsafe behaviors such as implicit or explicit medical advice, off-label product recommendations, and misleading health claims in LLM-generated responses.


### Publications & intellectural property

Publications:
- [Guardrails for avoiding harmful medical product recommendations and off-label promotion in generative AI models](https://daniellopezmartinez.com/publication/2024-cvpr-guardrails)
- [Trustworthiness in medical product question answering by large language models](https://daniellopezmartinez.com/publication/2024-kdd-medical-trustworthiness)
- [Detecting sensitive medical responses in general purpose large language models](https://daniellopezmartinez.com/publication/2024-ml4h-detecting-sensitive-responses)

Patents:
- [Systems for generation of prompts for evaluation of language models](/publication/2025-llm-red-teaming-patent) (lead inventor on patent for automated red-teaming).
