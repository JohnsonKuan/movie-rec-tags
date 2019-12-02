# movie-rec-tags
Content-based movie recommender system using MovieLens tags

## Python Libraries Used:

* warnings
* re
* PIL
* wordcloud
* pandas
* numpy
* umap
* matplotlib
* seaborn
* gensim
* nltk

## Environment YAML File

I included a conda YAML file for you to create the environment I used with all the libraries installed:

```bash
conda env create -f env_movie_rec_tags.yml
```

## Motivation for the Project

I wanted to see if I can build a simple but reasonable content-based movie recommender system with only MovieLens tags. There are three key business questions that I answer along the way which are critical to building this recommender system.

## Files

* Movie-Rec-Movielens-Tags.ipynb

  * Jupyterlab notebook with all the code used in the analysis

* env_movie_rec_tags.yml

  * YAML File with configuration of environment used
  
## Data

All data used is from the MovieLens 20M datasets: https://grouplens.org/datasets/movielens/20m/

## Medium Blog Post

## Summary of Results

I was able to build a simple content-based movie recommender system with only MovieLens tags by answer three key business questions (see blog post for more details):

1. Q1: How many tags do we need for each movie?

  * I kept the top N tags for each movie based on relevance score
  * I demonstrated that N = 50 was reasonble to make sure we had enough relevant tags for each movie

2. Q2: How do we use tags to measure the similarity between movies?

  * I demonstrate two appproaches that were reasonble:
    * Jaccard Distance of two sets of movie tags
    * Cosine Similarity of Movie Vectors (aka Content Embeddings) based on tags

3. Q3: How do we use tags to generate movie recommendations for a user?

  * I demonstrated that we can compute a user vector based on the average of movie vectors that the user has watched
  * I demonstrated that we can use this user vector to find similar movies based on cosine similarity
  * These similar movies are the recommendations to the user



