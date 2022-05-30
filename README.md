# NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING
This dataset consists of TV Shows and Movies available on Netflix as of 2021. The dataset is from Flixable
that is a third-party Netflix search engine. The attributes in the dataset are show_id, type, title, director, cast,
country, date_added, release_year, rating, duration, listed_in, and description. Exploratory data analysis and
clustering of similar content by matching text-based features are the objectives of the study.

After data loading, I searched for missing data and found several such rows in director, cast, country,
date_added, and rating. I imputed no_director, no_cast, and no_country in their respective features. After
that, I dropped all rows with missing values. To handle text-based features more efficiently, I combined the
names of two or more words using underscores. I found no duplicates in the data.

I gathered some inferences from exploratory data analysis. Movies and TV Shows on Netflix are in a ratio
of 7/3. Over the past five years, Netflix has shifted its focus toward TV shows. The number of movies added
to Netflix reduced by 45%, while the number of TV Shows added increased by 70%. Most content on Netflix
is from United States followed by India and United Kingdom. Jan Suter is the most featured director, while
Anupam Kher is the most featured actor. International movies is the top genre, followed by Dramas and
Comedies. Most movies are of the length of ~90 mins, while most TV Shows have only one season. Most
content on Netflix is mature audience only rated. Most content has a description length of ~140 words. Life,
young, new, family, and man are the top 5 most occurring words from the complete vocabulary of
description.

Next, I created three datasets 1st using the description feature alone, 2nd using the genres feature alone, and
3rd using country, rating, genres, and type features. I employed MiniBatchKMeans, Ward clustering,
Gaussian Mixture, and Spectral clustering. For the 1st dataset, I found 41 optimal clusters using Spectral
clustering. For the 2nd and 3rd datasets, I found 42 and 108 optimal clusters respectively, using Ward
clustering.

The Spectral clustering algorithm performed best on the large-sized dataset (1st). Ward clustering performed
best on the medium-sized datasets (2nd and 3rd). MiniBatchKMeans was the fastest clustering algorithm,
and it gave decent results on all the datasets. Gaussian Mixture clustering didn’t perform appreciatively.

Using the results of both Spectral and Ward clustering, I built a simple yet effective recommender system.
The system recommends top similar local content, top content with a similar genre, and content that you may
find interesting
