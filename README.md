# MangaVerse API

The **MangaVerse API** is your ultimate gateway to a vast collection of manga data, designed for developers and enthusiasts who want to explore, analyze, and integrate manga information into their applications. With a user-friendly interface and a comprehensive database, you can access details about titles, authors, genres, chapters, and more.

## Getting Started

1. **Sign Up**: Create an account on RapidAPI.
2. **Subscribe**: Choose a pricing plan that suits your needs.
3. **API Key**: Obtain your unique API key to start making requests.
4. **Documentation**: Check out the [MangaVerse API Documentation](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/mangaverse-api1) for detailed usage instructions.


## Key Features

- **Extensive Database**: Access a wide range of manga titles and their associated metadata.
- **Search Functionality**: Easily search for manga by title, genre, or author.
- **Chapter Information**: Retrieve detailed information about chapters, including summaries and release dates.
- **User Reviews and Ratings**: Get insights from the community with user-generated reviews and ratings.


## Mangaverse Endpoint: /search

### Description:
This endpoint enables users to search for manga or anime titles based on a query string. It expects a 'query' parameter in the request URL.

### Request:
- **Method:** GET
- **Path:** /search
- **Query Parameters:**
  - `query` (mandatory): The search query string.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing search results matching the query.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the query parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the search process.



## Mangaverse Endpoint: /info

### Description:
This endpoint is designed to retrieve information about a manga or anime by its title. It accepts a query parameter 'title' which is mandatory. Additionally, it optionally accepts a 'bestMatch' parameter, defaulted to true. If 'bestMatch' is set to false, it will search for partial matches.

### Request:
- **Method:** GET
- **Path:** /info
- **Query Parameters:**
  - `title` (mandatory): The title of the manga or anime.
  - `bestMatch` (optional): Determines whether to search for the best match (default: true).

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing information about the manga or anime.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the title parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.



## Mangaverse Endpoint: /manga/details

### Description:
This endpoint retrieves detailed information about a manga based on its ID.

### Request:
- **Method:** GET
- **Path:** /manga/details
- **Query Parameters:**
  - `id` (mandatory): The ID of the manga for which details are requested.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing detailed information about the specified manga.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the id parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.



## Mangaverse Endpoint: /news

### Description:
This endpoint retrieves news related to anime, providing insights into recent developments, announcements, and events. It supports pagination using the 'limit' query parameter to specify the number of news entries to fetch. By default, it returns the latest 120 entries.

### Request:
- **Method:** GET
- **Path:** /news
- **Query Parameters:**
  - `limit` (optional): Number of news entries to retrieve. Defaults to 120 if not provided.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing news entries based on the specified limit.

- **Error Response:**
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.



## Mangaverse Endpoint: /episodes

### Description:
This endpoint fetches a list of episodes for a given anime title. It requires the 'title' query parameter to be provided in the request URL.

### Request:
- **Method:** GET
- **Path:** /episodes
- **Query Parameters:**
  - `title` (mandatory): The title of the anime for which episodes are requested.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing a list of episodes for the specified anime title.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the title parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.



## Mangaverse Endpoint: /genre-list

### Description:
This endpoint retrieves a list of available genres in the manga database.

### Request:
- **Method:** GET
- **Path:** /genre-list

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing a list of genres available in the manga database.

- **Error Response:**
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.



## Mangaverse Endpoint: /manga/genre

### Description:
This endpoint retrieves manga based on a specified genre. It requires the 'genreId' query parameter to be provided in the request URL.

### Request:
- **Method:** GET
- **Path:** /manga/genre
- **Query Parameters:**
  - `genreId` (mandatory): The ID of the genre for which manga titles are requested.
  - `page` (optional): The page number for paginated results. Defaults to page 1 if not provided.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing manga titles based on the specified genre and pagination parameters.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the genreId parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.



## Mangaverse Endpoint: /manga/characters

### Description:
This endpoint retrieves information about characters featured in a manga based on its ID.

### Request:
- **Method:** GET
- **Path:** /manga/characters
- **Query Parameters:**
  - `id` (mandatory): The ID of the manga for which character information is requested.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing information about characters featured in the specified manga.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the id parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.



## Mangaverse Endpoint: /manga/stats

### Description:
This endpoint retrieves statistical information about a manga based on its ID, providing insights into its popularity, ratings, and other relevant metrics.

### Request:
- **Method:** GET
- **Path:** /manga/stats
- **Query Parameters:**
  - `id` (mandatory): The ID of the manga for which statistical information is requested.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing statistical information about the specified manga.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the id parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.



