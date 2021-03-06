# The-Smartest-Among-Us-Refactor

[![project-languages-used](https://img.shields.io/github/languages/count/diegopie/The-Smartest-Among-Us?color=important)](https://github.com/diegopie/The-Smartest-Among-Us)
[![project-top-languages-used](https://img.shields.io/github/languages/top/diegopie/The-Smartest-Among-Us?color=important)](https://github.com/diegopie/The-Smartest-Among-Us)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

!["play" screen of app](./public/assets/img/app.png)

## Description

This my personal refactor of a project I worked on with two of my [colleagues](#Contributors). I'm happy with the work we did but I know there are opportunities for efficiency and I would like to eventually add more features to the site!

This application acts as a fun quiz site. Users can access global quizzes to familiarize themselves with the site and compete in a global leaderboard. They may also play randomly generated quizzes with many categories and options to choose from! Users can even save random quizzes they enjoy to their account, where they can try and beat their scores and share the quiz with their friends. Users can even create their own quiz, either by editing a random quiz they liked or creating one from scratch!
 

&NewLine;
&NewLine;

## Table of Contents

- [Development](#Development)
- [Bugs](#Bugs)
- [Future Development](#Future-Development)
- [Contributors](#Contributors)
- [Contact](#Contact)
- [Reference Material](#Reference-Material)
- [License](#License)

## Development

- [Technology Overview](#Technology-Overview)
- [Installation](#Installation)
- [Dependencies/Packages](#Dependencies/Packages)
- [Server](#Server)
- [Client](#Client)

### Technology Overview

&NewLine;
&NewLine;

```sh
Frontend – Handlebars, Bootstrap,  
Backend – Node, Express
Database – mySQL, Sequelize
Authentication – Express-session, passport-local, bcrypt
```

### Installation

If you'd like to play with this code you may fork this repo and run on your machines. You will need [node.js](https://nodejs.org/en/) and [mySQL](https://dev.mysql.com/downloads/mysql/) installed. Outside of cloning the project and installing the dependencies, there are a few things to take care of to get the app running.

- Create a mySQL database named quizapp
- run server.js in a node environment to create all the necessary SQL tables

Next is setting up the global quizzes. I plan to change this in the [future](#Future-Development), but to use the globally accessible quizzes we first need to create a user in the db, known as global, then create the quizzes using this first user as the creator. It's not very efficient but it allows us to write global leaderboards to the server and do server-side updates to the quizzes. I do all this in [Postman](https://www.postman.com/downloads/). Make sure you change the password! 😅

- To create the initial, global user, make a POST request to localhost:8080/api/user with raw JSON. The needed JSON can be found in db/seeds/user.json

`{
  "username":"global",
  "password": "impstr"
}`

- Now the quizzes can be created and assigned to this first user. Make a POST request to localhost:8080/api/quiz with raw JSON. Our JSON quiz files can be found in db/seeds/HKquiz.json and AUquiz.json, but you can create your own as well using this same setup. A template of how quizzes are stored in the database can be found in that same folder under quiz.json


&NewLine;
&NewLine;

### Dependencies/Packages

&NewLine;
&NewLine;

| | | |
| ------ | ------ | ------ |
| [bcryptjs](https://www.npmjs.com/package/bcryptjs) |  [dotenv](https://www.npmjs.com/package/dotenv) | [express](https://www.npmjs.com/package/express) |
| [express-handlebars](https://www.npmjs.com/package/express-handlebars) | [express-session](https://www.npmjs.com/package/express-session)  | [mysql2](https://www.npmjs.com/package/mysql2) |
| [passport](https://www.npmjs.com/package/passport) | [passport-local](https://www.npmjs.com/package/passport-local)  | [sequelize](https://www.npmjs.com/package/sequelize) |

&NewLine;
&NewLine;

#### Dev Dependencies

&NewLine;
&NewLine;

| | | |
| ------ | ------ | ------ |
| [eslint](https://www.npmjs.com/package/eslint) | [eslint-config-prettier](https://www.npmjs.com/package/eslint-config-prettier) | [eslint-plugin-prettier](https://www.npmjs.com/package/eslint-plugin-prettier)|
| [nodemon](https://www.npmjs.com/package/nodemon) | [prettier](https://www.npmjs.com/package/prettier) |

&NewLine;
&NewLine;

> [Back To Development](#Development) || [Back To Table of Contents](#Table-of-Contents)

### Server

- [Database](#Database)
- [Routes](#Routes)
- [Authentication](#Authentication)

#### Database

&NewLine;
&NewLine;

We use a SQL database to service our application, with mySQL and mySQL Workbench being our interface of choice.

![Database Map](./public/assets/img/dbmap.png)

#### Routes

Currently, all HTTP and API routes are in controller/routes.js. It's a fairly straightforward file that also handles the site's CRUD operators.

#### Authentication

Express-session, Passport, Passport-Local Strategy, bcryptjs

These packages are used to hash and secure user passwords. We also have simple redirects for when unauthenticated users hit a page they are not allowed to see.

> [Back To Server](#Server) || [Back To Development](#Development)

### Client

This app is rendered using Handlebars.js. It's not a very complex implementation but is of great help to render a user's saved quizzes from the database.

## Future Development

I have a few things in mind for this app, mostly just to optimize the current code then to add features.

- Organize the routes into their own files
- Rework creating and storing global quizzes
- Refactor the jQuery powering quiz rendering
- Give users custom styling options for their quizzes

## Contributors

The original repo can be found [here](https://github.com/Diegopie/The-Smartest-Among-Us)! We created this app as a school project with the University of Utah and I am forever grateful I was able to work with these two 😊!

Diego Hernandez || [GitHub](https://github.com/Diegopie) || [LinkedIn](https://www.linkedin.com/in/diego-hernandez-7327381b2/)

Seth Martineau || [GitHub](https://github.com/slothings)

Kay || [GitHub](https://github.com/theykay)

## Contact

If you have any feedback our questions, please reach me at diegopie@outlook.com!

## License

This project is [MIT](https://choosealicense.com/licenses/mit/) licensed
