# Movie Recommendation Systems

*Project Date: 2020-08-17*

## Introduction

With the information explosion in customer choices, the decision-making process becomes harder for the general public. Recommendation systems have been widely employed as an information filtering system to assist this process. For instance, collaborative filtering (CF) is one of the earliest and most successful recommender technologies, which provides personalized recommendation to users with similar action patterns. In this project, eight CF recommendation systems were deployed:

- User-based CF
- Item-based CF
- Customer Clustering 
- Movie Clustering
- Biclustering
- Singular Value Decomposition (SVD)
- Funk SVD
- Non-negative Matrix Factorization (NMF)

The mean square error (MSE) served as an indicator for estimating model accuracy. 

## Dataset

The [datasets](https://www.kaggle.com/netflix-inc/netflix-prize-data) of this project were released by Netflix in 2006. They can be found in the [Data](./Data) folder with the following name:

- [`combined_data_1`](./Data/combined_data_1.txt)
- [`combined_data_2`](./Data/combined_data_2.txt)
- [`combined_data_3`](./Data/combined_data_3.txt)
- [`combined_data_4`](./Data/combined_data_4.txt)
- [`movie_titles`](./Data/movie_titles.csv)

Besides, to determine similar movies for Movie Clustering, besides `movie_titles`, a separate [Kaggle dataset](https://www.kaggle.com/danielgrijalvas/movies) was utilized that contained additional characteristics for each movie, such as release country, genre, director, etc. It is stored in the [Data](./Data) folder as well:

- [`movies`](./Data/movies.csv)

The training dataset stored in files starting with `combined_data` contains over 100 million ratings from over 480,000 randomly-chosen, anonymous subscribers on nearly 18,000 movie titles. This dataset provides 4 key variables: *CustomerID*; *Rating*; *Date*; and *MovieID*.

## Files

This project was done in Python with three jupyter notebooks.

- [`Data_Analyses`](./Data_Analyses.ipynb)
- [`Data_Manipulation`](./Data_Manipulation.ipynb)
- [`Recommendation_Systems`](./Recommendation_Systems.ipynb)

`Data_Analyses` is aimed to do some basic data cleaning and analyses to the training dataset. 

`Data_Manipulation` exists because due to the memory limitation of personal computers, some manipulations could not be conducted on such a large dataset. Thus, a subset of the matrix was used for this project. This jupyter notebook implements the process of matrix cutting and saving. Finally, it will save the matrix that contains 4,642 customers and 2,784 movies as [target.csv](./Data/target.csv).

`Recommendation_Systems` will build the corresponding recommendation systems mentioned in the Introduction part.

## Results

The MSE results are shown in the table.

|Model|MSE|
|:---:|:-:|
|User-based CF|0.8167|
|Item-based CF|0.7445|
|Customer Clustering|0.6227|
|Movie Clustering|0.7158|
|Biclustering|0.5917|
|SVD|0.4290|
|Funk SVD|0.6159|
|NMF|0.6499|