## Mangaverse Endpoint: /manga/review

### Description:
This endpoint retrieves reviews for a manga based on its ID, with support for pagination.

### Request:
- **Method:** GET
- **Path:** /manga/review
- **Query Parameters:**
  - `id` (mandatory): The ID of the manga for which reviews are requested.
  - `page` (optional): The page number for paginated results. Defaults to page 1 if not provided.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing reviews for the specified manga, optionally paginated.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the id parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.




## Mangaverse Endpoint: /manga/recommendation

### Description:
This endpoint retrieves recommendations for a manga based on its ID, suggesting other manga titles that users might enjoy.

### Request:
- **Method:** GET
- **Path:** /manga/recommendation
- **Query Parameters:**
  - `id` (mandatory): The ID of the manga for which recommendations are requested.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing recommendations for the specified manga.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the id parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.


## Mangaverse Endpoint: /manga/interest-stacks

### Description:
This endpoint retrieves interest stacks for a manga based on its ID, allowing users to see what other manga titles readers of the specified manga are interested in.

### Request:
- **Method:** GET
- **Path:** /manga/interest-stacks
- **Query Parameters:**
  - `id` (mandatory): The ID of the manga for which interest stacks are requested.
  - `page` (optional): The page number for paginated results. Defaults to page 1 if not provided.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing interest stacks for the specified manga, optionally paginated.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the id parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.




## Mangaverse Endpoint: /manga/news

### Description:
This endpoint retrieves news related to a specific manga based on its ID, providing updates, announcements, and other relevant information.

### Request:
- **Method:** GET
- **Path:** /manga/news
- **Query Parameters:**
  - `id` (mandatory): The ID of the manga for which news is requested.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing news related to the specified manga.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the id parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.


## Mangaverse Endpoint: /manga/forum

### Description:
This endpoint retrieves forum discussions related to a specific manga based on its ID, allowing users to engage with other fans and discuss various aspects of the manga.

### Request:
- **Method:** GET
- **Path:** /manga/forum
- **Query Parameters:**
  - `id` (mandatory): The ID of the manga for which forum discussions are requested.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing forum discussions related to the specified manga.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the id parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.



## Mangaverse Endpoint: /manga/clubs

### Description:
This endpoint retrieves clubs or groups dedicated to discussing or sharing content related to a specific manga based on its ID.

### Request:
- **Method:** GET
- **Path:** /manga/clubs
- **Query Parameters:**
  - `id` (mandatory): The ID of the manga for which clubs are requested.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing clubs or groups related to the specified manga.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the id parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.



## Mangaverse Endpoint: /manga/pictures

### Description:
This endpoint retrieves pictures or images related to a specific manga based on its ID, providing visual content such as artwork, covers, and promotional materials.

### Request:
- **Method:** GET
- **Path:** /manga/pictures
- **Query Parameters:**
  - `id` (mandatory): The ID of the manga for which pictures are requested.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing pictures or images related to the specified manga.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the id parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.



## Mangaverse Endpoint: /manga/more-info

### Description:
This endpoint retrieves additional information or details about a specific manga based on its ID, providing insights beyond basic metadata.

### Request:
- **Method:** GET
- **Path:** /manga/more-info
- **Query Parameters:**
  - `id` (mandatory): The ID of the manga for which additional information is requested.

### Response:
- **Success Response:** 
  - **Status:** 200 OK
  - **Content:** JSON containing additional information about the specified manga.

- **Error Response:**
  - **Status:** 400 Bad Request
  - **Content:** JSON with a message indicating the absence of the id parameter.
  
  - **Status:** 500 Internal Server Error
  - **Content:** JSON with an error message if an unexpected error occurs during the retrieval process.

## Commonly Asked Questions

### 1. What kind of data can I access through the MangaVerse API?
You can access information about manga titles, chapters, authors, genres, and user reviews.

### 2. How do I authenticate my API requests?
You will need to include your API key in the headers of your requests as specified in the API documentation.

### 3. Are there any usage limits for the API?
Yes, usage limits depend on the subscription plan you choose. Refer to the RapidAPI dashboard for specific limits.

### 4. Can I filter manga by genre?
Yes, the API provides filtering options to search for manga by different genres.

### 5. Is there support for multiple languages?
The MangaVerse API primarily supports data in English, but some titles may be available in other languages. Check individual title entries for language availability.

For more information and to start using the MangaVerse API, visit [MangaVerse API on RapidAPI](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/mangaverse-api1).

