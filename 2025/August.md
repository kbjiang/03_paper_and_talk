## Why Do We Need Weight Decay in Modern Deep Learning?
Date of publish: Nov 2024
Authors: Francesco D’Angelo∗ , Maksym Andriushchenko,∗ Aditya Varre, Nicolas Flammarion 
Tags: #weight-decay #SGD 

Talk link:
Paper link:  https://arxiv.org/pdf/2310.04415
Related: 
### Main results
1. Examined the effect of WD (weight decay) in different scenarios, specifically,
	1. over-training: such as multi-pass vision tasks; WD "modifies the optimization dynamics enhancing the ever-present implicit regularization of SGD via the loss stabilization mechanism."
		1. did not read this part
	2. *under-training*: such as single-pass LLM; WD "balances the *bias-variance* tradeoff in stochastic optimization leading to lower training loss and improved training stability" 
	3. Overall: "weight decay is *never* useful as an explicit regularizer but instead changes the training dynamics in a desirable way."
		1. against common belief

### Weight decay in the under-training regime (section 3)
1. Two key effects
	1. better optimization of the training loss
	2. prevention of loss divergences under `bfloat16` weight precision
2. better optimization
	1. 