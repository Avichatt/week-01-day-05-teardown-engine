### Which of the 6 layers surprised you the most in terms of complexity for the product you chose? Why?

For the basic calculator app, **Layer 5 (Deployment & Core Execution Logic)** was the most surprisingly “non-trivial.” At first glance, a calculator feels trivial, but the moment you examine floating-point precision, operator precedence parsing, and edge-case handling (like chained expressions and parentheses), you realize there is subtle algorithmic rigor involved. It’s not complex in scale, but it demands correctness discipline — especially around numeric representation errors and deterministic behavior. The surprise wasn’t scale — it was how much correctness matters even in “simple” systems.

---

### What was the single biggest difference you noticed between the LLMs you tested?

The biggest difference wasn’t tone or verbosity — it was **layer discrimination discipline**. The stronger model (Claude-class) correctly collapsed irrelevant layers (ML, LLM orchestration) when analyzing the calculator app, explicitly stating “Layer 4 does not apply.” Weaker models tended to either over-elaborate every layer uniformly or subtly fabricate sophistication to maintain structural symmetry. The key differentiator was the ability to *withhold complexity* when it wasn’t justified — that restraint is what made the output feel architecturally intelligent rather than template-driven.
