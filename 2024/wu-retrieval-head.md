Date: 2024-04-30
Date of publish: 2024
Authors: Wenhao Wu et,al.
Tags: #UnderstandTransformers 

Talk link: 
Paper link: [2404.15574 (arxiv.org)](https://arxiv.org/pdf/2404.15574)
Related: 

## Main results
1. Demonstrated a special set of *attention heads* are responsible for information retrieval, i.e., *retrieval heads*
2. Heuristically proved that retrieval heads are
	1. *universal*: all explored models (decoder) with long-context capability have a set of retrieval heads
	2. *sparse*: less than 5$\%$ of the attention heads are retrieval
	3. *intrinsic*: retrieval heads already exist in models pretrained with short context. When extending the context length to 32-128K by continual pretraining, it is still the same set of heads that perform information retrieval.
	4. *dynamically activated*: retrieval heads always attend to the required information no matter how the context is changed. The rest of the retrieval heads are activated in different contexts.
	5. *causal*: completely pruning retrieval heads leads to failure in retrieving relevant information and results in hallucination, while pruning random non-retrieval heads does not affect the model’s retrieval ability.
## Details
1. Definition of retrieval heads
	1. *Attention heads* that implement the conditional copy-paste algorithm. 
		1. Notice how this relates to the idea of Transformers being universal function learner. Agrees with ICL papers [[[01a-In-Context Learning A Case Study of Simple Function Classes]], [[01b-What Learning Algorithm is In-Context Learning]]]
		2. More specifically, *attention layers* for algorithm implementation [Ref 1] while *FNN layers* for storing knowledge [Ref 2]. 
	2. ![[Pasted image 20240430213035.png|1000]]
2. Test detail
	1. In tests, *attention heads* with retrieval score higher than preset threshold is considered retrieval heads.
	2. First used *Needle-in-a-Haystack*, then more realistic use cases.
	3. result figures
		1. ![[Pasted image 20240430214653.png|1000]]
		2. ![[Pasted image 20240430214614.png|1000]]
		3. COT is heavily influenced by retrieval heads![[Pasted image 20240430215603.png|1000]]
## My takeaways

## Reference
1. In-context Learning and Induction Heads [2209.11895 (arxiv.org)](https://arxiv.org/pdf/2209.11895)
2. Transformer Feed-Forward Layers Are Key-Value Memories [2012.14913 (arxiv.org)](https://export.arxiv.org/pdf/2012.14913)