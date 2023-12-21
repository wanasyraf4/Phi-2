# Phi-2

Phi-2 is a 2.7 billion-parameter language model that demonstrates outstanding reasoning and language understanding capabilities, showcasing state-of-the-art performance among base language models with less than 13 billion parameters.Phi models aims to answer this question by training SLMs that achieve performance on par with models of much higher scale (yet still far from the frontier models). 


# Key Insights Behind Phi-2
The massive increase in the size of language models to hundreds of billions of parameters has unlocked a host of emerging capabilities that have redefined the landscape of natural language processing. A question remains whether such emergent abilities can be achieved at a smaller scale using strategic choices for training, e.g., data selection.

![image](https://github.com/wanasyraf4/Phi-2/assets/107595740/bd1a532c-6146-4d68-b70c-e9b6569448f3)
*Figure 1. Comparison between Phi-2 (2.7B) and Phi-1.5 (1.3B) models. All tasks are evaluated in 0-shot except for BBH and MMLU which use 3-shot CoT and 5-shot, respectively.*

# Training Details
Phi-2 is a Transformer-based model with a next-word prediction objective, trained on 1.4T tokens from multiple passes on a mixture of Synthetic and Web datasets for NLP and coding. The training for Phi-2 took 14 days on 96 A100 GPUs. Phi-2 is a base model that has not undergone alignment through reinforcement learning from human feedback (RLHF), nor has it been instruct fine-tuned.  Despite this, it is observed as better behavior with respect to toxicity and bias compared to existing open-source models that went through alignment **(see Figure 2)**.

![image](https://github.com/wanasyraf4/Phi-2/assets/107595740/f84b0588-a2b8-4f86-a4b4-333ba91e3b65)
*Figure 2. Safety scores computed on 13 demographics from ToxiGen. A subset of 6541 sentences are selected and scored between 0 to 1 based on scaled perplexity and sentence toxicity. A higher score indicates the model is less likely to produce toxic sentences compared to benign ones*

# Phi-2 Evaluation
With only 2.7 billion parameters, Phi-2 surpasses the performance of Mistral and Llama-2 models at 7B and 13B parameters on various aggregated benchmarks. Notably, it achieves better performance compared to 25x larger Llama-2-70B model on muti-step reasoning tasks, i.e., coding and math. Furthermore, Phi-2 matches or outperforms the recently-announced Google Gemini Nano 2, despite being smaller in size.
<img width="497" alt="image" src="https://github.com/wanasyraf4/Phi-2/assets/107595740/5f36423d-af5e-4d3a-ba62-dccc21b102cc">


# Reference
Microsoft research, (2023) Phi-2: The surprising power of small language models, https://www.microsoft.com/en-us/research/blog/phi-2-the-surprising-power-of-small-language-models/
