# Movie Recommender System

## Overview
Let's assume you're interested in creating a recommendation engine to help recommend to users new movies based on previous ratings of movies they've watched. 

There are atleast two types of recommender systems you can build:

### 1. User Based Collaborative Filtering

> + The idea here is to build a matrix of users (rows) vs things they've bought/watched/browsed/rated (columns)
> + Compute similarity scores between users (rows) 
> + Find similar users to you
> + Recommend stuff they've bought/watched/browsed/rated that you haven't  

**Downsides**: 

+ Users can be nefarious
	+ a user can spam by rating movies in a way to benefit their cause
	+ [Shiling Attack](https://link.springer.com/article/10.1007/s10462-012-9364-9)
+ People's taste and interest change over time
+ Far more users than things
  + Computationally very $$

### 2. Item Based Collaborative Filtering

> + Find every pair of movies that were watched by the same user
> + Measure similarity of their rating across all users who have watched the same movie
> + Sort by movie, then by similarity strength (though there are other ways to do this)

This repository includes an implementation of an **Item Based Recommender System** for movies. 

The dataset is available via [GroupLens](http://grouplens.org/datasets/movielens/latest/). It contains:

+ 100,000 ratings 
+ 1,300 tag applications 
+ 9,000 movies 
+ 700 users
+ Last updated 10/2016