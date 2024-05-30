The dataset has been extracted from the Netflix Prize data and netflix-prize-with-genres datasets available at the following links:
https://www.kaggle.com/datasets/netflix-inc/netflix-prize-data
https://github.com/tommasocarraro/netflix-prize-with-genres/blob/master/netflix_genres.csv

It contains a small subset with N = 200 customers (M = 1334 movies) and a large subset with N = 10000 customers (M = 4383 movies).

The data in the node tables represent the following variables:

ID: node identifier (the C prefix is used to denote customer nodes, and the M prefix is used to denote movie nodes)
Label: node label (identical to the node identifier)
Type: node type

The two following node types are used to form a bipartite network:

Customer: Netflix customer
Movie: Movie on Netflix

An expanded version of the node table for the large subset of customers (N = 10000) has been created which includes movie genre information from the netflix-prize-with-genres dataset ("topic4_node_list_genre_10000_customers.csv"). In this node table, the following node attribute has been added for movie nodes only:

MovieGenre: genre of the movie nodes represented by movie IDs. Notes: (i) the genre can be represented by multiple categories (e.g., Comedy|Drama|Romance), (ii) when no movie genre is available, the category "NA" is used, (iii) Customer nodes have no movie genre, therefore this attribute is left blank, (iv) the association between movie IDs and movie titles can be found in the "movie_titles.csv" file, (v) if you want to find more information about a specific movie, you can search the IMDb database using the movie title

The data in the edge table files represent the following variables associated to the original Netflix Prize data:

Source: CustomerID [string] - Netflix customers represented by randomly-assigned ids (for privacy)
Target: MovieID [string] - Movies watched by customers on Netflix, represented by identifiers
Weight: Rating from 1 to 5 stars [integer] - Ratings made by customers for movies they watched
Date: Date in the format YYYY-MM-DD [string] - Date of the customer ratings

Please refer to the Netlix Prize data web page for more information on the data.
