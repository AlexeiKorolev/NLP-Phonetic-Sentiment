# NLP-Phonetic-Sentiment
Determining the weight that phonetics have on a word's meaning as a possible use case for lightweight language models. For my wordback dataset, I used the words present within the Vander sentiment analyzer in the NLTK library. To get the phonetic pronunciations, I used Carnegie Mellon's Logios lexicon (http://www.speech.cs.cmu.edu/tools/lextool.html). I used this data to train two models: a neural network and a random forest. The random forest model performed better, but the neural network would be more suited for lightweight applications. 

# The results

The resulting model had a **96.5% classification accuracy** when determining if a word had a positive or negative meaning, and a mean squared error of just about **0.1**. The model was only given the types of sounds present within a word and the quantity of each sound present. There was no information about the order of the sounds. Hence, by using sounds alone, it was able to very accurately predict whether or not a word had a positive or negative meaning. These results show that phonetics alone conveys meaning without even having the structure of a word.

I tested these results by running the model on two very rhythmic pieces of text: The Raven by Edgar Alan Poe and What a Wonderful World by Louis Armstrong. The model gave The Raven a very negative score of **-117** and What a Wonderful World a near-neutral score of **-5.6**. This test shows that there may be a negative bias when analyzing large pieces of text, but simultaneously, the model clearly and correctly differentiated the two pieces of text.

Ultimately, this project is a proof of concept for more research to be conducted in this field of linguistics, as it has important applications in lightweight language models, which may need to understand the connotation of slang, local dialect, or garbled speech without having prior exposure to it. 

Phonetics may be the key to a lightweight yet robust model that understands speech that it has not yet been exposed to. 
