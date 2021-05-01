# Text-Extraction
The extractive text summarization technique involves pulling key phrases from the source document and combining them to make a summary. The extraction is made according to the defined metric without making any changes to the texts.
### I performed two extractive text summarization models:
1)	Extractive Text summarization by using Gensim
2)	Extractive Text summarization by using Spacy
Gensim library is used here for the task of text summarization. It is the most famous deep NLP Library. 
This algorithm produces a certain ratio of the no of original sentences from the given text by taking the argument ratio. It is extractive summarization as there are no new words/sentences created. These are algorithms which can be used for generative summarization (where algorithms come up with own words).
About Algorithm:
Road Map: RAW Text -> Cleaned Text -> Sentences -> Tokenized sentences -> Sentence Vector -> Similarity Matrix -> Graph -> Ranking -> Summary
•	Raw text is of no worth, we have to convert to clean text as the process of text pre-processing. We remove capital letters, puntuations, numbers.
This process is also called as text pre-processing.
•	The cleaned text is divided into sentences.
•	Sentences are divided into words. This process is also called as Tokenization of sentences.
•	Sentences are converted to word vectors as computer don’t understand letters.
•	Sentence vectors are formed by using word vectors (Made into numbers) - Appending the word vectors. We can also use TF-IDF to do (Word vectors perform well).

•	A similarity matrix nXn is created, where n is the number of sentence vectors for further computing similarity.

•	There are multiple ways to compute similarity famous ones are cosine similarity and Euclidean distance.
•	A graph is formed, where nodes are sentences and Edges represent similarity (Every node is connected to other node as the similarity between two sentences always exists). Hence it is a complete graph.
•	For ranking we use Page Ranking Algorithm (which google uses). In Page ranking algorithm, the pages are treated as nodes and similarity between web pages are treated as edges. The score denotes the probability of user accessing the link. In our case, the score represents importance of particular sentence in the text.
•	All the sentences are ranked in the order of score and top K lines are displayed.
•	Thus, it pulls out the require sentences out of the given input.

