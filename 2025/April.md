## Transformers without Normalization
Date of publish: March 2025
Authors: Shivam Garg, Dimitris Tsipras, Percy Liang, Gregory Valiant
Tags: #DL-fundation #Transformers 

Talk link: 
Paper link: https://arxiv.org/pdf/2503.10622
Related: 
### Main results
1. 

## On the Biology of a Large Language Model
Date of publish: March 2025
Authors: Anthropic
Tags: #Transformers #LLM

Talk link: 
Paper link: https://transformer-circuits.pub/2025/attribution-graphs/biology.html
Related: 


## Llama 4 Deep Dive: Why Meta’s Latest Models Change Everything \[Breakdowns\]
Date of publish: April 2025
Authors: Devansh
Tags: #Transformers #LLM 

Talk link: 
Paper link: https://artificialintelligencemadesimple.substack.com/p/llama-4-deep-dive-why-metas-latest?utm_source=substack&utm_medium=email#media-aadf8b64-14d7-47ea-86df-41eafac81702
Related: 
### Main results
1. Mostly covered the four trends Llama 4 adopted. See 'deep dive'
### Deep dive on four trends
1. MOE
	1. The selection is happening at token level
		1. ![[Pasted image 20250406205647.png|600]]
2. Native multimodality and early fusion
	1. *Native* as opposed to *bolted-on*.
	2. "This **cross-modal attention** allows for a much deeper level of grounding and reasoning than possible with separate models."
	3. ![[Pasted image 20250406205730.png|600]]
3. Long RoPE
	1. interleaving RoPE and NoPE
4. Revamped Post-training
	1. only does *light* SFT
		1. to not stifle a model's exploratory potential during RL.
		2. focus on challenging, high-signal data to prevent over-fitting simple patterns
			1. clustering data points, and those farthest away from any centroid are potentially the most challenging ones.
	2. Intensive online reinforcement learning (main part)
	3. light DPO
	4. ![[Pasted image 20250406205832.png|600]]