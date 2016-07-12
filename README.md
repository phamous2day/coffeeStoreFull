# Coffee Site Frontend

Having done - mostly - the backend, you are going to now build the frontend of the Coffee website using AngularJS. This app will have multiple pages, which means you will need to use ngRoute.

## The Pages

The page you'll need to build are:

1. The home page, which explains to the user what the site is about, and why they should buy coffee from here.
2. The options page, where the user will select the grind type and quantity to buy.
3. The delivery page, where the user will enter the address to delivery the coffee to.
4. The payment page, where they will review the order and submit credit card payment.
6. Thank you page, where they are redirected to after they submit an other.
7. The login page, where the user will login to the site. The following pages will require the user to login before he can access them:
  * options page
  * delivery page
  * payment page
8. The register page, where the user will register for an account on the site so that he can login.

There are screenshots for each page. But feel free to make it look better!

## CORS Setup

You will setup the cors module with your express app, so that the backend can be accessed from a different domain. Read the instructions (code example) here: https://www.npmjs.com/package/cors.

For a detailed explanation of CORS, read https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS.

Once you have your backend set up with CORS, you will run your backend on a port of your choosing. You will start the frontend as a separate project in a separate directory. You will use the `serve` command to serve up the static files in your frontend project, you must use a different port number than the backend. To access the backend, you will need to use the full URL of the backend, for example:

// Base URL of the backend
var API = 'http://localhost:1337';

/* then elsewhere in your code */
$http.get(API + '/options')
  .success(function(data) {
    /* do stuff with data */
  });

## Frontend Setup

1. Setup your HTML file(s), JS files, CSS files, link them up.
2. Include angular.js and angular-route.js:
  * http://ajax.googleapis.com/ajax/libs/angularjs/1.5.7/angular.js
  * http://ajax.googleapis.com/ajax/libs/angularjs/1.5.7/angular-route.js
3. You will need angular-cookie.js as well:
  * http://ajax.googleapis.com/ajax/libs/angularjs/1.5.7/angular-cookies.js
4. Use bootstrap's CSS
5. Setup AngularJS app
  * create a module
  * attach that module to a DOM element using the ng-app directive
6. Setup ngRoute routing, the steps:
  * include the angular-route.js script
  * put "ngRoute" as a dependency of the AngularJS module you are using for the app
  * set up a config section that uses $routeProvider to setup the routes
  * setup all the routes and sub-page HTML files for each of the pages you need to build, listed in "The Pages" above. Just put in placeholder text for each one for now.

Run in your front end directory:

serve -p YOUR_PORT_NUMBER

To connect to your backend API - say your backend runs on http://localhost:3000, you will use

var API = 'http://localhost:3000';
$http.get(API + '/options')
  .success(function(data) {
    ...
  });

## The Home Page

Build the home page to look like the home-page.png screenshot. The bootstrap grid system could help:

https://getbootstrap.com/examples/grid/

The "Get Started" link should take you to the options page.

