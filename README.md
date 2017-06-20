# WDI-Project2-Shopping-Cart

Introduction:
1)This is the second project for WDI-10.
2) It will be a shopping cart/interface as seen from a buyer's point of view

Preliminaries:
1) MongoDB has to be installed (at terminal: npm install mongodb --save)
2) Run "sudo service mongod start" at project file in terminal first to create DB from product-seeder.js.
3) Run "npm start" at project file in terminal to begin listening.



---Progress Log

1) Progress updates on 19 June 2017
  a) Created static pages using "handlebars" - provides better visualization in Atom editor compared to Pug
  b) Setup "product-seeder.js" file to instantiate a 'document' for DB. This will create an array of seperate objects as listed in "var products"
  c) The array 'document' will later be manipulated in "index.js" (routes folder) to output items as per handlebars styling ("index.hbs").
    i) comments for array slicing and push inside "index.js"
  d) The handlebars styling has "# each" to loop through the referenced product array from "index.js".
  e) User sign in security by using CSRF method.
    i) link: https://github.com/expressjs/csurf
    ii) installed package at terminal: npm install csurf --save
    iii) CSRF requires express-sessions enabled to function. Link:https://www.npmjs.com/package/express-session
    iv) installed express-sessions at terminal: npm install --save express-session

2) Progress updates from 20 June 2017
  a) Create user signup/login functions with Passport package.
    i) installed Passport package at terminal: npm install passport --save
    ii) installed bcrypt package at terminal: npm install bcrypt --save
    iii)installed bcrypt-nodejs package at terminal: npm install bcrypt-node js --save
  b) To allow for message pop-ups during each session, recommended solution is to use "Connect Flash" middleware (note: cookieParser and Session middleware must be available)
    i) link: https://www.npmjs.com/package/connect-flash
    ii)installed connect-flash package at terminal: npm installed connect-flash --save
  c)installed Local Passport strategy at terinaml: npm install passport-local --save
  d)installed express-validator package to ensure valid email entries
    i) Link: https://github.com/ctavan/express-validator
    ii) At project file in terminal: npm install express-validator --save
  e)created validation for email and password input, and corresponding message output by flash into signup page view (using handlebars placeholder)
  e) created User signing in routes
