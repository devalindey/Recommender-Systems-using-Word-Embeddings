# Recommender-Systems-using-Average-Word2vec-and-TF-IDF-Word2vec
Movie recommendation engines built using word embeddings.

## **What is Word2vec?**

Word2Vec is a simple neural network model with a single hidden layer. It predicts the adjacent words for each and every word in the sentence or corpus. We need to get the weights that are learned by the hidden layer of the model and the same can be used as word embeddings.


## **Average Word2vec**

The sum of all the vectors divided by the total number of words in the description is known as **Average Word2vec**. It can be calculated as follows:

![Imgur](https://i.imgur.com/YIiuuyb.png)

where,  vectors are in **D**-dimensional space, & **n** = total number of words.


## **TF-IDF Word2vec**
TF-IDF is a term frequency-inverse document frequency. It helps to calculate the importance of a given word relative to other words in the document and in the corpus. It calculates in two quantities, TF and IDF. Combining two will give a **TF-IDF score**.

*Steps to calculate the TF-IDF Word2Vec:*
1. Calculate the TF-IDF vector for each word.
2. Calculate the Word2Vec for each word.
3. Multiply the TF-IDF score and Word2Vec vector representation of each word and total.
4. Finally, divide the total by sum of TF-IDF vectors. It can be written as follow:

![Imgur](https://i.imgur.com/Ikrhbbp.png)


## Content-based recommendation system

A content-based recommendation system recommends movies to a user by considering the similarity of movies. This recommender system recommends a movie based on the movie description. It identifies the similarity between the movies based on its description. It also considers the user's previous movie history in order to recommend a similar movie.

Example: If a user likes the movie 'Avengers: Endgame', then the recommender system recommends the user to watch other Marvel movies or it recommends some similar 'action' movies.

We need to find similar movies to a given movie and then recommend those similar movies to the user. How to find whether the given movie is similar or dissimilar? A similarity measure was used to find the same. ***Cosine similarity*** was used in our recommender system to recommend the movies.

As I mentioned above, we are using scraped IMDB data and don’t have a user's watch history. Hence, we won't use a collaborative recommendation engine.

![Imgur](https://i.imgur.com/k6Md1hU.png)
