# DiseaseEcology
Can we define the field of disease ecology? Using natural language processing? We can sure try!

**Code**

Contains code for cleaning and analyzing the corpus datasets.

*Cleaning*

After pre-processing, which is basically turning a bunch of pdf files into .txt files, we tokenize the corpus then remove punctuation, capitalization, and a list of common stopwords (like 'and' and 'the'). We then look at the most commong words in the corpus, and remove those we decide are in some way meaningless. These include, for instance, 'journal,' which is a very common word that is present in most of the papers due to their reference list. 

From the cleaned corpus consisting of papers that cite Anderson & May, we generate a list of most common words that we think are also meaningful, and use this to build the set of key words for our literature search.

*Topic Detection*

We use a few different techniques to look at topic detection in the corpus. These include Facebook's publicly available fastText code (fastText folder), non-negative matrix factorization (TD_NMF.ipynb), and latent Dirichlet allocation (TopicDetection.ipynb). 

For the analysis of the actual corpus, we look at only abstracts, as these discuss only what is actually done in the paper, and not a general background on the topic.
