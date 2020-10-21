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

The datasets of this project were released by Netflix in 2006. Some of them can be found in the [Data](./Data) folder. The relevant datasets are:

- [`combined_data_1.txt`](https://www.kaggle.com/netflix-inc/netflix-prize-data)
- [`combined_data_2.txt`](https://www.kaggle.com/netflix-inc/netflix-prize-data)
- [`combined_data_3.txt`](https://www.kaggle.com/netflix-inc/netflix-prize-data)
- [`combined_data_4.txt`](https://www.kaggle.com/netflix-inc/netflix-prize-data)
- [`movie_titles.csv`](./Data/movie_titles.csv)

Part of the data cannot be found in the [Data](./Data) folder due to the limitation of Github file size.

Also, to determine similar movies for Movie Clustering, a separate [Kaggle dataset](https://www.kaggle.com/danielgrijalvas/movies) besides `movie_titles.csv` was utilized that contained additional characteristics for each movie, such as release country, genre, director, etc. It is called `movies.csv` and is saved in the [Data](./Data) folder.

- [`movies.csv`](./Data/movies.csv)

The training dataset stored in files starting with 'combined_data' contains over 100 million ratings from over 480,000 randomly-chosen, anonymous subscribers on nearly 18,000 movie titles. This dataset provides 4 key variables: *CustomerID*; *Rating*; *Date*; and *MovieID*.

## Files

This project was carried out in Python with three jupyter notebooks.

- [`Data_Cleaning.ipynb`](./Data_Cleaning.ipynb)
- [`Data_Manipulation.ipynb`](./Data_Manipulation.ipynb)
- [`Recommendation_Systems.ipynb`](./Recommendation_Systems.ipynb)

`Data_Cleaning.ipynb` is aimed to do some basic data cleaning and analyses to the training dataset. 

`Data_Manipulation.ipynb` exists because due to the memory limitation of personal computers, some manipulations could not be conducted on such a large dataset. Thus, a subset of the matrix was used for this project. This jupyter notebook implements the process of matrix cutting and saving. Finally, it will save the submatrix that contains 4,642 customers and 2,784 movies as [target.csv](./Data/target.csv).

`Recommendation_Systems.ipynb` will build the corresponding recommendation systems mentioned in the [Introduction](https://github.com/Mingxuan-Yang/Movie-Recommendation-Systems#introduction) part.

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