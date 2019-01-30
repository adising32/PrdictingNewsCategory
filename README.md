# PrdictingNewsCategory

Dataset : Consists of 2225 documents from the BBC news website corresponding to stories in five topical areas from 2004-2005.
Natural Classes: 5 (business, entertainment, politics, sport, tech). Publication : - D. Greene and P. Cunningham. "Practical Solutions to the Problem of Diagonal Dominance in Kernel Document      Clustering", Proc. ICML 2006.

Preprocessing : The articles are read from txt files and are stored in a list. All punctuation marks, numbers, stopwords are removed to get a filtered list. All words are lemmatized according to their part of speech. 
Word2Vec analysis - Vectors for each word are obtained from Google's pre trained word2vec model. It includes word vectors for a vocabulary of 3 million words and phrases that they trained on roughly 100 billion words from a Google News dataset. The vector length is 300 features.

Model : A convolutional neural network is built using 1-D convolution layers, 1D Maxpooling Layers and multilayer perceptrons.

_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
embedding_2 (Embedding)      (None, 250, 300)          6554400   
_________________________________________________________________
conv1d_3 (Conv1D)            (None, 250, 256)          230656    
_________________________________________________________________
max_pooling1d_3 (MaxPooling1 (None, 125, 256)          0         
_________________________________________________________________
conv1d_4 (Conv1D)            (None, 125, 128)          98432     
_________________________________________________________________
max_pooling1d_4 (MaxPooling1 (None, 31, 128)           0         
_________________________________________________________________
flatten_2 (Flatten)          (None, 3968)              0         
_________________________________________________________________
dense_3 (Dense)              (None, 256)               1016064   
_________________________________________________________________
dropout_1 (Dropout)          (None, 256)               0         
_________________________________________________________________
dense_4 (Dense)              (None, 5)                 1285      
=================================================================
Total params: 7,900,837
Trainable params: 1,346,437

Accuracy : 97.1%
