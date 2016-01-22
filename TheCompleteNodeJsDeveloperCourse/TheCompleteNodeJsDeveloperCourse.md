# The Complete NodeJs Developer Course

![alt text](gitSilhuette.PNG)
## Section: 1 - What You'll Learn
### Lecture 1: What You'll Learn

### Lecture 2: About The Teacher: Andrew Mead

## Section: 2 - Getting Setup & Hello World

### Lecture 3: Installing Node.js and Sublime

### Lecture 4: Using the Terminal (OS X & Linux)

### Lecture 5: Using the Terminal (Windows)

### Lecture 6: Hello World!

## Section: 3 - Introduction to Node.js

### Lecture 7: What is Node.js?

### Lecture 8: Creating Variables

### Lecture 9: Strings

### Lecture 10: Numbers

### Lecture 11: If Statments

### Lecture 12: Functions

### Lecture 13: Objects
### Lecture 14: Project: Bank Account
### Lecture 15: Booleans
### Lecture 16: Undefined
### Lecture 17: Arrays
### Lecture 18: Project Setup: Bank Account 2
### Lecture 19: Project Solution: Bank Account 2
### Lecture 20: For & While Loops
### Lecture 21: Variable Scope
### Lecture 22: Closures
### Lecture 23: Project Setup: Bank Account 3
### Lecture 24: Project Solution: Bank Account 3

## Section: 4 - Getting Input & Storing Data
- npm install yargs@3.15.0 --save
### Lecture 25: Creating an npm based app
### Lecture 26: Using 3rd party libraries in your app
### Lecture 27: Project: Password Manager 1
### Lecture 28: Getting Input From User
### Lecture 29: Validating & Requiring Input
### Lecture 30: Project Setup: Password Manager 2
### Lecture 31: Project Solution: Password Manager 2
### Lecture 32: Working with JSON
### Lecture 33: Encrypting Information
- hashing
### Lecture 34: Project: Password Manager 3
### Lecture 35: Handling Errors
### Lecture 36: Project: Password Manager 4

## Section: 5 - Asynchronous Programming
### Lecture 37: Async Basics
### Lecture 38: Callback Functions
- npm install request@2.6.0 --save

### Lecture 39: Requiring local files
### Lecture 40: Project: Weather App 1
- IP service with API ipinfo.io
    - curl ipinfo.io
    - see lecture 53 (using _PostMan_ app)

### Lecture 41: Project: Weather App 2
- npm install yargs@3.15.0 --save
### Lecture 42: Promises
### Lecture 43: Advanced Promises
### Lecture 44: Project: Weather App 3

## Section: 6 - Creating A Web Server With Express.js
### Lecture 45: Hello Express.js
- install express
    - _projectDir\webServer_ >npm install express@.13.2 --save

### Lecture 46: Serving Up Static Websites
### Lecture 47: Middleware Is Awesome
### Lecture 48: Using Git
### Lecture 49: Project: Server Middleware
### Lecture 50: Generate SSH, join Heroku & GitHub
### Lecture 51: Deploying Your Application

## Section: 7 - Project: Todo REST API
### Lecture 52: Installing Postman
### Lecture 53: Getting All Todos
- using PostMan app
- see lecture 40 (using _curl_ cmd utility)
### Lecture 54: Get Todo By Id
### Lecture 55: Postman Environments
### Lecture 56: Creating New Todos
- install body-parser
    - npm install body-parser@1.13.3 --save
### Lecture 57: Refactoring With Underscore
- install Underscore to deal with objects and arrays
    - npm install underscore --save
    - var _=require("underscore");
    - var match = _.findWhere(list,{id:1});
### Lecture 58: Underscore Challenge
### Lecture 59: Deleting Todos By Id
### Lecture 60: Updating Todos
### Lecture 61: Passing Variables By Reference
### Lecture 62: Filtering By Todo Completed Status
### Lecture 63: Searching By Todo Description

## Section: 8 - Working With A Real Database (and adding it to the Todo API)
### Lecture 64: Sublime Text Bonus!
### Lecture 65: Installing Sequelize and Sqlite
- the source code in c:\WebstormProjects\TheCompleteNodeJsDeveloperCourse\node-8-2-sequelize\
- npm install sequelize@3.5.1 --save
- npm install sqlite@3.0.10 --save
- go to sqlitebrowser.org

### Lecture 66: Adding Model Validation & Fetching Models
### Lecture 67: Project: POST /todos
### Lecture 68: Project: GET /todos/:id
### Lecture 69: Project: GET /todos
### Lecture 70: Postgres On Heroku
- install postgres database

    heroku addons:create heroku-postgresql<br>
    heroku pg:wait<br>
    npm install pg@4.4.1 --save<br>
    npm install pg-hstore@2.3.2 --save<br>
    var env = process.env.NODE_ENV<br>

