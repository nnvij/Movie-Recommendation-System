# Movie-Recommendation-System
 - Recommender system is a type of information filtering system that seeks to predict the "rating" or "preference" a user would give to an item.
 - The system improves the quality of search results and provides items that are more relevant to the search item or are related to the search history of the user.
 - A movie recommendation system is an automated system that can suggest movies to users based on their preferences.
 
## Types of Recommender System:
#### Content-Based Filtering:
- Content-based filtering uses a user’s past movie ratings and preferences to recommend similar movies. It looks at the attributes of a movie such as its genre, actors, director, etc. and matches it with the user’s preferences.

#### Collaborative Filtering:
- Collaborative filtering uses the ratings and preferences of other users to recommend movies. It looks at the ratings of similar users and recommends movies that they have liked and rated highly.

## Problem Statement:
- Using content based filetering, design a Movie recommender system which could recommend similar movies as per Movie Genre and Tags.
- Based on collaborative filtering, design a movie recommender system using Singular value decomposition (SVD).

### Tools used:
- Python, Pandas (data processing), Matplotlib, Plotlyexpress

## Data:
- Movielens dataset is used for this project: https://grouplens.org/datasets/movielens/
 ![image](https://user-images.githubusercontent.com/103464406/217036341-043b629e-bb7e-4ff6-adb2-0cae0b60b5c2.png)

## EDA:

## Model:
### Content Based filtering:
- Movies recommendation system is created based on similar genre or similar movie tags.
- We calculate the cosine similarity score for all the movie titles in the dataset as per genre and tags.
- Using TfidfVectorizer convert text column genre/tag  to feature vectors.
- Once we have the feature matric we will calculate similarity scores across titles.
- Create function that will take an input movie title and generate movie recommendation based on genre/tags of the input title.
#### Cosine similarity:
- Cosine similarity is a measure of similarity between two non-zero vectors. 
- It is calculated as the angle between these vectors (which is also the same as their inner product).
 ![image](https://user-images.githubusercontent.com/103464406/217038040-4492c00d-5503-4069-a301-7e5366543bf2.png)

#### Function movie_recommender:
- Takes as input the title of the movie for which we predict movie recommendation.
- Find the index for the title and pick up the similarity score for that index.
- We will then sort the score and return the top 10 movie titles with highest similarity score.
  ![image](https://user-images.githubusercontent.com/103464406/217041694-02e5d2c0-0248-4422-9001-e1fc8bdeb801.png)

- Copycat (1995)	is a crime/thriller movie and if we compare with som eof the other recommendation they also seem to belong to the same genre
  ![image](https://user-images.githubusercontent.com/103464406/217041099-1b6836d4-8fe9-46bd-b4a4-faf7d6b935b4.png)
  ![image](https://user-images.githubusercontent.com/103464406/217041626-155bc6eb-ac89-461d-b532-740714632b15.png)


### Collaborative Filtering:
