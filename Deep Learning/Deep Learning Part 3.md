# RNN - Recurrent Neural Networks:

	• type of Neural Network where the output from previous step are fed as input to the current step. 
	• In traditional neural networks, all the inputs and outputs are independent of each other,
	• but in cases like when it is required to predict the next word of a sentence, the previous words are required and hence there is a need to remember the previous words. 
	• Thus RNN came into existence, which solved this issue with the help of a Hidden Layer. 
	• The main and most important feature of RNN is Hidden state, which remembers some information about a sequence.
	• uses the same parameters for each input as it performs the same task on all the inputs or hidden layers to produce the output. 
	• This reduces the complexity of parameters, unlike other neural networks.
	
	• Main application - NLP
	• Use cases:

		○ Text autocompletion
		○ Translation
		○ NER : Named Entity Recognition
		○ Sentiment Analysis

## Why not ANN?:

	• No fixed # of neurons 
	• Too much computation (with word2Vec)
	• Parameters are not shared
	• Data is sequential in nature. Order matters.

<p align="center">
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/rnn.png" height=300/> 
</p>

## Types of RNN:

<table>
    <tr>
        <td>Many to Many</td>	
        <td>Language Translation/td>
    </tr>
    <tr>
        <td>Many to One</td>	
        <td>Sentiment Analysis</td>
    </tr>
    <tr>
        <td>One to Many</td>	
        <td>Music generation, poetry writing</td>
    </tr>
<table>

## LSTM:
	• Long Short Term Memory
	• Two hidden states : Long / short
	• Train the network to retain context for long and short term
	• 3 Gates : Input, output, forget
    • <a href="http://colah.github.io/posts/2015-08-Understanding-LSTMs/">Article</a>

## GRU
	• Only one state for long & short term memory
	• Light weight LSTM
	• 2 gates : update , reset
	• Less accurate than LSTM on longer sequence
    • More efficient in computation than  LSTM

## Bidirectional RNN:
<p align="center">
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/bidir_rnn.png" height=300/> 
</p>
    
    • An additional layer which contains the context from the reverse sequence


# Techniques to process Textual data


### 1. Build vocabulary and number the individual words:
    ○ Distance problem b/w random and similar words
### 2. One hot encoding
    ○ Relationship between similar words (ex: grapes, bananas are fruits)
    ○ Computation cost
    ○ Transfer learning is not possible, need complete retrain
### 3. Word embedding
    ○ Capture similarity  b/w  words
    ○ Feature extraction from words -> Feature Vector

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/word_embed1.png" height=300/> 
</p>
<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/word_embed2.png" height=300/> 
</p>

# Word  embedding:
	• Word embedding is just a fancy way of saying numerical representation of words. 
	• A good analogy would be how we use the RGB representation for colors.
	• Supervised
	• Not widely used any more
	• Are not hand crafted
	• Embeddings are by-product of training a model for classification, like sentiment
    • Similar words have similar feature vector values in the embedding
    • Padding, according to the max words in a sentence

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/word_embed3.png" height=300/> 
</p>

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/word_embed4.png" height=300 />
</p>

# Word2Vec

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/word2vec.png" height=300/>
</p>

    • CBOW : Continuous bag of words
		○ Predict target from the context
	• Skip gram
		○ Given Target, predict the context
	• Skip-gram: works well with a small amount of the training data, represents well even rare words or phrases.
    • CBOW: several times faster to train than the skip-gram, slightly better accuracy for the frequent words.

# BERT

<a href="http://jalammar.github.io/illustrated-bert">Blog</a>

	• Bidirectional Encoder Representations from Transformers (by Google)
	• Google Search suggestions are powered by BERT
	• Issue with Word2Vec -> Fixed embeddings
		○ "Fair" can be used in different contexts
	• BERT can generate contextualized embeddings
<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/BERT1.png" height=300/>
</p>

	• Can generate embeddings for a sentence as well
<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/BERT2.png" height=300/>
</p>

	• Mask sequences, train to predict the missing words, embeddings is the by-product
<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/BERT3.png" height=300/>
</p>


