# Recommender-Systems-using-Average-Word2vec-and-TF-IDF-Word2vec
Movie recommendation engines built using word embeddings

What is Word2Vec?
Word2Vec is a simple neural network model with a single hidden layer. It predicts the adjacent words for each and every word in the sentence or corpus. We need to get the weights that are learned by the hidden layer of the model and the same can be used as word embeddings.

Let’s see how it works with the sentence below:

![Image of Yaktocat](https://miro.medium.com/max/1126/1*nHCu34KJUpgPBa7FZutolA.png)

From the above, let’s assume the word “theorist” is our input word. It has a context window of size 2. This means we are considering only the 2 adjacent words on either side of the input word as the adjacent words.

Now, the task is to pick the nearby words (words in the context window) one-by-one and find the probability of every word in the vocabulary of being the selected adjacent word. Here, the context window can be changed as per our requirement.

Word2Vec has two model architectures variants: Continuous Bag-of-Words (CBoW) and SkipGram. The internet is literally flooded with a lot of articles about Word2Vec, hence I have not explained in detail. Please check here for more details on Word2Vec.

In simpler terms, Word2Vec takes the word and returns a vector in D-dimensional space.

Please note, Word2Vec provides the word embeddings in low dimensionality (50–500) which are dense (it’s not a sparse matrix, most values are non-zero). I used 300 dimension vectors for this recommendation engine. As I mentioned above, Word2Vec is good at capturing semantic meaning and relationships.

Training our own word embeddings is an expensive process and also requires a large dataset. I don’t have a large dataset as I scraped Goodreads data which only pertains to the genres of business and cooking. We will use Google pre-trained word embeddings which were trained on a large corpus, including Wikipedia, news articles and more.

The pre-trained embeddings helped to get the vectors for the words you want. It is a large collection of key-value pairs, where keys are the words in the vocabulary and values are their corresponding word vectors.

In our problem, we need to convert the book descriptions into a vector and finding the similarity between these vectors to recommend books. Each book description is a sentence or sequence of words. I have tried two methods: average Word2vec and TF-IDF Word2Vec.
