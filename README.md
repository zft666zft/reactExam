# Assignment 1 - ReactJS app

**Name**: Futong Zhu  
**Student Number**: 20108799  

## Overview

This repository contains a ReactJS-based movie application that allows users to browse, filter, search, and manage their favorite movie lists and watchlists. The application leverages the TMDB API to fetch dynamic movie data, providing multiple views, detailed pages, and interactive features.

#### Features
1. Introduced new pages (as shown in the uploaded images):
   - **Watchlist, Upcoming, Trending, Hot Movies, Top Rated** page tabs.
   - Extensive linking of information: On the Cast or Crew pages, you can click on names to navigate to their detailed profiles, and use "View Movies" to find films they participated in.
2. Interactive Favorites and Watchlist icons: Clicking these icons once adds the movie to the respective page. Clicking again removes it from the page.
3. Enhanced filter functionality (refer to the third uploaded image) with:
   - Rating and Release Year sliders.
   - A sorting dropdown for refined movie searches.
4. Implemented pagination to improve navigation across pages:
   - The middle page number in the pagination dynamically updates based on the total pages.
   - Users can enter a specific page number to jump directly to that page.
5. Efficient caching: Integrated `react-query` to cache data from all static and parameterized endpoints, reducing memory consumption.

## Setup requirements

To run the app locally after cloning the repository, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/zft666zft/react-movie-labs.git
   cd react-movie-labs
   cd movies
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up your TMDB API key in a `.env` file:
   ```env
   REACT_APP_TMDB_API_KEY=your_tmdb_api_key_here
   ```

4. Start the development server:
   ```bash
   npm start
   ```

5. Access the app at `http://localhost:3000`.

## API endpoints

Below are the TMDB endpoints used in the app in the order of your provided code:

+ **Discover movies**: `/discover/movie`  
  Fetches a list of movies with optional filters like language and sorting.

+ **Get movie details**: `/movie/:id`  
  Retrieves detailed information about a specific movie.

+ **Get genres**: `/genre/movie/list`  
  Provides a list of movie genres.

+ **Get movie images**: `/movie/:id/images`  
  Fetches images (posters, backdrops) for a specific movie.

+ **Get movie reviews**: `/movie/:id/reviews`  
  Retrieves reviews for a specific movie.

+ **Get upcoming movies**: `/movie/upcoming`  
  Fetches a list of upcoming movies.

+ **Get trending movies**: `/trending/movie/week`  
  Fetches a list of trending movies for the week.

+ **Get recommendations**: `/movie/:id/recommendations`  
  Provides recommended movies based on a specific movie.

+ **Get similar movies**: `/movie/:id/similar`  
  Retrieves movies similar to a specific movie.

+ **Get movie cast and crew**: `/movie/:id/credits`  
  Provides a list of cast and crew for a specific movie.

+ **Get actor movies**: `/person/:id/movie_credits`  
  Fetches a list of movies associated with a specific actor.

+ **Get hot movies**: `/movie/popular`  
  Retrieves a list of popular movies.

+ **Get top-rated movies**: `/movie/top_rated`  
  Fetches highly-rated movies.

+ **Get actor details**: `/person/:id`  
  Retrieves detailed information about a specific actor.

+ **Get movie videos**: `/movie/:id/videos`  
  Fetches trailers and other videos for a specific movie.

---

## Routing

Here is the list of supported routes and their associated pages:

+ `/` - Displays the home page with a list of movies.
+ `/movies/favorites` - Displays the user's favorite movies.
+ `/movies/watchlist` - Displays the user's watchlist.
+ `/movies/upcoming` - Displays a list of upcoming movies.
+ `/movies/trending` - Displays trending movies for the week.
+ `/movies/hot-movies` - Displays popular movies.
+ `/movies/top-rated` - Displays top-rated movies.
+ `/movies/:id` - Displays detailed information about a specific movie.
+ `/movies/:id/recommendations` - Displays movie recommendations.
+ `/movies/:id/similar` - Displays similar movies.
+ `/movies/:id/cast` - Displays the cast of the movie.
+ `/movies/:id/credits` - Displays detailed credits (cast and crew) for a specific movie.
+ `/movies/:id/videos` - Displays trailers and other videos for a specific movie.
+ `/reviews/form` - Allows users to write a review.
+ `/reviews/:id` - Allows users to view or edit an existing review.
+ `/actors/:id/movies` - Displays movies associated with a specific actor.
+ `/actors/:id/details` - Displays detailed information about a specific actor.


#### Independent Learning (If Relevant)
1. Interactive functionality for Favorites and Watchlist icons:
   - Clicking the icon once adds the movie to the respective list; clicking again removes it.
2. Pagination implementation:
   - The page number in the middle dynamically updates with the total number of pages.
   - Users can directly input a page number to jump to the desired page. 

These features were self-researched and implemented using online resources, enhancing the project's scope beyond the course material. Let me know if you'd like to add further refinements.