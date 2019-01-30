# PrdictingNewsCategory

Dataset : Consists of 2225 documents from the BBC news website corresponding to stories in five topical areas from 2004-2005.
Natural Classes: 5 (business, entertainment, politics, sport, tech). Publication : - D. Greene and P. Cunningham. "Practical Solutions to the Problem of Diagonal Dominance in Kernel Document      Clustering", Proc. ICML 2006.

Preprocessing : The articles are read from txt files and are stored in a list. All punctuation marks, numbers, stopwords are removed to get a filtered list. All words are lemmatized according to their part of speech. 
Word2Vec analysis - Vectors for each word are obtained from Google's pre trained word2vec model. It includes word vectors for a vocabulary of 3 million words and phrases that they trained on roughly 100 billion words from a Google News dataset. The vector length is 300 features. Link : http://mccormickml.com/2016/04/12/googles-pretrained-word2vec-model-in-python/

Model : A convolutional neural network is built using 1-D convolution layers, 1D Maxpooling Layers and multilayer perceptrons.

Accuracy : 97.1%
