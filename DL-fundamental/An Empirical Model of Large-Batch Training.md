Date of publish: Dec 2018
Authors: Sam McCandlish, Jared Kaplan, Dario Amodei
Tags: #batch-size #SGD #loss 

Talk link:
Paper link:  [1812.06162](https://arxiv.org/pdf/1812.06162)
Related:
### Main results
1. The loss *landscape* is over model parameters
	The “landscape” is defined **over the parameters** of the model (e.g., weights $\theta$.)  
	Formally, we can write:
		$L(\theta) = \mathbb{E}_{x \sim p_{\text{data}}}[\ell(x; \theta)]$
	- This represents the **true loss** (or population risk). Each point of $\theta$ is defined by the population of data $x$.
	- However, we can only have *sample* or *batch* of $x$ therefore our loss $L$, as well as gradient $g = \nabla_{\theta}(L)$, are only estimated, with variance and bias, whose magnitude is associated with batch size.
2. Gradient and batch size (SGD)-section 2.1
	1. "When we perform an SGD update with a finite batch size, we’re approximating the gradient to this true loss."
	2. "When the batch size is very small, the approximation will have very high variance, and the resulting gradient update will be mostly noise... "
	3. "By contrast, when the batch size is very large, the batch gradient will almost exactly match the true gradient..."
3. Trade-off between training time and compute cost is controlled by batch size. 
	1. 'Initially, we can increase the batch size without much increase in total computation, then there is a “turning point” where there is a substantive tradeoff between the two, and finally when the batch size is large we cannot make further gains in training time.' ![[Pasted image 20251029221058.png]]
4. Critical batch size
	1. Beyond the perfect scaling region, the gain in training time is diminishing. One might as well spend money on things other than increasing batch size. ![[Pasted image 20251029224623.png|500]]
		1. When $B$ is small $G_{\text{est}}$ is less likely to align with true gradient $G$, therefore training should be less aggressive, i.e. smaller $\epsilon_{\text{opt}}$; when $B$ is large $G_{\text{est}}$ is close to true $G$ but increase of $\epsilon_{\text{opt}}$ is slow now.
		2. Size of learning rate  is a surrogate of training time, the bigger the faster; $\epsilon_{\text{max}}$ is the $\epsilon_{\text{opt}}$ when we have noiseless true gradient.
	2. Smaller the loss target, bigger the critical batch size. E.g., at later stage of training, can increase batch size. ![[Pasted image 20251029225005.png|500]]
### Related
1. [[02_study/01-Course-study/stanford-cs336/notes#Data parallel]]