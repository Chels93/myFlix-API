myFlix API (movie_api):

OVERVIEW:
The myFlix API is the server-side component of a web application that provides users with information about movies, directors, and genres. Users can create accounts, manage their profiles, and curate a list of their favorite movies. Built using the MERN stack, the API follows REST architecture principles, offering secure and efficient access to movie-related data stored in a non-relational database. The application demonstrates proficiency in backend development, including server frameworks, database management, authentication, authorization, and data security.

INSTALLATION PREREQUISITES:
- Node.js
- MongoDB

FEATURES:
- Returns a list of all movies to the user
- Returns data (description, genre, director, image URL, whether it's featured or not) about a single movie by title to the user
- Return data about a genre (description) by name/title (e.g., "Comedy")
- Return data about a director (bio, birth year, death year) by name 
- Allow new users to register
- Allow users to update their user info (username, password, email, date of birth)
- Allow users to add a movie to their list of favorites
- Allow users to remove a movie from their list of favorites 
- ALlow existing users to deregister 

DEPLOYMENT:
- Install dependencies using: npm install
- Run the server using: npm start 
- Github link: https://github.com/Chels93/movie_api

TECHNICAL STACK:
- Node.js: Server runtime environment
- Express: Web framework for building RESTful APIs
- MongoDB: Non-relational database for storing movie and user data
- Mongoose: Object Data Modeling (ODM) library for MongoDB

API ENDPOINTS:
    Movies:
        HTTP Method	            Endpoint	                            Description
            GET	            /movies	                                Returns a JSON object list of all movies
            GET	            /movies/:Title	                        Returns data about a single movie by title
            GET	            /movies/genre/:genreName	            Returns data about a genre by name
            GET	            /movies/director/:directorName	        Returns data about a director by name
    Users:
        HTTP Method	            Endpoint	                            Description
            GET	            /users	                                Returns a list of all users
            POST            /users                                  Registers a new user and returns the user data along with a JWT token
            POST	        /login                                  Allows users to login
            PUT	            /users/:username	                    Allows users to update their user info
            GET	            /users/:username	                    Get user info by username 
            GET	            /users/:username/favoriteMovies         Get favorite movies for a specific user
            POST            /users/:username/movies/:movieId        Allows users to add a movie to their list of favorites
            DELETE          /users/:username/movies/:movieId        Allows users to remove a movie from thier list of favorites 
            DELETE          /users/:username                        Allows existing users to deregister


ENHANCEMENTS AND FUTURE PLANS:
- Add actor information and actor-based queries
- Include movie ratings and user reviews
- Build additional user interaction features like “To Watch” lists
- Optimize performance with caching mechanism

ACKNOWLEDGEMENTS:
- Movie data is inspired by public movie databases
- Project structure and design influenced by best practices in backend development
