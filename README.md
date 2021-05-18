# The-Movie-Cinema

![Python](https://img.shields.io/badge/Python-3.8-blueviolet)
![Framework](https://img.shields.io/badge/Framework-Flask-red)
![Frontend](https://img.shields.io/badge/Frontend-HTML/CSS/JS-green)
![API](https://img.shields.io/badge/API-TMDB-fcba03)

This application provides all the details of the requested movie such as overview, genre, release date, rating, runtime, top cast, reviews, recommended movies, etc.

The details of the movies(title, genre, runtime, rating, poster, etc) are fetched using an API by TMDB, https://www.themoviedb.org/documentation/api, and using the IMDB id of the movie in the API, I did web scraping to get the reviews given by the user in the IMDB site using `beautifulsoup4` and performed sentiment analysis on those reviews.

## Link to the application

Check out the live demo: https://the-movie-cinema.herokuapp.com/

## Note

Don't worry if the movie that you are looking for is not auto-suggested. Just type the movie name and click on "enter". You will be good to go even though if you made some typo errors.
Source code: https://github.com/Harshvardhan1999/The-Movie-Cinema/tree/master/Movie%20Recommendation%20System

## 'Invalid Request' Error

If you're getting invalid request error in your application, kindly note that there is nothing wrong with that error. There must be some other reason for the invalid request. There are several ways to track the issue.
1. If you make a request without the API key for the first time, your browser caches the request in the browser memory and throws an Invalid request error. Check whether you've replaced the API key in both the lines in the recommend.js file. Even though you replaced the API key for the next subsequent requests, your browser will always make use of the request from the browser cache.  If you did and still getting an invalid error, press 'ctrl+f5' (which clears the content of the browser cache) and try making a request again.
2. If that doesn't help you out, check the browser console. If you're getting a server-side error (error code should be greater than or equal to 500), check your command prompt (Windows) or terminal (Linux and Mac). That should define the cause.

## How to get the API key?

Create an account in https://www.themoviedb.org/, click on the `API` link from the left hand sidebar in your account settings and fill all the details to apply for API key. If you are asked for the website URL, just give "NA" if you don't have one. You will see the API key in your `API` sidebar once your request is approved.

## How to run the project?

1. Clone this repository in your local system.
2. Install all the libraries mentioned in the [requirements.txt](https://github.com/Harshvardhan1999/The-Movie-Cinema/blob/master/Movie%20Recommendation%20System/requirements.txt) file.
3. Get your API key from https://www.themoviedb.org/. (Refer the above section on how to get the API key)
4. Replace YOUR_API_KEY in **both** the places (line no. 23 and 43) of [static/recommend.js](https://github.com/Harshvardhan1999/The-Movie-Cinema/blob/master/Movie%20Recommendation%20System/static/recommend.js) file.
5. Open your terminal/command prompt from your project directory and run the [main.py](https://github.com/Harshvardhan1999/The-Movie-Cinema/blob/master/Movie%20Recommendation%20System/main.py) file by executing the command `python main.py`.
6. Go to your browser and type `http://127.0.0.1:5000/` in the address bar.
7. Hurray! That's it.

### Sources of the datasets 

1. [IMDB 5000 Movie Dataset](https://www.kaggle.com/carolzhangdc/imdb-5000-movie-dataset)
2. [The Movies Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset)
3. [List of movies in 2018](https://en.wikipedia.org/wiki/List_of_American_films_of_2018)
4. [List of movies in 2019](https://en.wikipedia.org/wiki/List_of_American_films_of_2019)
5. [List of movies in 2020](https://en.wikipedia.org/wiki/List_of_American_films_of_2020)

Thank you!
