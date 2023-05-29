# Large Language Model (LLM)

This is a survey of Large Language Models (LLM).

---------------------------------------
### Models
* [GTP4ALL](https://github.com/nomic-ai/gpt4all) an ecosystem of open-source chatbots trained on a massive collections of clean assistant data including code, stories and dialogue.

### Improving LLM
* [Chain-of-Thought Prompting Elicits Reasoning in Large Language Models](https://arxiv.org/pdf/2201.11903.pdf)

### Multimodal LLM
* [AudioGPT](https://github.com/AIGC-Audio/AudioGPT) [paper](https://arxiv.org/abs/2304.12995)
* [Otter](https://github.com/Luodian/Otter) based on Flamingo
* [Llama Adapter v2](https://github.com/ZrrSkywalker/LLaMA-Adapter) [paper](https://arxiv.org/abs/2304.15010)
* [PaLM-E: An Embodied Multimodal Language Model](https://palm-e.github.io/)
* [Flamingo: a Visual Language Model for Few-Shot Learning](https://arxiv.org/abs/2205.01068)
* [SimVLM: Simple Visual Language Model Pretraining with Weak Supervision](https://arxiv.org/abs/2108.10904)

### Domain-specific LLM
* Minecraft -> [VOYAGER: An Open-Ended Embodied Agent with Large Language Models](https://voyager.minedojo.org/assets/documents/voyager.pdf)
* Coding -> [Teaching Large Language Models to Self-Debug](https://arxiv.org/abs/2304.05128)
* Biology -> [GeneGPT](https://arxiv.org/abs/2304.09667) Teaching Large Language Models to Use NCBI Web APIs
* Finance -> [BloombergGPT](https://arxiv.org/abs/2303.17564) A Large Language Model for Finance
* Medical -> [ChatDoctor](https://arxiv.org/abs/2303.14070) Medical Chat Model Fine-tuned on LLaMA Model using Medical Domain Knowledge

### LLM
* [Finetuned Language Models Are Zero-Shot Learners](https://arxiv.org/abs/2109.01652)
* [Gpt-neox-20b: An open-source autoregressive language model](https://arxiv.org/abs/2204.06745)
* [Scaling Language Models: Methods, Analysis & Insights from Training Gopher](https://arxiv.org/abs/2112.11446)
* [Training language models to follow instructions with human feedback](https://proceedings.neurips.cc/paper_files/paper/2022/hash/b1efde53be364a73914f58805a001731-Abstract-Conference.html)
* [Domain-specific language model pretraining for biomedical natural language processing](https://dl.acm.org/doi/abs/10.1145/3458754?casa_token=P-T8trc32d8AAAAA:94zBcf_gj0Ht5jLClGczKrM22PkBDJGvBHtYgI3P76BJHqz8OnfZsi8d7XAyfV4Nm0YbQsXtKFrf)
* [Using DeepSpeed and Megatron to Train Megatron-Turing NLG 530B, a Large-Scale Generative Language Model](https://arxiv.org/abs/2201.11990)
* [Training Compute-Optimal Large Language Models](https://arxiv.org/abs/2203.15556)

### NLI
* [LLM Serve as A Database Interface](https://arxiv.org/pdf/2305.03111.pdf)
* [DIN-SQL: Decomposed In-Context Learning of Text-to-SQL with Self-Correction](https://arxiv.org/pdf/2304.11015.pdf)
* [Demonstration of InsightPilot: An LLM-Empowered Automated Data Exploration System](https://arxiv.org/pdf/2304.00477.pdf)
* [Data BIRD-SQL](https://bird-bench.github.io/)
  
## Understanding
* [Evidence of Meaning in Language Models Trained on Programs](https://arxiv.org/abs/2305.11169)
* [Eight Things to Know about Large Language Models](https://arxiv.org/abs/2304.00612)
* [Are Emergent Abilities of Large Language Models a Mirage](https://arxiv.org/pdf/2304.15004.pdf)

## Dataset

* [PILE](https://pile.eleuther.ai/) 800G text Pile is a large, diverse, and open-sourced dataset created by concatenating over 800 public datasets. The Pile dataset includes a wide range of text, including books, scientific articles, news articles, and web pages. The authors used the Pile dataset to fine-tune the GPT-NeoX-20B model.

* [Github](https://github.com/kojima-takeshi188/zero_shot_cot) (Experiments used publicly available datasets except for “Last
Letters” and “Coin Flip” datasets. We created these two datasets.
(*1) N : Number, M : Pick up one from multiple choices, Y : Answer Yes or No, F : Free Format.
(*2) Average number of words in questions texts.) 
 
* [Github](https://github.com/openai/code-align-evals-data) (Training dataset was collected in May 2020 from 54 million public software repositories hosted on GitHub, containing 179 GB of unique Python files under 1 MB. We filtered
out files which were likely auto-generated, had average line
length greater than 100, had maximum line length greater
than 1000, or contained a small percentage of alphanumeric
characters. After filtering, our final dataset totaled 159 GB.)

* [GLUE Github](https://paperswithcode.com/dataset/glue) The General Language Understanding Evaluation (GLUE) benchmark consists of a collection of nine different natural language understanding tasks, including sentiment analysis, natural language inference, and question answering. The authors use this dataset to evaluate the performance of their models on a range of different tasks.
* SuperGLUE: The SuperGLUE benchmark is an extension of the GLUE benchmark, consisting of a set of eight more difficult natural language understanding tasks. The authors use this dataset to evaluate the performance of their models on more challenging tasks.
* SQuAD: The Stanford Question Answering Dataset (SQuAD) consists of a set of Wikipedia articles and associated questions, where the goal is to answer the questions based on the information in the articles. The authors use this dataset to evaluate the performance of their models on question answering tasks.
* TriviaQA: The TriviaQA dataset is another question answering dataset, but with a focus on more difficult questions that require a deeper understanding of the text. The authors use this dataset to evaluate the performance of their models on more challenging question answering tasks.
* OpenAI Codex: The OpenAI Codex dataset consists of a large collection of code snippets and natural language descriptions of what the code does. The authors use this dataset to evaluate the performance of their models on code generation tasks.

* CONCEPTUAL CAPTIONS [Dataset](https://ai.google.com/research/ConceptualCaptions/) The authors use the Conceptual Captions dataset, is a large-scale image captioning dataset, which consists of over 3.3 million images with corresponding captions. The images cover a wide range of topics and come from a variety of sources, including Flickr and Google Images. The captions are generated by annotators, who are asked to describe the content of the image in a natural language sentence.
For their experiments, the authors use a preprocessed version of the Conceptual Captions dataset, which includes only the images and captions that contain at least one noun and one verb. The resulting dataset contains around 2.8 million image-caption pairs.

* [Paper](https://arxiv.org/pdf/2204.06745.pdf) The paper presents GPT-NeoX-20B, an open-source autoregressive language model with 20 billion parameters. The authors used a variety of datasets to train and evaluate the model, including:
* Common Crawl: The Common Crawl dataset is a large collection of web pages that have been crawled and archived. The authors used the Common Crawl dataset to pretrain the GPT-NeoX-20B model.

* WMT14: The WMT14 dataset is a collection of parallel corpora for machine translation, consisting of English and German text. The authors used the WMT14 dataset to evaluate the performance of the GPT-NeoX-20B model on machine translation tasks.
* LAMBADA: The LAMBADA dataset is a language modeling benchmark where the goal is to predict the final word of a sentence given the preceding words. The authors used the LAMBADA dataset to evaluate the GPT-NeoX-20B model's ability to handle long-term dependencies.

* PubMed: PubMed is a large biomedical literature database maintained by the US National Library of Medicine. The authors used PubMed to create a biomedical language model.
* Wikipedias: The authors used Wikipedias in multiple languages to train Gopher language models for multiple languages.
* OpenWebText: OpenWebText is a large dataset of web pages, similar to Common Crawl, that has been specifically curated for use in language modeling. The authors used * OpenWebText for both pretraining and fine-tuning Gopher.
* Reddit: Reddit is a social media platform with a large amount of user-generated text. The authors used Reddit to fine-tune Gopher on conversational and informal text.

* COIN [Github](https://github.com/coin-dataset/annotations) The authors created a new dataset called COIN, which stands for "Collaborative Instruction and Navigation." COIN dataset provides a novel task of training language models to follow natural language instructions in complex environments, and enables the evaluation of language models' ability to understand and navigate in such environments based on natural language instructions..The COIN dataset consists of 13,003 natural language instructions paired with 133,995 navigation environments. The navigation environments are 2D maps with objects that the language models must navigate to in order to follow the instructions correctly. The objects in the environment are categorized into three types: targets (objects that the language model should navigate to), distractors (objects that should be avoided), and neutral objects (objects that are not relevant to the instruction).

* [Medical](https://scholar.google.com/scholar_url?url=https://dl.acm.org/doi/pdf/10.1145/3458754%3Fcasa_token%3D_ydLimYqoNwAAAAA:wDDbcCGWdjFXQ4fNLoFdKQdzC5ZhdFDcnoGbTHt6_Tq88R69paTWm8gGcqFjFzCKUZErhphYpOpB&hl=en&sa=T&oi=ucasa&ct=ucasa&ei=7stBZJ3CI_KP6rQPzs6N8A0&scisig=AJ9-iYsjBhEEv8t8UG0jE0Zf1EWz) The authors of the paper do not mention any specific dataset used for their experiments. However, they do mention that they evaluate their method on several benchmark datasets in biomedical NLP, including the i2b2 2010 challenge dataset, the SemEval-2014 Task 7 dataset, and the ShARe/CLEF eHealth Evaluation Lab 2014 dataset. These datasets contain a variety of tasks related to clinical text analysis, such as named entity recognition, relation extraction, and classification.

[Flamingo](https://palm-e.github.io/assets/palm-e.pdf) 
* Omniglot: a handwritten character recognition dataset, which contains 1623 different handwritten characters from 50 different alphabets.
* Mini-ImageNet: a subset of the ImageNet dataset, which contains 100 classes with 600 images each.
* FewRel: a few-shot relation extraction dataset, which contains sentences and corresponding entity pairs, and the goal is to predict the relation between them.
* Text-to-SQL: a dataset for translating natural language questions into SQL queries, which contains a small number of annotated examples for each query type.


* WikiText-103


## Contact

Wenlu Wang
wenlu.wang.1@gmail.com
