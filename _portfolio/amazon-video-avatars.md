---
title: "Video Avatars & Multimodal Experiences"
excerpt: "Applied research, design and prototyping of real-time multimodal video avatar systems that shaped Amazon’s strategy for agentic, embodied AI experiences."
collection: portfolio
category: amazon
order: 4
---


### Overview

This project explored how real-time, multimodal video avatars can enable more natural, persistent, and task-oriented interactions between users and AI systems. The work focused on designing and prototyping embodied, agentic interfaces that combine speech, vision, and structured interaction flows, and on understanding the architectural and UX trade-offs required to make such systems viable at scale.

The project served as a strategic proof of concept for how large language models, low-latency speech pipelines, and expressive video avatars can be orchestrated into coherent, end-to-end experiences. While one concrete application area involved healthcare pre-visit intake and digital provider experiences, the underlying architecture and interaction patterns were intentionally designed to generalize across domains where trust, continuity, and rich human–AI interaction matter.

Through multiple prototype iterations, the work evaluated key design dimensions (including latency, realism, turn-taking, interruption handling, modularity, and deployment constraints) and informed broader thinking across Amazon on agentic, embodied AI systems. The resulting insights directly influenced roadmap discussions and long-term strategy around multimodal AI experiences, beyond any single product or vertical.


### System Design & Architecture

I designed and implemented end-to-end prototypes enabling real-time interaction between a user and a digital avatar in the browser. The system integrated multiple AI components into a low-latency, modular pipeline:
- Speech & turn detection for conversational flow
- Speech-to-text (STT) for real-time transcription
- LLM-based response generation, abstracted behind a backend service
- Text-to-speech (TTS) with streaming audio output
- Video avatar rendering with synchronized lip-sync and expressive motion
- WebRTC transport for low-latency audio/video delivery


Within this framework, I evaluated multiple approaches for avatar representation and synthesis, including:
- Video-based avatar generation pipelines suitable for near-real-time interaction
- Diffusion-based generative models for expressive, high-fidelity avatar synthesis, particularly in non-real-time or semi-streaming settings
- 3D Gaussian splatting–based representations as a potential path toward more flexible, view-consistent, and lower-latency avatar rendering compared to traditional mesh- or video-only approaches

These explorations informed architectural trade-offs around latency, realism, controllability, and deployment complexity, and helped shape longer-term thinking about how embodied AI systems might evolve beyond static video avatars toward more dynamic and generalizable visual representations.