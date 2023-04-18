- Paper URL https://arxiv.org/pdf/2210.02441.pdf
- [Gist](https://github.com/labmlai/annotated_deep_learning_paper_implementations/blob/master/labml_nn/distillation/readme.md): The output probabilities of a trained model give more information than the labels because it assigns non-zero probabilities to incorrect classes as well. These probabilities tell us that a sample has a chance of belonging to certain classes. For instance, when classifying digits, when given an image of digit _7_, a generalized model will give a high probability to 7 and a small but non-zero probability to 2, while assigning almost zero probability to other digits. Distillation uses this information to train a small model better.


## Notes
1. Is it Q&A only? We can phrase almost everything into a question though.
2. . Ensemble of imperfect prompts. What about the cost?
3. Table 1: when AMA with GPT-J-6B underperforms comparing to GPT-3, it does so by a lot.
4. "LLMs are brittle <plain>&mdash;</plain> small changes to the prompt result in large performance virations."
5. Three things they aim to do
	1. prompts effective across tasks and models type/size.
	2. scalably reformat taks inputs to forementioned prompts
	3. aggregate predictions (weak supervision instead of majority vote)
6. "recovers dependencies among prompts"?
7. Two key components: 
	1. collection of prompts $\mathrm{P}$ and aggregator $\phi$
	2. single prompt $p(x)$ where $x$ is context
8. open-ended QA prompt vs restrictive prompt. Former is more effective because.. page 5.
9. "We find that using an open-ended prompt that asks the LM to generate relevant context, and then prompting the model to answer the original question using the generated context is effective."