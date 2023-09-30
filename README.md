
# Up In Sports App
Web app in the beginning stages of being an all in one stop shot for everything 
sports. 
Right now the app allows for login/sign and GET for NBA data.

## Backend
**NodeJS Express**
The backend is written using NodeJs and Express.
api calls to external server are made through axios

You can find the our external API here: ['https://api-nba-v1.p.rapidapi.com]
on app start: an API call is made to the external api, and instantly loads data 
into local db. This was done for testing purposes as after so many
requests a fee is charged.

our models routes and schemas depict what data we get and how.

**postgresql**
Database of choice for this project is postgresql
.env file contains DATABASE_URL

## Frontend
**React JS**

# USER FLOW
1. In developement both servers need to be started and listening on different ports
2. backend immediately makes call to external api and loads local db with teams and players.
3. User interface is loaded to home page for user.
4. user signsup if not registered already, if registered logs in.
5. a token is generated from backend stored on our api class to set state in our upper App.js component.
6. this token is used to allow for access to teams and player routes and nav.
7. in develoment teams and players can be accessed regardless of token.
8. User context is stored at the top of the hierhchy on the frontend.
9. A separate api file is located on the frontend that makes requests to the server that the backend is listening for data requests to the frontend.
10. nvalink are proved to direct user flow options.
11. teams nav link leads to a list of all stored teams.
12. players nav link leads to a list of all stored players.
13. details are provided for both teams and players to view individual team or player details.
14. Those can be accessed through links in the list components. 
15. when a user signs up user profile data is stored in the users table of our db, and can be modified by user through a ProfileForm component.
16. our backend routes lead to database requests.
17. finally the user can logout at anytime and UserContext is set to null and so is the token.