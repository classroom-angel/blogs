# Friday March 22, 2019 - End of Week 1

## Individual Accomplishments this Sprint

This Sprint, I helped with the product canvas and building out the back end along with John. I deployed the back end development branch to Heroku, created knex setup and database configuration, made my own local database, created a user seed for 500 fake users, hashed passwords for register, added a login endpoint, and hashed passwords and return a JSON web token for login. A lot of the work was repeating code I could reference from the back end portion of Web Development, and Faker was new to me (I’d only heard of it, never used it). The hardest past for me was getting my Docker set up properly so I could make a local PostgreSQL database to test out my seed.

## Detailed Analysis

For the login API, I referred to old code to get the JWT (JSON web token) and bcrypt going properly. I required (used) three things, the database, JWT, and bcrypt, the hashing package. Then I have a function for generating a token that takes in a user from the database as an argument. Lastly, I have a login endpoint, which is a GET method. It pulls in the username and password from the request body, then queries the database for the first user where the username matches one in the database. If there is a user and the passwords match, a JSON web token is returned. Otherwise, you get an error message back: “You shall not pass!” There’s also a catch for any errors that might happen.

![login code](/images/login-code.png)

## Milestone Reflections

I helped with a bunch of the parts of the product canvas/technical design document. We started by explaining what problem we were attempting to solve and how our application would do that. Then we defined out user roles and what permissions they needed. We moved on to our features and explaining which users have access to them, what internal and external APIs we’d use, and I did a lot of the user stories. We worked on the views that different users see at different stages of use. Then we moved on to architecture choices. We decided on technologies that were taught during the course, but we’re going with React Hooks (new) and Material UI (we haven’t really used this). John and I built the data model section (he did the breakdown of each part). We worked on the weekly outline, the summary, and finally, the competitor landscape.

## Pull Requests/Trello cards

- [Hash passwords Trello](https://trello.com/c/3isYvQqI)
- [Hash passwords PR](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/14)

- [Add login API Trello](https://trello.com/c/21mF5yFi)
- [Add login API PR](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/15)

- [Mock user data with Faker Trello](https://trello.com/c/xvjRYywQ)
- No pull request for this one, I merged into our development branch without making a feature branch.

- [Create knex config and database config Trello](https://trello.com/c/t3B0gGe6)
- [Create knex config and database config Trello](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/5)

