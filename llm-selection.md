Using the same three systems:

* LLM 1: OpenAI (GPT-4 class)
* LLM 2: Anthropic (Claude 3 class)
* LLM 3: Google DeepMind (Gemini 1.5 class)

---

# LLM Selection Decision

| Decision Factor                                                                    | My Choice      | Reason (1 sentence)                                                                        |
| ---------------------------------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------------ |
| Which LLM followed my prompt structure most faithfully?                            | LLM 2 (Claude) | It adhered most cleanly to section boundaries and formatting constraints without drifting. |
| Which LLM was most technically accurate (least hallucination)?                     | LLM 2 (Claude) | It was the most cautious about naming technologies and avoided speculative stack details.  |
| Which LLM's output was most readable and well-organized?                           | LLM 2 (Claude) | Its hierarchical structure and clarity made cross-layer comparison easier.                 |
| Which LLM handled the "honesty check" best (admitting when a layer doesn't apply)? | LLM 2 (Claude) | It was most willing to explicitly say when a layer was thin or minimally used.             |

---

**Selected LLM for final tool:** Claude (Anthropic)

**Why:** While GPT-4 was more technically deep, Claude produced the most structurally faithful, cautious, and evaluation-aligned output — which makes it more reliable for a repeatable architectural teardown tool where hallucination control and format consistency matter more than maximal technical speculation.
