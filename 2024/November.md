## A brief summary of language model finetuning
Tags: #LLM #finetune
Authors: Cameron R. Wolfe
Paper link: https://stackoverflow.blog/2024/10/31/a-brief-summary-of-language-model-finetuning
Talk link: 
Related: 
### Why interesting
### Ideas/conclusions
- Most knowledge from an LLM comes from pretraining.
- We can perform fine tuning in the form of continued pretraining to expose the LLM to more (and new) data/knowledge.
- Alignment-focused objectives can be achieved via fine tuning (SFT) on small, high-quality datasets. We don’t need tons of data to learn the style or format of output, only to learn new knowledge.

## How Transformers Learn Causal Structure with Gradient Descent^transformer-causal
Tags: #UnderstandTransformers 
Authors: Jason Lee
Paper link: 
Talk link: https://youtu.be/xlWBsISnaRA
Related: 
### Why interesting
### Ideas/conclusions

### References
1. https://transformer-circuits.pub/2021/framework/index.html


## UNDERSTANDING DEEP LEARNING REQUIRES RETHINKING GENERALIZATION
Tags: #DL-fundation  #DL-generalization 
Authors: Chiyuan Zhang et.al.
Paper link: https://arxiv.org/pdf/1611.03530
Talk link: 
Related: 
### Why interesting
### Ideas/conclusions
1. Optimization does not mean generalization
2. Regularization is helpful, but not essential to generalization
3. Good exploration on SGD leading to minimal norm solution and decent generalization

### References
1. [[October#**Reconciling modern machine-learning practice and the classical bias–variance trade-off**]]
2. [Implicit Regularization in Matrix Factorization](https://dl.acm.org/doi/pdf/10.5555/3295222.3295363) 
	1. Ref 17 and [video](https://youtu.be/gh9vrvLx7Mo)
	2. Nathan Srebro is the man!
