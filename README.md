## Movie Recommendation System using Python and Machine Learning (Content Based Filtering)

This project implements a movie recommendation system using content-based filtering, a machine learning technique. Content-based filtering recommends items to users based on the features of items and the preferences expressed by the user. In this system, I leverage movie metadata such as genres, keywords, cast, and crew to recommend similar movies to users based on their preferences.

### Project Overview

#### Objective
The objective of this project is to recommend movies to users based on the content similarity between movies.

#### Dataset
The dataset used in this project consists of two main files:
- `movies.csv`: Contains information about movies, including titles, overview, genres, keywords, cast, and crew.
- `credits.csv`: Contains information about movie credits, including cast and crew details.

Download datasets at: [MovieLens Dataset](https://grouplens.org/datasets/movielens/) and [IMDb Datasets](https://www.imdb.com/interfaces/)


### Implementation Steps

1. **Data Loading and Preprocessing**:
    - Read the dataset into Pandas DataFrames.
    - Merge the two DataFrames based on the movie title.
    - Extract relevant features such as genres, keywords, cast, and crew from the merged DataFrame.
    - Preprocess the text data by tokenizing and stemming the words.

2. **Feature Engineering**:
    - Combine the extracted features into a single column to represent movie tags.
    - Transform the text data into numerical vectors using CountVectorizer.

3. **Similarity Calculation**:
    - Calculate cosine similarity between movies based on their tag vectors.

4. **Recommendation Function**:
    - Define a function to recommend movies similar to a given movie.
    - Retrieve the movie index from the DataFrame based on the input movie title.
    - Calculate similarity scores between the input movie and other movies.
    - Sort the movies based on their similarity scores and recommend the top-ranked ones.

5. **Testing**:
    - Test the recommendation function with sample movie titles.
    - Generate movie recommendations for a given movie title.

### How to Use
1. Ensure you have the required libraries installed (`numpy`, `pandas`, `nltk`, `sklearn`).
2. Download the dataset files (`movies.csv` and `credits.csv`) or provide your own dataset.
3. Run the provided Python script to execute the recommendation system.
4. Call the `recommend()` function with a movie title to get recommendations based on that movie.

### Conclusion
This movie recommendation system offers a personalized way to suggest movies to users based on the content similarity between movies. Content-based filtering techniques like this can be useful in various applications, including movie streaming platforms and online entertainment websites, to enhance user experience and engagement.

Feel free to explore and customize the recommendation system to suit your specific requirements and datasets.

**Enjoy discovering new movies!**
