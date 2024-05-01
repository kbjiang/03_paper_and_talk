Date: 2023-12-29
Date of publish: 
Authors: Ekin Akyurek, Dale Schuurmans, Jacob Andreas, Tengyu Ma, Denny Zhou
Tags: #ICL #UnderstandTransformers 

Talk link: https://youtu.be/UNVl64G3BzA
Paper link: [[2211.15661] What learning algorithm is in-context learning? Investigations with linear models (arxiv.org)](https://arxiv.org/abs/2211.15661)
Related: 
	- [[01a-In-Context Learning A Case Study of Simple Function Classes]]

## Main results
- Explored what learning algorithms a Transformer can implement
	- Proved that Transformers can simulate classical learning algorithms, i.e., *Gradient descent* and *closed-form Ridge*.
- Examine learned algorithm computationally
- Examine learned algorithm algorithmically

## Details
1. Theoretically proved that Transformers can *simulate* classical learning algorithms
	1. Classical learning algorithms for linear regression
		1. ![[Pasted image 20240214212125.png|400]]
	2. Arithmetic primitives for forementioned algorithms
		1. ![[Pasted image 20240214212350.png|400]]
		2. *All can be implemented by a single transformer decoder layer*
			1. E.g., Affine by FF layers, Move by self-attention layers
	3. Example of implementing 1-step SGD with decoder layers. The two images show the same operations in different views.
		1. ![[Pasted image 20240214213234.png|900]]
		2. ![[Pasted image 20240214213342.png|900]]
	4. Examine learned algorithm computationally
		1. Figure 1 in paper shows Transformer ICL on noiseless linear regression agree closely with ordinary least squares. This is similar to results in Garg et al.
		2. Figure 2 in paper shows that with different noise level in data, Transformer ICL implements Ridge regressor with different parameters. This means it "always" learns the *Bayes Optimal* algorithms. ![[Pasted image 20240214213923.png|900]]
	5. Examine learned algorithm algorithmically
		1. Probing $X^TY$ and $w_{\text{OLS}}$ at different layers. By doing so, "we can gain insight into ICL by inspecting learners’ intermediate states: asking *what* information is encoded in these states, and *where*." 
		2. ![[Pasted image 20240214214325.png|900]]
## Main takeaways

## Reference
1. Linear classifier probes [1610.01644.pdf (arxiv.org)](https://arxiv.org/pdf/1610.01644.pdf)
	1. Also https://youtu.be/HJn-OTNLnoE
	2. Basically one uses *features* at intermediate layers as input and train a linear classifier toward the label. The better the classifier, the more confident we become about the feature is learnt at that layer.
