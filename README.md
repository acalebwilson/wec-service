## WEC
A prototype website for Whitby Evangelical Church. A portfolio project.

This is the backend of a portfolio project, and is a prototype design for a local church website in need of improvement (at time of writing).

The site is a single page react app, created using create-react-app, with an express - nodejs backend, and with MongoDB as a database. The front end repo can be found here - https://github.com/acalebwilson/wec. A live version is available at https://acalebwilson.com. The project was of interest to me as a way to apply skills I had learned through the [freecodecamp](https://www.freecodecamp.org/) course as it involved both front and backend skills, and has greatly impoved my proficiency with HTML, CSS (SASS), JS (with React and nodejs on the backend), responsive web design, and given me a deeper understanding of both the web development process and software design in general.

### Authentication
I chose to use JWTs (JSON Web Tokens) in cookies for authentication as it made development simpler - express-session doesn't seem to enjoy the fact that the CRA app in development can't be served from the same server as the backend processes (or at least, I couldn't find a solution). On a successful login (through [passport-js](http://www.passportjs.org/)) a cookie is sent with a signed JWT which is checked on each subsequent request on a protected route, which easily meets the authentication requirements of what is needed for this project.  I chose to use JWTs in cookies for authentication as it made development simpler - express-session doesn't seem to enjoy the fact that the CRA app in development can't be served from the same server as the backend processes (or at least, I couldn't find a solution).

### Upload
The backend uploads audio files to the google cloud bucket associated with my live site, a url is returned and another request with the additional details is submitted by the client.


