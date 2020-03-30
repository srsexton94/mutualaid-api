
# Mutual Aid, Dual Power: Server Side
## Project Description
This project is a social networking app that is designed to support Mutual Aid network organizing efforts.  Recently, in the wake of the COVID-19 global crisis, Mutual Aid networks and resources have emerged all over the world.  However many of the networks are disconnected and there isn’t a prominent common resource connecting/compiling this information.

This app is intended to stand as a both a network in and of itself, as well as a compilation of other networks and resources to help get users connected to the resources they need, in the medium that works for them.

This repo is the API for this project... <!-- add more descriptive info -->

## Project Links <!-- add as finised -->
* [Front End Repo](https://github.com/srsexton94/mutualaid-client)

## Technologies

## Dependencies
* [GA Express Api Template]()
* `npm install`, `-g nodemon`
* `npm run server`, starts express server
* `npm test`, runs automated tests
* `npm run debug-server`, prints extra info on whats happening
* `npm install aws-sdk`, installs aws-sdk
* `npm install dotenv`, installs dotenv
* `npm install multer`, installs multer
* [GA Express Api Deployment Guide](https://git.generalassemb.ly/ga-wdi-boston/express-api-deployment-guide)

## Set Up
```
// install dependencies
npm install

// ensure nodemon is installed
npm install -g nodemon

// ensure API is functioning
npm run server
```

## User Stories
- As an unregistered user I want to be able to
  - view all public posts and access their content/links
  - sign up/create an account
- As a registered user I want to be able to sign in
- As a signed-in user I want to be able to...
  - sign in, update my info, & sign out
  - view all posts
  - view a specific subdivision of posts
  - view a specific post
  - create, update, and delete my own posts

#### MVP
* Provide sign up/in/out and change password
* Display all posts, view a single post, update/delete your ownpost

#### Moderate Stretch Goals
* Display all posts sorted by type (tabs in wireframes)
* Sort posts by time AND location
* Add tags? Or search bar?
* Add comments resource to posts
* Update entire account information, not just password
* Add user profile pictures/photos in posts

#### Stretch "for the stars!" Goals
* Offer “forgot password?” change to un-signed in users
* Offer google/facebook authentication
* Display networks and/or offer posts on a map

## ERD
![](./images/erd.png)

### Extra Guidance
`server.js` - where the actual Express `app` object is created, where
the middlewares and routes are registered, etc..
If you want to add any middlewares to your app, do that here.

`app/` contains models (mongoose) & route files. To create your own model, see
`app/models/example.js`. Route files are like controllers but include serialization/HTTP requests.

`config/db.js` is where you specify the name/URL of your database.

`lib/` is for code that will be used in other places in the app.
- `auth.js` has token authentication code
- `custom_errors.js` creates custom error classes (add your own!)
- `error_handler.js` catches errors (ie `.catch`es) & sets response status code