- Google 'heroku dialect mysql' lot of interesting stuff about running even java spring apps on heroku

### Lecture 71: Project: DELETE /todos/:id
### Lecture 72: PUT /todos/:id
## Section: 9 - Adding Authentication
### Lecture 73: Creating the User Model
### Lecture 74: Using Sequelize Hooks For Validation
- sequelize Hooks for validation, 'toLowerCase'
### Lecture 75: Hashing and Salting Passwords
- use _bcrypt_ module for 'crypting' ('hashing' discussed earlier in Lecture 33)
    - npm install bcrypt@0.8.5 -- save
![inst](bcryptInstall.png)
### Lecture 76: POST /users/login
### Lecture 77: Custom Sequelize Class Methods
### Lecture 78: Generating a JWT For Authentication
### Lecture 79: Making Todo Routes Private
- adding middleware to add user to any request by parsing token
### Lecture 80: Playing With Associations
- Intro to associations (many to one <-> user has many todos) within playground\basic-sqlite-database.js 
### Lecture 81: Associating Users With Their Todo
- add associations (many to one <-> user has many todos) to app db.js module
### Lecture 82: Associating Users With Their Todo Pt. 2
### Lecture 83: Deploying To Heroku
### Lecture 84: Logout Part 1
- create module model\token.js
- to secure token use crypto-js to hash token
- create table to store hashed tokens
- in server.js in /users/login store token

### Lecture 85: Logout Part 2

## Section: 10 - Socket.io, The Front-end, and A Chat App
### Lecture 86: Getting Started
- npm install express@4.13.3 --save
### Lecture 87: Adding Socket.io To Your App
- install jQuery
- install socket javascript library from https://cdn.socket.io/socket.io-1.3.7.js
    -- select all, save as file <project>\public\js\socket.io-1.3.7.js

### Lecture 88: Exploring The Front-end
### Lecture 89: Sending Live Data Back & Forth
### Lecture 90: Creating The Front-end UI
### Lecture 91: Showing Messages In App
### Lecture 92: Working With Time
- moment.js from momentjs.com 
### Lecture 93: Timestamps
- epochconverter.com to play unix timestamp
- get timestamp from moment 
    - _now.format('X')_ unix timestamp in sec    
    - _now.format('x')_ OR _now.valueof()_ unix timestamp in millisec
    - moment.utc(timestamp) get time from unix timestamp

### Lecture 94: Show Message Time In Chat App

### Lecture 95: Parsing Query Params
- small query parse support util gist.github.com/andrewjmead -> QueryParam.js -> click btn 'Raw' -> save as QueryParam.js
### Lecture 96: Showing Names
- use _action='chat.html'_ in form tag to redirect with form submitted par-rs
### Lecture 97: Add A Join Page
### Lecture 98: Chat Room Names
- use regular expression str.replace(/\+/g, ' ')
    - / - start and end of regex
    - g after ent slash is the _global_ modifier (to replace globally)
    - \+ - escape plus sign with is special character in regex
    - thus __/\+/g__ means replace '+' in whole input string
    - look mozilla developer org for regex syntax
    
### Lecture 99: Connecting To A Room
- socket emit custom message  _join room_ 
    - socket.join(roomName)
    - socket.brodcast.to(roomName).emit(message, {personNmae:'':message:'', timestamp:moment().valueOf()})
    - socket.id and socket.to
    
    
### Lecture 100: Send Disconnect Message
### Lecture 101: Adding @currentUser command
### Lecture 102: Bootstrap & Styling The Join Page
### Lecture 103: Styling The Join Page
### Lecture 104: Styling The Chat Page
### Lecture 105: Final Custom Styles

## Section: 11 - Bonus Preview: The Complete Web Developer Course
### Lecture 106: Intro
### Lecture 107: Hello World
### Lecture 108: Structure Of A Web Page
### Lecture 109: Your Own example.com
### Lecture 110: Header Tags
### Lecture 111: Paragraphs
### Lecture 112: Formatting Text
### Lecture 113: Unordered Lists
### Lecture 114: Ordered Lists
### Lecture 115: Images
### Lecture 116: Forms
### Lecture 117: Links
### Lecture 118: Tables
### Lecture 119: HTML Entities
### Lecture 120: IFrames
### Lecture 121: Putting It All Together: HTML Project

---
# Questions:
1. how to break server.js to _modules_ (in real app this file can grow pretty big)
2. how to setup/populate production database without manually insert or comment pieces of code in db.sequlize.sync({force:true})
    - is the answer in Lecture 83? The answer is: - Yes, use db.sequlize.sync({force:true}) in pushed code and initialize with separate http post requests.

