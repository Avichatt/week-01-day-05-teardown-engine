# Reflection: AI Architectural Teardown Exercise

### 1. How did the prompt evolution (v1 -> v2) improve the quality of the output?
The transition from V1 to V2 shifted the perspective from "Functional Description" to "Structural Reasoning." 
- **In V1**, the prompt asked for "What is happening," which often resulted in generic feature lists (e.g., "It uses a database"). 
- **In V2**, the introduction of the **Senior AI Architect Persona** and the requirement to **Reason from First Principles** forced the LLM to hypothesize specific infrastructure (e.g., "vLLM for serving," "Kafka for streaming") based on the product's scale. 
- The addition of specific "Hard Engineering Challenges" and "Hiring Profiles" for each layer grounded the output in reality, making it feel like an actual technical interview or board-room deconstruction rather than a Wikipedia summary.

### 2. Which architecture layer surprised you most in its complexity during this exercise?
**Layer 3 (Machine Learning Models)** in the context of LLM products. 
It’s easy to assume that LLM products are *only* LLMs. However, the deconstruction of Perplexity AI and Midjourney revealed that the "invisible" classic ML layers—like **re-ranking Cross-Encoders** for search or **Style-Reference Encoders** for image generation—are often the secret sauce. While the LLM provides the "brain," the Layer 3 models act as the "nervous system," filtering and ranking information before it ever hits the expensive generative layer. This realization clarifies why simple "prompt-only" wrappers often fail to compete with built-out architectural products.
