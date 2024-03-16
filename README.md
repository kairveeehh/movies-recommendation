# Movie Recommendation System using Cosine Similarity

## Overview
In this project, I implemented a movie recommendation system using machine learning techniques. The system analyzed movie metadata such as genres, keywords, cast, and crew to provide personalized movie recommendations to users.

## Data Preprocessing
- Loaded the movie datasets (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`) from Kaggle.
- Merged the datasets based on movie titles to consolidate movie information.
- Performed initial data cleaning and selected relevant columns for analysis.

## Text Data Processing
- Converted stringified lists in columns such as `genres`, `keywords`, `cast`, and `crew` to actual lists using `ast.literal_eval`.
- Preprocessed text data by dropping missing values, extracting relevant information (e.g., names of genres, keywords, cast, crew), and formatting them appropriately.

## Vectorization
- Vectorized text data using Count Vectorization to convert it into numerical representations suitable for machine learning algorithms.
- Created a feature matrix with a limited number of features (e.g., 5000) using CountVectorizer.

## Similarity Calculation
- Utilized cosine similarity to compute the similarity between movies based on their feature representations.
- Cosine similarity measured the cosine of the angle between two vectors, providing a similarity score between -1 and 1.

## Recommendation Function
- Defined a recommendation function (`recommend`) to recommend movies based on user input.
- Retrieved the index of the input movie in the dataset, calculated similarity scores between the input movie and all other movies, sorted the movies based on similarity scores, and recommended the top similar movies (excluding the input movie itself).

## Saving Models
- Saved the processed movie dataset (`new`) and the similarity matrix (`similarity`) using pickle for future use.

## Example Usage
- Provided an example of recommending movies with the movie "Gandhi" as input to showthe functioning of the system.

##Author 
Kairvee vaswani 
vkairvee@gmail.com

