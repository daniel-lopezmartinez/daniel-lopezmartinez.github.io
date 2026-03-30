---
title: "The Evaluation Stack for Health AI"
date: 2026-03-15
permalink: /posts/2026/03/2026-03-15-health-ai-evals/
description: "Why medical knowledge benchmarks aren’t enough for real-world health assistants, and what an evaluation stack should look like as Health AI moves from static vignettes to conversational, action-taking systems."
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


## The Knowledge Benchmark Era

Until recently, health AI evaluation focused heavily on medical licensing exams and multiple-choice question answering [[1](#ref-1), [2](#ref-3)], as well as short clinical vignettes [[4]](#ref-4). These benchmarks served a real purpose. They were standardized, reproducible, and gave the field a shared language for measuring progress. And the progress was real: language models performing strongly on medical knowledge benchmarks was a legitimate scientific achievement.

However, these benchmarks are not the endpont. 

Saturating a knowledge benchmark doesn't tell you whether a system is safe or useful when deployed.  For example, A model that can ace a multiple-choice question about beta-blocker pharmacology may still fail in practice when a patient reports dizziness on bisoprolol without volunteering their fever severity, and the system recommends a routine next-day appointment instead of urgent evaluation. While the knowledge may be there, the clinical judgment, exercised dynamically across a real conversation with incomplete information, may not necessarily be.

So knowledge benchmarks that answer the question: *does this model know medicine?* is a necessary condition, but it is nowhere near sufficient.

## The Interaction Gap

The deeper problem is structural. Most traditional benchmarks are single-turn: the system receives a fixed input and produces a fixed output. Real health interactions are nothing like that. A patient begins with partial information, answers follow-up questions selectively, and interprets the system’s responses through their own health literacy, emotional state, and prior experiences.

That means model capability does not automatically translate into effective real-world use.

Recent work has made this gap especially clear. When leading models are tested in isolation on fully specified medical scenarios, they may perform impressively. But once real users are involved, performance can deteriorate sharply [[2]](#ref-2). Users may omit important details, describe symptoms imprecisely, or misunderstand the system’s guidance. A strong model can still underperform in practice if the interaction itself is poorly scaffolded.

This is why health AI evaluation is partly a modeling problem, but also an HCI problem. The relevant question is not only whether the model can produce a high-quality answer. It is also whether the system helps the user arrive at the information needed for a safe answer in the first place.

## The Agentic Dimension

The problem becomes even harder once health AI systems stop being pure question-answering systems and start becoming agents. A traditional benchmark can tell you whether a model knows something, or even whether it can produce a reasonable answer under controlled conditions. But agentic health AI has to do more than answer. It has to decide what information is missing, determine whether it is safe to proceed, use tools correctly, and complete workflows without creating new risks in the process.

That changes the evaluation target. The question is no longer just whether the model produced a good response. It is whether the system behaved appropriately as an actor inside a clinical workflow. And that requires measuring dimensions that traditional benchmarks do not capture.

## The right unit of evaluation is the system

For health AI, the right unit of evaluation is almost never just the base model. It is the **system**: the model, prompts, retrieval layer, policy constraints, tools, escalation logic, interface, and the human on the other side of the interaction. That distinction matters because failures often happen in the seams.


The frame I find most useful is to think about evaluation as a stack rather than a single test. For me, that stack has five layers.

1. Capability evaluation: Can the model retrieve relevant medical knowledge, reason over symptoms, recognize obvious red flags, and follow core safety policies?
2. Conversation evaluation: Can it handle realistic, multi-turn interactions with appropriate context gathering, uncertainty expression, escalation behavior, and communication quality?
3. Workflow and agent evaluation: Can it use tools correctly, maintain state, avoid hallucinating completed actions, and behave reliably inside healthcare workflows such as triage, refill management, scheduling, or information retrieval?
4. Human-AI evaluation: Do patients or clinicians actually use the system well? Do they know what information to provide? Do they interpret outputs appropriately? Does the interface support good judgment?
5. Prospective real-world evaluation and post-deployment monitoring: Does the system work under real conditions, with real users, real oversight, and ongoing surveillance for regressions, failure modes, and unexpected patterns of use?

Each layer answers a different question. None of them fully substitutes for the others.

## In Conclusion

The question of how to evaluate agentic health AI fairly and comprehensively is unsolved. But the conversation is moving in the right direction: toward multi-turn interaction, realistic patient complexity, evaluation frameworks that treat clinical safety as a primary criterion, and the recognition that evaluating agents requires measuring what they do and the corresponding outcomes, not just what they say.

The future of health AI will be built on warranted trust. Warranted trust requires the ability to actually distinguish systems that are safe and effective from systems that merely look impressive under the controlled conditions where we tend to measure them. Getting that distinction right isn't a technical footnote to the work of building these systems.

It is the work. And the right mantra for the next phase of the field is simple: **evaluate the system, not just the model.**



## References
- <a id="ref-1"></a>[1] [Toward expert-level medical question answering with large language models](https://www.nature.com/articles/s41591-024-03423-7)
- <a id="ref-2"></a>[2] [Reliability of LLMs as medical assistants for the general public: a randomized preregistered study](https://www.nature.com/articles/s41591-025-04074-y)
- <a id="ref-3"></a>[3] [Benchmarking large language models on the United States medical licensing examination for clinical reasoning and medical licensing scenarios](https://www.nature.com/articles/s41598-025-31010-4)
- <a id="ref-4"></a>[4] [A vignette-based evaluation of ChatGPT’s ability to provide appropriate and equitable medical advice across care contexts](https://www.nature.com/articles/s41598-023-45223-y)