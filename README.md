# Analyzing-Movie-Reviews

In this project, we'll be working with Jupyter notebook, and analyzing data on movie review scores.

The dataset is stored in the `fandango_score_comparison.csv` file. It contains information on how major movie review services rated movies. The data originally came from [FiveThirtyEight](http://fivethirtyeight.com/features/fandango-movies-ratings/). 

Each row represents a single movie. Each column contains information about how the online moview review services [RottenTomatoes](http://rottentomatoes.com/), [Metacritic](http://metacritic.com/), [IMDB](http://www.imdb.com/), and [Fandango](http://www.fandango.com/) rated the movie.

The dataset was put together to help detect bias in the movie review sites. Each of these sites has 2 types of score -- <mark>User</mark> scores, which aggregate user reviews, and <mark>Critic</mark> score, which aggregate professional critical reviews of the movie. Each service puts their ratings on a different scale:

* RottenTomatoes - <mark>0-100</mark>, in increments of <mark>1</mark>.
* Metacritic - <mark>0-100</mark>, in increments of <mark>1</mark>.
* IMDB - <mark>0-10</mark>, in increments of <mark>.1</mark>.
* Fandango - <mark>0-5</mark>, in increments of <mark>.5</mark>.

Typically, the primary score shown by the sites will be the <mark>Critic</mark> score. Here are descriptions of some of the relevant columns in the dataset:

* <mark>FILM</mark> -- the name of the movie.
* <mark>RottenTomatoes</mark> -- the RottenTomatoes (RT) critic score.
* <mark>RottenTomatoes_User</mark> -- the RT user score.
* <mark>Metacritic</mark> -- the Metacritic critic score.
* <mark>Metacritic_User</mark> -- the Metacritic user score.
* <mark>IMDB</mark> -- the IMDB score given to the movie.
* <mark>Fandango_Stars</mark> -- the number of stars Fandango gave the movie.

To make it easier to compare scores across services, the columns were normalized so their scale and rounding matched the Fandango ratings. Any column with the suffix <mark>_norm</mark> is the corresponding column changed to a <mark>0-5</mark> scale.

For example, <mark>RT_norm</mark> takes the <mark>RottenTomatoes</mark> column and turns it into a <mark>0-5</mark> scale from a <mark>0-100</mark> scale.

Any column with the suffix <mark>_round</mark> is the rounded version of another column.

For example, <mark>RT_user_norm_round</mark> rounds the <mark>RT_user_norm</mark> column to the nearest <mark>.5</mark>.
