# Movie Recommendation System Using Collaborative Filtering

## Project Overview

The Movie Recommendation System is a Machine Learning project that recommends movies to users based on their previous ratings and preferences.

This project uses **Collaborative Filtering** to identify similarities between movies based on user rating patterns and generate personalized movie recommendations.

The system is developed using Python and the MovieLens dataset.

## Objectives

* Build a personalized movie recommendation system.
* Apply Item-Item Collaborative Filtering.
* Calculate movie similarities using Cosine Similarity.
* Predict user ratings for unseen movies.
* Generate Top-10 movie recommendations.
* Evaluate the model using RMSE, MAE, Precision@10, and Recall@10.
* Handle the cold-start problem for new users and movies.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook
* PyCharm

## Dataset

**Dataset:** MovieLens ml-latest-small

**Source:** GroupLens Research

Dataset Link: https://grouplens.org/datasets/movielens/

The dataset contains:

* 100,836 user ratings
* 610 unique users
* 9,742 movies
* Ratings ranging from 0.5 to 5.0

## Project Structure

```text
Movie_Recommendation_System/
│
├── data/
│   └── ml-latest-small/
│       ├── ratings.csv
│       ├── movies.csv
│       ├── links.csv
│       └── tags.csv
│
├── movie_recommendation_collaborative_filtering.ipynb
├── main.py
├── requirements.txt
└── README.html
```

## Methodology

### 1. Data Collection

The MovieLens dataset is downloaded from GroupLens and loaded using Pandas.

### 2. Data Preprocessing

* Check missing values.
* Remove duplicate user-movie interactions if present.
* Analyze user ratings.
* Create a user-item rating matrix.
* Split the dataset into training and testing sets using chronological user-wise splitting.

### 3. Exploratory Data Analysis

Visualizations are created to understand:

* Rating distribution.
* Number of ratings per user.
* Most frequently rated movies.
* User activity patterns.

### 4. Collaborative Filtering

Item-Item Collaborative Filtering is implemented using Cosine Similarity.

The system identifies movies with similar rating patterns and uses a user's previous ratings to estimate preferences for unseen movies.

### 5. Model Evaluation

The model is evaluated using the following metrics:

**RMSE (Root Mean Squared Error)**

Measures the average magnitude of rating prediction errors, with larger errors penalized more heavily.

**MAE (Mean Absolute Error)**

Measures the average absolute difference between actual and predicted ratings.

**Precision@10**

Measures the proportion of recommended movies in the Top-10 list that are relevant.

**Recall@10**

Measures the proportion of relevant held-out movies successfully included in the Top-10 recommendations.

For ranking evaluation, ratings of 4.0 or higher are considered relevant.

## Top-10 Movie Recommendations

The system generates personalized Top-10 movie recommendations for three sample users.

Recommendations are generated based on historical ratings and predicted preferences.

Movies already rated by the user are excluded from the recommendation list.

## Cold-Start Problem

The cold-start problem occurs when a new user or movie has insufficient rating information.

### New User

A popularity-based recommendation strategy is used to recommend frequently rated movies until the user provides enough ratings for personalized recommendations.

### New Movie

A new movie without interaction history cannot receive a reliable collaborative filtering score. Content-based filtering using genres or movie descriptions can be added as a future improvement.

## Results

The notebook calculates:

* RMSE
* MAE
* Precision@10
* Recall@10
* Top-10 recommendations for sample users

Actual evaluation values are generated when the notebook is executed.

## Advantages

* Provides personalized recommendations.
* Uses real-world movie rating data.
* Identifies similarities between movies.
* Supports Top-N recommendation generation.
* Demonstrates practical Machine Learning concepts.

## Limitations

* Recommendations depend on historical rating data.
* Sparse ratings may reduce similarity accuracy.
* New movies have limited collaborative information.
* Popularity-based recommendations are not personalized.
* Offline evaluation does not guarantee real-world user satisfaction.

## Future Enhancements

* Implement Matrix Factorization using SVD.
* Compare User-Based and Item-Based Collaborative Filtering.
* Develop a Streamlit web application.
* Add genre-based content filtering.
* Improve cold-start recommendations.
* Deploy the application as a web service.

## Conclusion

The Movie Recommendation System demonstrates how Collaborative Filtering can be used to generate personalized movie recommendations from historical user ratings.

The project covers data preprocessing, exploratory analysis, similarity computation, rating prediction, model evaluation, and recommendation generation.

It provides practical experience in Machine Learning, Python programming, and recommender system development.


