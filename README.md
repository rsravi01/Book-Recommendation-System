# Book-Recommendation-System
Overview

This project is a Book Recommendation System built using Flask as the web framework and Collaborative Filtering for recommendations. It suggests books based on user preferences using Cosine Similarity.

Features

Displays popular books with their titles, authors, ratings, and cover images.

Provides a search-based recommendation system where users enter a book title to find similar books.

Uses collaborative filtering to recommend books based on rating patterns.

Flask-based web interface to interact with the model.

Tech Stack

Python (Backend & Model Processing)

Flask (Web Framework)

Pandas & NumPy (Data Handling & Computation)

Pickle (Model Storage)

HTML, CSS (Frontend for UI)

Dataset

This project uses three main datasets:

books.csv - Contains book details (title, author, image URLs, etc.).

users.csv - Contains user information (user ID, location, etc.).

ratings.csv - Contains user ratings for books.

These datasets are preprocessed and stored in .pkl files for faster access.

How It Works

Data Preprocessing

The dataset is cleaned and formatted into a pivot table.

Missing ratings are filled with zero.

Model Training

Cosine Similarity is computed between books based on user ratings.

A similarity matrix is created for book recommendations.

Flask Application

The homepage (/) displays popular books.

The /recommend page allows users to input a book title.

The /recommend_books route processes the input and returns similar books.

Installation & Setup

Prerequisites

Ensure you have Python 3.8+ installed along with the required libraries:

pip install flask pandas numpy

Running the Project

Clone the repository:

git clone https://github.com/your-repo/book-recommender.git
cd book-recommender

Ensure the required files (popular.pkl, pt.pkl, books.pkl, similarity_scores.pkl) are in the project directory.

Start the Flask server:

python app.py

Open your browser and go to:

http://127.0.0.1:5000/

File Structure
```
|-- static/
|   |-- style.css  # Styles for the web pages
|-- templates/
|   |-- index.html  # Homepage displaying popular books
|   |-- recommend.html  # Recommendation page
|-- books.csv  # Book dataset
|-- users.csv  # Users dataset
|-- ratings.csv  # Ratings dataset
|-- popular.pkl  # Processed popular books data
|-- pt.pkl  # Pivot table for recommendations
|-- books.pkl  # Book metadata
|-- similarity_scores.pkl  # Precomputed similarity scores
|-- app.py  # Flask web app
|-- README.md  # Project documentation
```
Future Improvements

Implement Hybrid Filtering (Collaborative + Content-Based) for better accuracy.

Add a search autocomplete feature for book titles.

Deploy the system using Heroku or AWS for public access.

License

This project is open-source and available under the MIT License.
