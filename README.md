# NLP-Assignments

### HW1: 
This assignments goal was to practice feature engineering for a logistic regression classifier on both movie reviews and Shakespeare plays. In the assingmnet we had to create a set of basic features and "interesting" features for both corpora. For the movie reviews corpus the goal was distinguish postive reviews and ngeative reviews, while in the Shakespeare plays corpus the goal was to distinguish the comedies and tragedies. The features I chose ended up working well for both corpora given the assignment instrunctions. For the basic features in both corpora, I used a simple bag of words sparse matrix. For the interesting features, I created a "polarity score" that was a ratio of the count of a word in the positive (good reviews and comedies respectively) case to the count of a word in the negative (negative reviews and tragedies respectively) case. This ratio was used as a way to choose important words to use in the sparse matrix that would be passed to the classifier.

### HW2: 
This assignment's gaol was to practice using character level models for various tasks. The assignment had two parts; the first was using an n-gram character language model to distinguish english text from brazilian text and the second was to analyze a character level trained GRU unit on surnames for its effectiveness in sequence generation of surnames. 

The language modeling: the count for unigrams, brigrams, and trigrams were collected, then the total perplexity of each document was calculate using linear interpolation smoothing where the paramaters were found using a discretized set of values on a validation set, and finally the documents were separated by perplexity using trigram only linear interpolation smoothing.

Sequence generation: The gru is trained on the dataset, then I calculate the accuracy and perplexities of the model's performance for each character for each word in the test set. The trained model was then used to generate some example surnames. Finally, this process was run multiple time for different hidden unit sizes.

### HW3: 
The goal of this assignment was to use a Viterbi Decoder for sequence labeling with a LTSM named-entity recognition model and evaluate its performance. First the LSTM was trained to predict span level tags of words in those spans. Then a transition matrix was created of size K x K where K equals number of possible tags. Then a viterbi decoder was used to calculate the most likely sequence of tags. Then the violations, recall, precision, and f-mesaure were calulated for the decoder.

### HW4: 
The goal of this assignment was to practice reducing the demsnionality of words from their original space to a lower dimensional space and then evaluate the pairwise distance between the words in the embedded space. The copora consisted of english words and those words in other langauages and those words were vectorized using Word2Vec from the gensim library. Cosine Similarity was used to evaluate the most similar words to a word from the same language and from other language. The accuracy of these most similar words was gathered at the end for obsevation.
