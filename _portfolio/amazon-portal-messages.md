---
title: "AI-Driven Patient Message Routing & Automation (One Medical)"
excerpt: "An AI-driven system for routing and automating patient portal messages at One Medical, reducing clinician burden and improving operational efficiency at national scale."
collection: portfolio
category: amazon
order: 3
---


### Overview

At One Medical, I led applied ML and systems work to address one of the fastest-growing operational burdens in modern healthcare: patient portal message overload at scale.

Patient portals allow patients to message their care team asynchronously, but in practice most messages default to a patient’s primary care provider (PCP), even when the request is administrative, logistical, or better handled by a specialized operations team. This behavior overwhelms clinicians, increases burnout, and slows response times for patients.

My work focused on designing and productionizing an AI-driven routing and automation system that analyzes incoming patient messages and dynamically directs them to the appropriate destination across One Medical’s centralized care operations, with automatic actions and responses generated where appropriate.

### Intelligent Message Routing at Scale

I built a system that uses language models to perform topic, intent, and operational classification over patient portal messages. Based on these signals, messages are re-routed in real time to the correct team using configurable decision logic that can adapt to changing operational constraints.

This routing layer decoupled message understanding from downstream workflows, enabling One Medical to evolve policies and staffing models without retraining models or rewriting core logic.

### Automation of Responses and Actions

For a subset of well-defined message categories, the system supports automated responses and actions, including templated replies and workflow triggers. This reduced manual handling for routine requests while preserving human oversight for clinical decision-making and high-risk cases.

### Deep Operational Integration

To design the system, I spent time onsite at One Medical’s Arizona mission control center, working directly with the teams responsible for triaging and responding to patient messages nationwide. I conducted large-scale statistical analysis over millions of historical messages to understand volume patterns, failure modes, and opportunities for automation.

I partnered closely with product, engineering, and clinical stakeholders to ensure the solution aligned with real workflows, safety requirements, and regulatory constraints. The resulting system was deployed across One Medical’s U.S. footprint, improving routing accuracy, reducing clinician burden, and accelerating patient response times across the care network.