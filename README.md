# Book Recommendation System

This project is a book recommendation system developed using Python. It leverages Natural Language Processing (NLP) techniques to analyze book titles and authors and generate recommendations based on the similarity between books. The project utilizes a dataset containing various book attributes such as title, author, average rating, and price.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Setup Instructions](#setup-instructions)
- [Data Exploration](#data-exploration)
- [Visualizations](#visualizations)
- [Recommendation System](#recommendation-system)
- [Testing the System](#testing-the-system)
- [Conclusion](#conclusion)

## Introduction

The goal of this project is to develop a book recommendation system using a dataset of books and their attributes. This system leverages NLP techniques to analyze book titles and authors and generate recommendations based on the similarity between books.

## Dataset

The dataset contains information on books, including the following columns:
- `bookID`: Unique identifier for each book.
- `title`: Title of the book.
- `authors`: Author(s) of the book.
- `average_rating`: Average rating of the book.
- `prices`: Price of the book.
- `rating_type`: Type of rating (e.g., High, Medium, Low).
- `prices_type`: Type of price (e.g., High, Medium, Low).
- `author_category`: Category of the author (e.g., Fiction, Non-Fiction).

The dataset is loaded from an Excel file (`books_data.xlsx`) located in Google Drive.

## Setup Instructions

To run the project locally, follow these steps:

1. **Mount Google Drive**:
    ```python
    from google.colab import drive
    drive.mount('/content/drive')
    ```
2. **Install Necessary Libraries**:
    Install required libraries such as `pandas`, `numpy`, `sklearn`, and `plotly`.

3. **Import Libraries**:
    ```python
    import pandas as pd
    import numpy as np
    from sklearn.feature_extraction.text import TfidfVectorizer
    from sklearn.metrics.pairwise import linear_kernel
    import plotly.express as px
    import plotly.graph_objects as go
    ```
4. **Load the Dataset**:
    Load the dataset from Google Drive.
    ```python
    bookdata = pd.read_excel("/content/drive/MyDrive/Files/books_data.xlsx")
    ```

## Data Exploration

The dataset is explored to understand its structure and characteristics:
- Column names, data types, and basic statistics.
- Shape of the dataset, number of rows and columns.
- Summary statistics such as mean, standard deviation, etc.
- Checking for null values in the dataset.

## Visualizations

Several visualizations are created to better understand the dataset:
- **Histogram of Average Ratings**: Displays the distribution of average ratings.
- **Bar Chart of Books per Author**: Shows the number of books for each author.
- **Table of Average Ratings per Author**: Displays average ratings for each author.
- **Table of Average Prices per Author**: Displays average prices for each author.
- **Pie Chart of Price Types**: Shows the distribution of price types.
- **Pie Chart of Rating Types**: Shows the distribution of rating types.
- **Scatter Plot of Average Rating vs. Rating Type**: Visualizes the relationship between average rating and rating type.
- **Scatter Plot of Average Rating vs. Prices**: Shows the correlation between average rating and prices.

## Recommendation System

The recommendation system is built using a `TF-IDF Vectorizer` to calculate similarities between books:
- **TF-IDF Vectorizer**: Converts text data (title and author) into numerical format for similarity computation.
- **Cosine Similarity**: Computes the similarity between books based on their TF-IDF vectors.
 
### Recommendation Functions

1. **Recommend Books Based on a Book Title**:
   - Takes a book title as input and returns the top 10 recommended books based on similarity.

2. **Recommend Books by Author**:
   - Takes an author name as input and recommends books similar to those written by the given author.

3. **Top Rated Books by Author**:
   - Retrieves the top-rated books by a specific author.

## Testing the System

The system can be tested by entering a book title or an author name to see the recommended books. Examples of inputs and their corresponding outputs are provided in the project notebook.

## Conclusion

This project successfully demonstrates a book recommendation system using NLP and machine learning techniques. The system effectively recommends books based on similarity measures and provides valuable insights through various visualizations.

---

Feel free to explore the code and modify it to improve the recommendation system or to add more features!

## Authors

This project was developed as a group project.
