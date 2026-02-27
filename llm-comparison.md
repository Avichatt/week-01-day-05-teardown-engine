# LLM Comparison — Product Teardown: Perplexity AI

| # | LLM Name | Mode     | Response Time |
| - | -------- | -------- | ------------- |
| 1 | ChatGPT  | Thinking | ~18–25s       |
| 2 | Claude   | Standard | ~8–12s        |
| 3 | Gemini   | Flash    | ~4–6s         |

## Layer-by-Layer Comparison

### Layer 1 — Data Foundation
| Criteria                   | LLM 1 | LLM 2 | LLM 3   | Best? |
| -------------------------- | ----- | ----- | ------- | ----- |
| Specificity (1-5)          | 5     | 4     | 2       | 1     |
| Named real tech?           | Y     | Y     | Partial | 1     |
| Real engineering challenge? | Y     | Y     | Weak    | 1     |

### Layer 2 — Statistics & Analysis
| Criteria                   | LLM 1   | LLM 2 | LLM 3 | Best? |
| -------------------------- | ------- | ----- | ----- | ----- |
| Specificity (1-5)          | 4       | 3     | 2     | 1     |
| Named real tech?           | Partial | No    | No    | 1     |
| Real challenge identified? | Y       | Weak  | No    | 1     |

### Layer 3 — Machine Learning Models
| Criteria                    | LLM 1 | LLM 2 | LLM 3   | Best? |
| --------------------------- | ----- | ----- | ------- | ----- |
| Specificity (1-5)           | 5     | 4     | 3       | 1     |
| Named model family?         | Y     | Y     | Partial | 1     |
| Real engineering challenge? | Y     | Y     | Weak    | 1     |

### Layer 4 — LLM / Generative AI
| Criteria                  | LLM 1 | LLM 2 | LLM 3 | Best? |
| ------------------------- | ----- | ----- | ----- | ----- |
| Specificity (1-5)         | 5     | 4     | 3     | 1     |
| Honest if not applicable? | Y     | Y     | Weak  | 1     |

### Layer 5 — Deployment & Infrastructure
| Criteria          | LLM 1 | LLM 2   | LLM 3 | Best? |
| ----------------- | ----- | ------- | ----- | ----- |
| Specificity (1-5) | 4     | 3       | 2     | 1     |
| Named real tech?  | Y     | Partial | No    | 1     |

### Layer 6 — System Design & Scale
| Criteria          | LLM 1 | LLM 2   | LLM 3 | Best? |
| ----------------- | ----- | ------- | ----- | ----- |
| Specificity (1-5) | 5     | 4       | 3     | 1     |
| Named real tech?  | Y     | Partial | No    | 1     |

## Overall Dimension Comparison

| Dimension                        | Winner | Why                                     |
| -------------------------------- | ------ | --------------------------------------- |
| Most technically specific        | 1      | Named architectures + tradeoffs         |
| Best at naming real technologies | 1      | Concrete stack details                  |
| Least hallucination              | 2      | Claude was more conservative            |
| Best hardest-problem insight     | 1      | Identified retrieval-grounding coupling |
| Best structure                   | 2      | Claude formatted cleaner                |
| Fastest useful response          | 3      | Gemini was fastest but shallow          |

## Key Observations (The Real Insights)

### 1️⃣ Thinking Mode vs Standard Mode
The thinking model:
- Explored tradeoffs
- Identified system coupling
- Highlighted failure modes
Standard models described components; Thinking models reasoned about constraints. **That’s a huge difference.**

### 2️⃣ Hallucination Behavior
- Gemini occasionally named plausible but vague systems.
- ChatGPT (Thinking) used "likely" qualifiers.
- Claude avoided overclaiming specific tech.
**Claude was the most conservative.**

### 3️⃣ Structure vs Depth Tradeoff
- **Claude:** Cleaner markdown, more readable.
- **ChatGPT:** More architecturally deep, more engineering insight.
This is why professionals extract best parts.

## 🔥 The Biggest Difference Between LLMs
The reasoning model didn’t just describe layers. It **connected layers causally.**
It identified bottlenecks and explained why Perplexity’s hallucination problem is harder than ChatGPT’s.

That’s the difference between:
- "Uses RAG."
- **“Retrieval quality bounds generation reliability; latency constraints limit chunk depth, increasing hallucination risk.”**

That’s interview-level thinking.
