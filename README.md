# Movie Swiper!

Movie Swiper is a movie recommendation web app that allows users to sign up, log in, and get personalized movie suggestions based on their preferences. Movie Swiper combines Firebase for user management with a third-party API for movie data to deliver a personalized movie suggestion engine in a web app interface. Users can easily find movies to watch tailored to their tastes.

Youtube video: https://www.youtube.com/@IhabElrayah/videos
live Demo: https://movie-swiper.netlify.app/


Summarised description of each file:

index.html - The main HTML page that contains the full login/registration form for new users to sign up or existing users to log in. Includes input fields for email, password, name, and movie preferences. Links to external CSS stylesheet and JavaScript files. 

index.js - Handles all front-end logic and interactions. Defines functions to register new users by storing info in Firebase, log in existing users by authenticating against Firebase, and validating form fields before submitting. Routes users to appropriate movie pages based on selected preferences. 

index.css - External CSS stylesheet that defines styling for the page layout, form container, header, input fields, buttons, and other visual elements on the index.html page. Uses custom fonts, gradients, and animations to create the visual style. 

reset_password.html - Forgot password page with email input and submit button in a simple form. When submitted, triggers the password reset process. Links to Firebase SDKs and accompanying JavaScript file. 

reset_password.js - Contains JavaScript to integrate with Firebase Authentication and send password reset emails. Email input is validated before reset email API is called. Reset password workflow is implemented here.

AA.html - The main HTML page for displaying Adventure/Action/Animation movies. Contains a header tag with title, and a div container to display the movie posters and titles dynamically loaded from the API. 

AA.js - Handles getting movie data from the RapidAPI movie database API. Makes an asynchronous GET request with the key and host headers. Parses the JSON response to extract movie titles and poster images. Passes these to a function to generate the HTML elements and render them on the page. 

Rapid API Moviee Database site: https://rapidapi.com/developer/analytics/Movies

AA.css - External CSS stylesheet that styles the overall page and movie items. Sets up a responsive grid layout with columns that adapt to screen size. Styles the background, text color, movie container dimensions, shadows, etc. Makes images responsive. 

comedy.html - Similar HTML page as AA.html but for displaying Comedy movies. Contains the same header and div structure that will be populated dynamically via the API. 

comedy.js - Fetches comedy movies by making the API request with a "comedy movie" query parameter. Reuses the same request logic and parsing as AA.js, only the query string differs. Renders comedy movies. 

comedy.css - Reuses the same CSS grid, responsive styling, and visual treatment as AA.css. The two pages share a consistent look.

package.json and package-lock.json define the project dependencies for making API calls. 

.env file contains sensitive Firebase config values needed by the app. Stored separately so it's not committed publicly. 

Fetch and Node-Fetch libraries are used to call external APIs and Firebase for user management and data storage. 

Configuration is split between dependencies (package.json) and secrets (.env) following security best practices
