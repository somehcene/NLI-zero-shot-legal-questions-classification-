# NLI-zero-shot-legal-questions-classification-
Repo for my final project before graduating from GOMYCODE for the "Introduction to Artificial Intelligence" 

# Dataset
The Belgian Statutory Article Retrieval Dataset (BSARD) is a French native dataset for studying legal information retrieval. BSARD consists of more than 22,600 statutory articles from Belgian law and about 1,100 legal questions posed by Belgian citizens and labeled by experienced jurists with relevant articles from the corpus.

The text in the dataset is in French, as spoken in Wallonia and Brussels-Capital region. The associated BCP-47 code is fr-BE.

The dataset was created mainly for document-retrieval: The dataset can be used to train models for ad-hoc legal information retrieval. Such model is presented with a short user query written in natural language and asked to retrieve relevant legal information from a knowledge source (such as statutory articles).

# My approach

Instead of using the dataset to do legal document retrieval i decided that i transform it to make it into an NLI dataset with the "questions" feature as a premise and create my own hypothesis for each question by using it's "category". This allows me to classify the questions into their categories by turning an NLI problem to a classification one using the zero-shot approach.

![Image Alt Text](classes.png)
