# NLI-zero-shot-legal-questions-classification-
Repo for my final project before graduating from GOMYCODE for the "Introduction to Artificial Intelligence" 

# Dataset
The Belgian Statutory Article Retrieval Dataset (BSARD) is a French native dataset for studying legal information retrieval. BSARD consists of more than 22,600 statutory articles from Belgian law and about 1,100 legal questions posed by Belgian citizens and labeled by experienced jurists with relevant articles from the corpus.

The text in the dataset is in French, as spoken in Wallonia and Brussels-Capital region. The associated BCP-47 code is fr-BE.

The dataset was created mainly for document-retrieval: The dataset can be used to train models for ad-hoc legal information retrieval. Such model is presented with a short user query written in natural language and asked to retrieve relevant legal information from a knowledge source (such as statutory articles).

# My approach

Instead of using the dataset to do legal document retrieval i decided that i transform it to make it into an NLI dataset with the "questions" feature as a premise and create my own hypothesis for each question by using it's "category". This allows me to classify the questions into their categories by turning an NLI problem to a classification one using the zero-shot approach.

<img src="NLI zero shot.png" alt="Image Alt Text" width="800" height="300">

# Methodology
After transforming the BSARD i went to the classification modeling. I finetuned famous LLMs that have been pretrained for NLI tasks on either french texts or multilingual texts including french:

* camemBERT : "CamemBERT is a state-of-the-art language model for French based on the RoBERTa architecture pretrained on the French subcorpus of the newly available multilingual corpus OSCAR. We evaluate CamemBERT in four different downstream tasks for French: part-of-speech (POS) tagging, dependency parsing, named entity recognition (NER) and natural language inference (NLI)" Model's official website

* DistilCamemBERT : istillation version of the well named CamemBERT, a RoBERTa French model version, alias DistilCamemBERT. The aim of distillation is to drastically reduce the complexity of the model while preserving the performances. The proof of concept is shown in the DistilBERT paper and the code used for the training is inspired by the code of DistilBERT.

* mDeBERTa V3 : DeBERTa improves the BERT and RoBERTa models using disentangled attention and enhanced mask decoder. With those two improvements, DeBERTa out perform RoBERTa on a majority of NLU tasks with 80GB training data.

<img src="Diagramme NLI_zero-shot - Page 1.png" alt="Image Alt Text" width="900" height="500">



