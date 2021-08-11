# The-Smartest-Among-Us-Refactor

[![project-languages-used](https://img.shields.io/github/languages/count/diegopie/The-Smartest-Among-Us?color=important)](https://github.com/diegopie/The-Smartest-Among-Us)
[![project-top-languages-used](https://img.shields.io/github/languages/top/diegopie/The-Smartest-Among-Us?color=important)](https://github.com/diegopie/The-Smartest-Among-Us)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

!["play" screen of app](./public/assets/img/app.png)

## Description

Talk about using the site and whatnot

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
Frontend – React, socket.io-client, Bootstrap, React-icons, React-Toastify, use-sound, uuid 
Backend – Node, express, socket.io
Database – Mongodb, Mongoose
Authentication – Express-session, passport-local, bcrypt
Testing – react-testing-library, jest, supertest
```

### Installation

Blaw blaw and how to set up the first user and quiz (seeds folder)

&NewLine;
&NewLine;

### Dependencies/Packages

&NewLine;
&NewLine;

| | | | |
| ------ | ------ | ------ | ------ |
| [bcryptjs](https://www.npmjs.com/package/bcryptjs) | [bootstrap](https://www.npmjs.com/package/bootstrap) | [concurrently](https://www.npmjs.com/package/concurrently) | [dotenv](https://www.npmjs.com/package/dotenv) |
| [express](https://www.npmjs.com/package/express) | [express-session](https://www.npmjs.com/package/express-session) | [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken) | [mongoose](https://www.npmjs.com/package/mongoose) |
| [passport](https://www.npmjs.com/package/passport) | [passport-local](https://www.npmjs.com/package/passport-local) | [react-bootstrap](https://www.npmjs.com/package/react-bootstrap) | [react-icons](https://www.npmjs.com/package/react-icons) |
| [react-loader-spinner](https://www.npmjs.com/package/react-loader-spinner) | [socket.io](https://www.npmjs.com/package/socket.io) | [socket.io-client](https://www.npmjs.com/package/socket.io-client) |
| [Use-sound](https://www.npmjs.com/package/use-sound) | [uuid](https://www.npmjs.com/package/uuid) | [yarn](https://www.npmjs.com/package/yarn) |

&NewLine;
&NewLine;

#### Dev Dependencies

&NewLine;
&NewLine;

| | | | |
| ------ | ------ | ------ | ------ |
| [eslint](https://www.npmjs.com/package/eslint) | [jest](https://www.npmjs.com/package/jest) | [Jest Testing Library](https://jestjs.io/docs/en/getting-started) |[nodemon](https://www.npmjs.com/package/nodemon) |
| [React-Testing-Library](https://testing-library.com/docs/react-testing-library/intro/) | [supertest](https://www.npmjs.com/package/supertest) |

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

We use a Mongo database to service our application, with Robo3T being our interface of choice.

![Database Map](./assets/DB_Map-01.png)

#### Routes

This app relies on dozens of API routes to manage each feature. They too are exported from an index.js file for simplicity. Obviously, each file using API routes for that specific feature. auth is shorthand for authenticated user and manages login, signup, search, etc.

#### Authentication

Express-session, Passport, Passport-Local Strategy, bcryptjs

### Client

We use react.js to build our front-end interface. We have custom linting rules beyond what react defaults with and a basic service worker to manage the PWA usage.

## Future Development

We have a lot planned for the future of this application. This MVP was built as a school project but we aim to continue working on this to enjoy with our friends! We use Jira to organize our development time and have our next sprint planned out. Here are some highlights

## Contributors

We are a small team who just recently began coding as part of the University of Utah's Coding Bootcamp. Our goal for this project to be ambitious, to take just 7 short week of development time and create an application that is unique. Something that forced us to learn well beyond our skills at the time. We are passionate about coding and are eager to continue to develop our skills.

![Diego H.](./assets/dh.jpg) Diego Hernandez || [GitHub](https://github.com/Diegopie) || [LinkedIn](https://www.linkedin.com/in/diego-hernandez-7327381b2/)

![Diego H.](./assets/ds.jpg) Diana Schull || [GitHub](https://github.com/dianalynshull)

![Diego H.](./assets/bz.jpg) Bing Z. || [GitHub](https://github.com/imbingz)

## Contact

If you have any feedback our questions, please reach us at diegopie@outlook.com!

## License

This project is [MIT](https://choosealicense.com/licenses/mit/) licensed
