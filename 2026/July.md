# MIT IMES Distinguished Speaker Series 2026: Geoffrey Hinton
Date of publish: 07/2026
Authors: Geoffrey Hinton
Tags: 

Talk link: 
Paper link: https://youtu.be/g6AwGpfE2b0
Related: 
## Main results
### Symbolic AI vs Biology-inspired AI
1. Former: meaning of a word comes from its relationships to other words. Need a relational graph. 
2. Latter: meaning of a word is a big set of semantic and syntactic features. 
### Unification of symbolic and Biology-inspired AI
1. Hinton (1985) learns a set of features for each word (semantic); learns how to make the features of all the previous words predict the features of the next word (relation). This unifies both AI theories.
2. instead of storing sentences or propositions, generate sentences by repeatedly predicting the next word.
3. relational knowledge resides in the way that features interact, not in static stored propositions.
4. One can get the features of a word by predicting the next word, also predict the next word by using the features. The weights/function is everything.
5. It is the **interaction** between the word embedding and NN weights that creates intelligence:
	1. **The Embedding (The "Data"):** As you noted, the word embedding represents the meaning of a word as a high-dimensional vector. These vectors are refined during training to capture semantic relationships. 
	2. **The Weights (The "Machinery"):** The weights are the fixed parameters of the network that define how those vectors are processed. They essentially store the "knowledge" of the system, determining how information is transformed, filtered, and passed through layers.
6. all LLMs are the descendent of that 1985 tiny LM; linguist are yet to find better models to explain human linguistic
### Words are like Legos
1. words are like high-dimensional Lego blocks that can model anything
2. each dimension is the activation level of a neuron that represents a feature
3. words have hands, and they can change form to work with each other (this is the forward pass through transformer layers)
