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
 ![image](https://user-images.githubusercontent.com/103464406/217096812-44da4bbe-82fb-4b43-9209-2b7f5d081e80.png)

 ![image](https://user-images.githubusercontent.com/103464406/217096839-8238de6d-f32a-4a28-a194-6fea85052c3b.png)
 
 ![image](https://user-images.githubusercontent.com/103464406/217096901-cb5bb7a6-e31c-45be-bd37-c7064e91289c.png)
 ![image](https://user-images.githubusercontent.com/103464406/217096994-c9e587e1-ed5a-4a79-91d7-e52030c25cf6.png)

 ![image](https://user-images.githubusercontent.com/103464406/217096957-502c3873-3331-4358-a66c-2061ac5d2135.png)
 ![image](https://user-images.githubusercontent.com/103464406/217097010-c5cc6f23-1a49-4078-b326-e05808eedbbb.png)
 
 ![image](https://user-images.githubusercontent.com/103464406/217097056-a35051df-b448-49a7-a17d-80249af3d04f.png)

 
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

- Copycat (1995)	is a crime/thriller movie and if we compare with som eof the other recommendation they also seem to belong to the same genre.

  ![image](https://user-images.githubusercontent.com/103464406/217041099-1b6836d4-8fe9-46bd-b4a4-faf7d6b935b4.png)



### Collaborative Filtering:
- We will use surprise library to create a recommender system.
- Singular value decomposition (SVD) is a collaborative filtering method for movie recommendation. 
- The aim is to provide users with movies’ recommendation from the latent features of item-user matrices

#### Function recommendation_SVD:
- Takes as input the userdId and the get_recommend> number of recommendations required.Default values userID=1, get_recommend =10
- Using Singular value decomposition (SVD) model the function will predict movie recommendations and return top recommendations.
 ![image](https://user-images.githubusercontent.com/103464406/217043062-40688304-686f-48a6-bf54-4604ce75cafa.png)
 ![image](https://user-images.githubusercontent.com/103464406/217043186-3c02865a-8bfb-4bca-b3c1-17be08a5f007.png)
