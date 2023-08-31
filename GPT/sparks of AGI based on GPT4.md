1. GPT4 shows mastery of natural language. E.g., letters supporting Electron as POTUS candidate (Fig 2.3).
2. GPT4 shows some common sense. E.g., stacking items (Fig 1.7)
3. GPT4 has some grasp of geometric concepts. E.g., produce TikZ code to draw person from letters (Fig 2.5). Even though initial instructions, such as $O$ is the face and $Y$ is the torso and arm, is needed, the model has to know what a person looks like, what letters look like, how to position letters so that they resembles a person. Note this version of GPT is trained on *text exclusively*.
	1. it's possible that it's written somewhere that it goes 'head, torso and legs from top to bottom' somewhere and GPT4 read it.
4. Sec 4.1.3, GPT4 lacks critical reasoning, and the authors suggest two reasons for it:
	1. while questions and solutions are abundant, *thinking process* is lacking in training data
	2. *limitation to try things and backtrack* is inherent to the next-word-prediction paradigm
	3. see also Section 8
5. Fig 4.5, GPT4 is capable of mathematical modeling: flow of logic/reasoning, list assumptions and data. Is there something other than statistical next-word estimation?
	1. btw the way it estimates # of A100 from Nvidia's revenue was interesting
6. Fig 5.4, GPT4 use tools, email and calendar, to communicate with others and make appointments.
7. Fig 5.5, it's scary good. Acting just like a human.
8. Fig 5.7, see how GPT4 was not able to rethink, but was able to spot its error after being prompted again.

### Interaction with humans
1. *Theory of mind*: what does another entity think.
2. Fig 6.5, a challenging family scenario. GPT-4 makes suggestions like a mature and sophisticated human.
3. Ability to explain oneself is a key aspect of intelligence and GPT4 possess such ability. 
	1. *output consistent*: explanations are consistent with predictions given input/context; even with false/counterfactrual input, GPT-4 explains its false/conterfactural output logically.
	2. *process consistent*: consistency between the explanation and model's predictions with future inputs. Fig 6.10.

[talk](https://youtu.be/qbIk7-JPB2c) by leading author. [Here](https://youtu.be/qbIk7-JPB2c?t=2386) is an interesting example and insight. He argues how it is possible for future GPT to overcome initial mistakes through reasoning, i.e., overcome the 'most likely next token'.

### Discriminative capabilities
1. Sec 7.2.1 on why metrics like ROUGE is not sufficient

seven