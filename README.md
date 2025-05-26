# Movie-Recommendation-system
Movie Recommendation System This is a Content-Based Movie Recommendation System that recommends similar movies to the one you enter. It applies natural language processing (NLP) techniques to movie metadata like genre, overview, cast, and keywords to calculate similarity between movies.
Objective
The main aim is to develop a recommendation engine that allows users to find new movies with similar content to the movie of their choice. Rather than using user ratings or external comments, this approach uses only the inherent properties of the movies themselves.

#How It Works 
This project employs the content-based filtering method, which functions through comparing the descriptive details of the movies. Following is a step-by-step explanation:

-> Data Collection and Preprocessing:

The system has a movie metadata dataset that includes columns like:
title, genres, keywords, cast, crew, and overview

JSON-like columns are processed using ast.literal_eval to transform strings into Python objects

All the information that is pertinent is merged into one text-based column named tags

-> Text Vectorization:

The tags column is processed with CountVectorizer to transform text data into numerical vectors

Stopwords are common words removed and vocabulary is restricted to the most common 5000 words

--> Similarity Computation:

Cosine similarity is computed between each pair of movies based on their tag vectors

The system constructs a similarity matrix to retrieve similar movies quickly

-> Recommendation Output:

When a movie is chosen by a user, the app provides the top 5 most similar movies with the maximum similarity scores

The system deals with missing entries and provides strong recommendations

-> Streamlit Interface:

A clean and minimalist interface is constructed with Streamlit

The user can choose a movie from a dropdown and see instant suggestions without reloading the application

![Screenshot 2025-05-27 004137](https://github.com/user-attachments/assets/b6978c0e-66a4-41a2-8bb2-20e410515016)
