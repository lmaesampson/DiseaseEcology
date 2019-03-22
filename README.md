# DiseaseEcology
Can we define the field of disease ecology? Using natural language processing? We can sure try!

**Project Overview**

The field of disease ecology is both new and inherently interdisciplinary, and is thus difficult to define. Without a definition of what exactly disease ecology *is*, it is also difficult to design coursework or determine what skills a person should master in order to be successful in the field. 

To determine what is and is not disease ecology, we decided to combine two approaches: a survey in which we ask disease ecologists to define themselves, and an NLP analysis of the corpus of disease ecology literature to see what disease ecologists are researching. 

**Code**

Contains code for cleaning and analyzing the corpus datasets.

*Cleaning*

After pre-processing, which is basically turning a bunch of pdf files into .txt files, we tokenize the corpus then remove punctuation, capitalization, and a list of common stopwords (like 'and' and 'the'). We then look at the most commong words in the corpus, and remove those we decide are in some way meaningless. These include, for instance, 'journal,' which is a very common word that is present in most of the papers due to their reference list. 

From the cleaned corpus consisting of papers that cite Anderson & May, we generate a list of most common words that we think are also meaningful, and use this to build the set of key words for our literature search.

*Topic Detection*

We use a few different techniques to look at topic detection in the corpus. These include Facebook's publicly available fastText code (fastText folder), non-negative matrix factorization (TD_NMF.ipynb), and latent Dirichlet allocation (TopicDetection.ipynb). 

For the analysis of the actual corpus, we look at only abstracts, as these discuss only what is actually done in the paper, and not a general background on the topic.
