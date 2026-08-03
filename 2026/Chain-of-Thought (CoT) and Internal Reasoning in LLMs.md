Date of publish: May 2026
Authors: GPT
Tags: #LLM-COT #LLM-reasoning

Talk link: 
Paper link: 
Related: 
## Core Idea
Chain-of-thought (CoT) reasoning in LLMs is not just an “explanation generator.”  
It is a hybrid process where the model:
1. Performs internal neural computation
2. Generates human-readable reasoning steps
3. Uses those generated steps as input for future computation
The visible reasoning and the internal reasoning are related, but they are not necessarily identical.
---
## Key Analogy: Human Thinking Aloud
A useful analogy is a human solving a problem aloud on a whiteboard.
Writing intermediate steps can genuinely improve thinking by:
- structuring attention
- reducing mistakes
- externalizing partial results
- creating a scratchpad for future reasoning
However, the written derivation is not a perfect transcript of cognition.
Some reasoning still happens internally:
- intuitions
- subconscious pattern matching
- heuristics
- mental shortcuts
LLMs appear to behave similarly.
---
## Why “Think Step by Step” Improves Accuracy
### CoT Provides More Test-Time Compute
Transformers compute through token generation itself. Each generated token becomes part of the next input context:
> internal state → reasoning token → updated context → new internal state

Longer reasoning chains therefore give the model:
- more inference steps
- more opportunities for refinement
- iterative correction
This is often described as increasing **test-time compute**.
---
## CoT Creates a Scratchpad
Reasoning tokens externalize intermediate structure.
Example:
Without CoT:
```text
17 × 24 = ?
```
With CoT:
```text
17 × (20 + 4)
= 340 + 68
= 408
```

The model can then condition future computation on:
- decompositions
- partial results
- intermediate reasoning states
The generated text becomes part of the reasoning process itself.
---
## Two Intertwined Processes
It is helpful to think of CoT as involving two simultaneous processes:
### 1. Internal Neural Computation
This includes:
- activations
- attention patterns
- latent representations
- internal circuits

These are the actual computations occurring inside the network.
---
## 2. Human-Readable Reasoning
This is the visible chain-of-thought text:
- explanations
- intermediate reasoning
- verbalized logic
These traces are partially informative, but not guaranteed to fully reflect the true internal causal process.
---
## Important Insight: CoT Is Not Necessarily Faithful

A model may:
- produce correct answers with flawed reasoning
- produce convincing explanations after internally deciding the answer
- rely on shortcuts while verbalizing more principled reasoning
This is similar to humans giving post-hoc rationalizations.

Therefore:
> CoT can improve reasoning performance while still being partially unfaithful as an explanation of the true internal computation.

---
## Why Researchers Care About Activations
Some researchers argue:
> Monitoring outputs alone is insufficient.

Instead of only inspecting the model’s explanations, they want to inspect:
- hidden activations
- attention heads
- residual streams
- neuron outputs
- causal internal circuits

The goal is to understand:
- what actually drove the answer
- whether the model used shortcuts
- whether latent unsafe reasoning exists
- whether explanations are faithful
---
## Behavioral vs Mechanistic Interpretability

### Behavioral Interpretability
Focuses on:
- outputs
- explanations
- reasoning traces
- observed behavior

Question:
> “What did the model say?”

---
### Mechanistic Interpretability
Focuses on:
- activations
- circuits
- internal representations
- causal pathways

Question:
> “What computations actually occurred?”
---
## Main Conclusion
Chain-of-thought reasoning is both:
- a reasoning aid
- and a communication channel
The visible reasoning is not merely a report of computation; it also becomes part of the computation itself.
However, the visible reasoning is not guaranteed to be a faithful transcript of the model’s true internal processes.
A useful mental model is:
> LLMs are simultaneously “thinking internally” and “thinking out loud,” with those two processes continuously interacting but not perfectly aligned.

## Question
1. What does this mean for evaluation of LLM generated COT traces?
