---
title: "The Evaluation Stack for Health AI"
date: 2026-03-15
permalink: /posts/2026/03/2026-03-15-heath-ai-evals/
description: "Why medical knowledge benchmarks aren’t enough for real-world health assistants—and what an evaluation stack should look like as Health AI moves from static vignettes to conversational, action-taking systems."
tags:
  - health-ai
  - llms
  - evaluation
  - ai-safety
  - healthcare
---

For a long time, medical AI evaluation was dominated by knowledge benchmarks: medical licensing exams, multiple-choice question answering, and short clinical vignettes [[1]](#ref-1). These benchmarks were useful. They helped establish that language models had absorbed enough medical knowledge to be taken seriously at all.

But health AI is no longer just about answering exam-style questions or generating plausible-sounding advice. The frontier is shifting toward systems that hold real-world conversations with patients, ask follow-up questions, retrieve context, explain medical information, and increasingly take action inside clinical workflows. Once that happens, the old defaults for evaluation start to break down.

A model can do very well on a licensing-style benchmark and still be weak at triage. It can look strong on a static vignette and still fail once a real user is involved. It can sound clinically sophisticated and still make mistakes when it has to gather missing information, manage uncertainty, or execute a workflow correctly.

Frontier models now perform extremely well on many medical knowledge benchmarks. But as health AI moves toward broader real-world deployment, we are learning a more humbling lesson: saturating a knowledge benchmark is not the same as practicing medicine safely.

That is why health AI needs an evaluation stack.


## References
- <a id="ref-1"></a>[1] [Toward expert-level medical question answering with large language models](https://www.nature.com/articles/s41591-024-03423-7)
- <a id="ref-2"></a>[2] [Reliability of LLMs as medical assistants for the general public: a randomized preregistered study](https://www.nature.com/articles/s41591-025-04074-y)