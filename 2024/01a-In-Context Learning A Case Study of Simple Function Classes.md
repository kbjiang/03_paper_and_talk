Date: 2023-12-29
Date of publish: 2022
Authors: Shivam Garg, Dimitris Tsipras, Percy Liang, Gregory Valiant
Tags: #ICL #UnderstandTransformers 

Talk link: https://youtu.be/DiJsg93zQDc
Paper link: [[2208.01066] What Can Transformers Learn In-Context? A Case Study of Simple Function Classes (arxiv.org)](https://arxiv.org/abs/2208.01066)
Related: 
	- [[01b-What Learning Algorithm is In-Context Learning]]

## Main results
1. *Empirically* proved that *Transformers can learn simple functions in-context*.
2. Proposed an interpretable and theoretically amenable setting for understanding ICL in transformers
## Details
1. Simplify the experiment to *train a model to in-context learn a certain function class*
2. Training Data
	1. Input $x_i$ is sampled from some iid
	2. Function $f$ is a given class of function (e.g. linear $y=w x$) whose parameter (e.g. $w$) is sampled from some iid
	3. A single prompt: $(x_1, f(x_1), ..., x_k, f(x_k), x_{\text{query}})$. 
		1. The form of $f$ is unknown to the model.
	4. ![[Pasted image 20240213170931.png|700]]
3. Training Objective: $\text{MSE}(y, f(x_{\text{query}}))$
4. Results
	1. Transformer learns simple functions well.
		1. It appears to learn the best regressor given data. E.g., It learns Least Square with full rank data, but Lasso with sparse linear data.
		2. The reference functions are trained using the same datapoints in the prompts, but *with predefined function form*! ![[Pasted image 20240213173520.png]]
	2. The learned algorithm seems to be robust
		1. The "double descent" is a hallmark of least square learner. Transformer showing the same behavior can be evidence that it really learned least square.
		2. ![[Pasted image 20240213174239.png|700]]
## My takeaways
1. Technically speaking, all large enough models with enough training should be able to do in-context learning. 
	1. Paper and following research focused on Transformer because it is most efficient.
2. This falls under meta-learning.
3. The inductive biases of a linear model is learned, not predefined. 
	1. The Transformer has to start with the whole hypothesis space.
	2. Analogous to CNN vs VIT.

## Reference
1. Double descent [*1912.07242.pdf (arxiv.org)](https://arxiv.org/pdf/1912.07242.pdf)
2. Meta learning [Meta-Learning: Learning to Learn Fast | Lil'Log (lilianweng.github.io)](https://lilianweng.github.io/posts/2018-11-30-meta-learning/)
3. Bayesian Linear Regression [CSC 411 Lecture 19: Bayesian Linear Regression (toronto.edu)](https://www.cs.toronto.edu/~rgrosse/courses/csc411_f18/slides/lec19-slides.pdf)