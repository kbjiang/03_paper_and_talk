## **Reconciling modern machine-learning practice and the classical bias–variance trade-off**
Tags: #DL-fundation #Math-heavy #DL-generalization
Authors: Mikhail Belkin, Daniel Hsu, Siyuan Ma, and Soumik Mandal
Talk link: 
Paper link: https://www.pnas.org/doi/10.1073/pnas.1903070116
Related: 
### Why interesting
### Ideas
1. overfitting
2. inductive biases ^inductive-bias
	1. *In this paper, we have dealt with several types of methods for choosing interpolating solutions. For random Fourier features, solutions are constructed explicitly by minimum norm linear regression in the feature space. As the number of features tends to infinity they approach the minimum functional norm solution in the reproducing kernel Hilbert space, a solution which maximizes functional smoothness subject to the interpolation constraints. For neural networks, the inductive bias owes to the specific training procedure used, which is typically SGD. When all but the final layer of the network are fixed (as in RFF models), SGD initialized at zero also converges to the minimum norm solution. While the behavior of SGD for more general neural networks is not fully understood, there is significant empirical and some theoretical evidence (e.g., ref. [16](https://www.pnas.org/doi/10.1073/pnas.1903070116#core-r16)) that a similar minimum norm inductive bias is present.*
3. 
![[Pasted image 20241031143056.png|900]]  



## **Towards Understanding Deep Classifiers though Neural Collapse**
Tags: #DL-fundation #Math-heavy #Neural-collapse #SGD
Authors: Mengjia Xu, Akshay Rangamani, Qianli Liao, Tomer Galanti, and Tomaso Poggio
Talk link: https://youtu.be/CcbOoxcqZes
Paper link: https://spj.science.org/doi/epdf/10.34133/research.0024
Related: 
### Why interesting
### Ideas
1. Neural collapse
	![[Pasted image 20241027164227.png|600]]
2. SGD and low-rank bias

### References
1. [Gerard Ben Arous Colloquium on stochastic gradient descent in high dimensions](https://youtu.be/T78S9FOEg50)
	