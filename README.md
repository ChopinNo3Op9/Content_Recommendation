# Content_Recommendation

# Project: Content-Based Movie Recommendation System

## Description:

This Jupyter notebook implements a content-based recommendation system using the MovieLens dataset. The overall process is outlined as follows:

### 1. Establishing Item Profiles

- Users assign tags to movies and movies have categorical values.
- Combine tags and categorical values for each movie, then calculate TF-IDF (Term Frequency-Inverse Document Frequency).
- Select the top-n (those with high TF-IDF values) keywords for each movie.
- Format: Movie ID - Keywords - Keyword Weight

### 2. Building an Inverted Index

- Search for movies through keywords.
- Iterate through the data of movie ID - Keywords - Keyword Weight, and use the keywords as keys to store tuples of (movie ID corresponding to the keyword, TF-IDF) as values in a dictionary.

### 3. User Profiles

- Determine which movies the user has watched and find the corresponding keywords in the movie data (Movie ID - Keywords - Keyword Weight).
- Aggregate all keywords from the user's watched movies and count the frequency of each keyword.
- Keywords with higher frequencies become the user's interest keywords, forming the user profile.

### 4. Recommending Movies Based on User Interest Keywords

- Using the user's interest keywords, find movies corresponding to those keywords. Multiple interest keywords may correspond to a single movie. 
- Sum up the weights of keywords for each movie and rank them. Movies with higher weights are recommended to the user.

## Usage:

1. Make sure to have the MovieLens dataset accessible.
2. Execute the Jupyter notebook in a Python environment with necessary dependencies installed.

