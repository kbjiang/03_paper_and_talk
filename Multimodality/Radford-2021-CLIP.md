### Title: Learning Transferable Visual Models From Natural Language Supervision

### Big idea
1. Natural language as labels, as opposed to 1-in-N labels (just integers really, not even words), provides a lot of nuances about the image and enables much more *nuanced/accurate/robust* representations of image therefore better transferability. 

### Pre-training
1. Idea: which caption goes with which image
	 ![[Pasted image 20231208180019.png]]
 2. Fig 2. LM vs BOW, predictive vs comparative objectives. For efficiency purpose

### My takeaways
1. *NL supervision is learning an open set of visual concepts from natural language*
	1. free of categorical annotation (e.g., ImageNet) $\rightarrow$  easier to gather large training set--Internet is filled with image with natural language caption.
	2. connects image representation to language $\rightarrow$  more flexible/robust at zero-shot transfer
2. Why NL supervision, as opposed to 1-in-N label, is better at transfer?
	1. Context resolves polysemy. E.g., "construction crane" vs "crane"
	2. Detailed description is more accurate: e.g., "a dog sitting on a *table*." or "a *photo* of a dog" vs "dog". 
	3. Think of NL as a "spectrum" of labels while 1-in-N label throw away a lot of details in image. Like not all dogs are the same.
3. *Question*: How do we know the robustness in transferability is from multi-modality, but not large training dataset?
	1. E.g., Fig 13 'banana in sketch'. 
		1. If ImageNet has both 'banana' and 'sketch' classes (?), would it do better?
		2. CLIP could have understand 'sketch' somewhere else, e.g. 'a sketch of a man', then leverage that understanding when see a sketch of a banana.
	2. I think it's not about the text modality, it's about the dense labeling it brings about. It's embedding (NL) vs integer (1-in-N)

### Resources
1. Detailed walk-through [Video](https://youtu.be/OZF1t_Hieq8)
2. OpenAI [post](https://openai.com/research/clip) 
### Terminology
1. bag-of-words (BOW)
	1. BOW vs Continuous BOW (CBOW)
		1. BOW: think of occurrence matrix, one-hot vector and TF-IDF, no semantic. 
			1. “This is good” and “Is this good” have same vector, "an old car" and "a 2nd-hand vehicle" are unrelated.
		2. CBOW: think of dense vector and word2vec, a little semantic
		3. Both are static, as opposed to BERT encoding.
	2. It is 3x efficient than "transformer LM" as shown in Fig. 2. It is because the latter does autoregressive generation.
2. Linear probing: 
	1. Add and finetune a linear Softmax layer on frozen pre-trained model.