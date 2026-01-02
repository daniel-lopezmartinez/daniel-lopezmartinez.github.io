---
title: "Buy For Me — Agentic Shopping System"
excerpt: "A browser-based agentic system that helps customers complete purchases across third-party websites using multimodal perception, reasoning, and tool-enabled actions.<br/><img src='/images/blog/buyforme.jpg' width='300'>"
collection: portfolio
category: amazon
order: 2
---


[Buy For Me](https://www.aboutamazon.com/news/retail/amazon-shopping-app-buy-for-me-brands) is an agentic commerce system within the Amazon Shopping app that enables customers to discover and purchase products from third-party brand websites when those items are not sold directly by Amazon. The system allows customers to delegate complex, multi-step shopping workflows, such as product discovery, configuration, and checkout, to an autonomous agent acting on their behalf, while remaining within the Amazon shopping experience. Unlike traditional integrations or chat-based assistants, _Buy For Me_ operates directly on real third-party webpages, navigating dynamic user interfaces to extract information, make decisions, and execute actions.

_Buy For Me_ autonomously executes end-to-end workflows that mirror how a human would shop on a third-party site, with additional verification and safety checks at each stage. During pre-purchase, the system surfaces eligible off-Amazon products and normalizes key product attributes so customers can evaluate options directly within the Amazon Shopping app. Once a customer authorizes a purchase, the agent executes the transaction by navigating the brand’s website on the customer’s behalf, managing multi-step interactions such as variant selection, cart updates, and checkout while handling dynamic UI behavior. After completion, post-purchase confirmations are ingested back into the app, enabling order tracking and support visibility while fulfillment, returns, and customer service remain managed by the brand.

_Buy For Me_ is implemented as a modular agentic architecture that combines multimodal large language models for reasoning and planning with browser-based automation for executing actions on real third-party websites. Multimodal LLMs reason over page structure, rendered content, and user intent to plan multi-step workflows, while an action layer navigates dynamic UIs to interact with the websites and perform actions. A key challenge was achieving reliable, low-latency execution at scale across highly variable and partially observable web environments under strict product, safety, and trust constraints.

As a founding scientist behind _Buy For Me_, I contributed from early problem framing through productionization. My work spanned defining the end-to-end agentic workflow for off-Amazon purchasing, evaluating and selecting between alternative agent frameworks, and shaping the decision to build a first-party agentic system. I worked on the core system design, evaluation, data, and scaling strategy for purchase automation, built early proof-of-concept agents, authored key components of the multi-agent framework used for reasoning and action execution, and developed browser-level authentication mechanisms to enable automated, end-to-end purchasing.
 

_Buy For Me_ has been covered by [Forbes](https://www.forbes.com/sites/kirimasters/2025/04/08/amazon-buy-for-me-is-the-latest-entrant-in-the-ai-shopping-agent-race/), [Engadget](https://www.engadget.com/ai/amazons-buy-for-me-ai-will-purchase-stuff-from-third-party-websites-123036361.html), [The Verge](https://www.theverge.com/news/642947/amazon-ai-buy-products-other-websites), [9to5mac](https://9to5mac.com/2025/04/03/amazons-new-buy-for-me-feature-is-a-wild-ai-innovation/) and others.

### Patents

- [Systems for automated interaction with user interfaces](/publication/2025-agentic-ui-automation-patent) (patent application)
