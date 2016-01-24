# Projects In ExpressJS LearnExpressJsBuilding 10 projects

## Section: 1 - Introduction
### Lecture 1: Introduction

## Section: 2 - Simple Express Server
### Lecture 2: Project Intro
### Lecture 3: Environment Setup
### Lecture 4: Sending a Response
### Lecture 5: Static Web Server
### Lecture 6: Package.json & More Requests - Basics
### Lecture 7: Package.json & More Requests - Advance
## Quiz 1: Chapter 1

## Section: 3 - PC Repair Website
### Lecture 8: Project Intro
### Lecture 9: Express Generator
- see http://expressjs.com/en/starter/generator.html
    - npm install -g express-generator
    - express myapp
    - cd myapp
    - npm install
    - these commands layout project structure

    ├── app.js
    ├── bin
    │   └── www
    ├── package.json
    ├── public
    │   ├── images
    │   ├── javascripts
    │   └── stylesheets
    │       └── style.css
    ├── routes
    │   ├── index.js
    │   └── users.js
    └── views
        ├── error.jade
        ├── index.jade
        └── layout.jade     
    - and than _npm install_ to install required by generator
    - npm start
    - install bootstrap client side css and js
- html2jade.org - jadeconverter  

### Lecture 10: Jade Layouts
### Lecture 11: Fetching JSON
### Lecture 12: Nodemailer Contact
- Nodemailer github.com/andris9/Nodemailer

### Quiz 2: Chapter 2 ## Quiz

## Section: 4 - SportsBlog Application
### Lecture 13: Project Intro
### Lecture 14: MongoDB & Middleware
- install MongoDb from mongodb.org (download c:\WWWDownload\mongodb-win32-x86_64-2008plus-ssl-3.2.1-signed.msi)
    - open cmd as Administrator
    - cd C:\Program Files\MongoDB\Server\3.2\bin
    - create forlders in root c:\mongodb\data\db\
    - create log c:\mongodb\log\mongo.log

    C:\Program Files\MongoDB\Server\3.2\bin>mongod --directoryperdb --dbpath c:\mongodb\data\db --logpath c:\mongodb\log\mon
    go.log --logappend --rest --install
    2016-01-24T12:46:07.432-0500 I CONTROL  [main] ** WARNING: --rest is specified without --httpinterface,
    2016-01-24T12:46:07.432-0500 I CONTROL  [main] **          enabling http interface
    C:\Program Files\MongoDB\Server\3.2\bin>net start MongoDB
    The MongoDB service was started successfully.    
    
    - to stop service use > net stop MongoDB (or through control panel>services)
    - set path to c:\Program Files\MongoDB\Server\3.2\bin
    - verify in cmd >mongo and than
    
    >show databases<br>
    local  0.000GB

- add to package.json


     
    "connect-flash": "*",
    "express-messages":"*",
    "express-session":"*",
    "express-validator":"*",
    "moment":"*",
    "mongoose":"*"

- install nodemon: add "main": "bin/www" in  package.json

    >npm install -g nodemon
- npm install (all added modules)
    - gyp ERR! stack Error: Can't find Python executable "python", you can set the PYTHON env variable.
    - need come back and install python
        - python-3.5.1 to c:\WWWDownload
        - add path to C:\Users\Alexei\AppData\Local\Programs\Python\Python35-32   <-  python.exe
        
- nodemon in project folder        
- setup middleware in app.js (copy from downloaded project source zip)
- visit startbootstrap.com 
    - click browse theme and template
    - select Clean Blog and download<br>
    ![Clean Blog Theme](CleanBlogTheme.PNG)
    - copy css and javascript from zip
    - copy \fonts and \img from zip to public directory

### Lecture 15: Routes & Views - Basics
### Lecture 16: Routes & Views - Concepts

- Error in rendering. on 51st second not clear what indent should be in _pasted code_<br>
  ![Indent content](Indent.PNG)  
    - backup after fixing error c:\WebstormProjects\SportsBlog.src\SportsBlogBackupLecture16_1stMinute.zip
    
### Lecture 17: Routes & Views - Implementation
### Lecture 18: Categories - Basics
### Lecture 19: Categories - Concepts
### Lecture 20: Categories - Implementation
### Lecture 21: Articles - Introduction
### Lecture 22: Articles - basic Structure
### Lecture 23: Articles - Implementation
### Lecture 24: Articles - Final View
### Lecture 25: Comments
## Quiz 3: Chapter 3 ## Quiz

## Section: 5 - User Login System
### Lecture 26: Project Intro
### Lecture 27: Handlebars & Dependencies
### Lecture 28: User Interface - Basic
### Lecture 29: User Interface - Implementation
### Lecture 30: Registration - Initial Steps
### Lecture 31: Registration - Basic
### Lecture 32: Registration - Final Implementation
### Lecture 33: Login
## Quiz 4: Chapter 4 ## Quiz

## Section: 6 - Chat Using Socket.io
### Lecture 34: Project Intro
### Lecture 35: App & Dependency Setup
### Lecture 36: Bootstrap UI
### Lecture 37: Adding Usernames
### Lecture 38: Sending Chat Messages
## Quiz 5: Chapter 5 ## Quiz

## Section: 7 - ClientKeeper
### Lecture 39: Project Intro
### Lecture 40: Server & Client Files - Basic
### Lecture 41: Server & Client Files - Implementation
### Lecture 42: Getting the Clients
### Lecture 43: Getting the Clients - Final Steps
### Lecture 44: Adding Clients
### Lecture 45: Update & Delete Clients - Basics
### Lecture 46: Update & Delete Clients - Implementations
## Quiz 6: Chapter 6 ## Quiz

## Section: 8 - Job Board Using MEAN.js
### Lecture 47: Project Intro
### Lecture 48: Mean.js Setup
### Lecture 49: Creating the Jobs Module - Basics
### Lecture 50: Creating the Jobs Module - Implementation
### Lecture 51: List & Details View
### Lecture 52: Edit, Delete & Filtering
## Quiz 7: Chapter 7 ## Quiz

## Section: 9 - MovieBase Using Kraken
### Lecture 53: Project Intro
### Lecture 54: Kraken Setup
### Lecture 55: Kraken Setup - Final Steps
### Lecture 56: Movie Model - Basics
### Lecture 57: Movie Model - Implementation
### Lecture 58: Getting & Adding Movies
### Lecture 59: Editing & Deleting Movies
### Lecture 60: Search & Filter Movies
## Quiz 8: Chapter 8 ## Quiz

## Section: 10 - Instagram App
### Lecture 61: Project Intro
### Lecture 62: App & Kickstart Setup
### Lecture 63: The Instagram API - Basics
### Lecture 64: The Instagram API - Implementation
### Lecture 65: User Images & Lightbox
## Quiz 9: Chapter 9 ## Quiz

## Section: 11 - Bizlist Using CouchDB
### Lecture 66: Project Intro
### Lecture 67: App & CouchDB Setup
### Lecture 68: Business Routes & Views - Structure
### Lecture 69: Business Routes & Views - Implementation
### Lecture 70: Add & Fetch Businesses - Basics
### Lecture 71: Add & Fetch Businesses - Implementation
### Lecture 72: Edit, Delete & Filter Businesses
### Lecture 73: Edit, Delete & Filter Businesses - Final Steps
## Quiz 10: Chapter 10 ## Quiz

## Section: 12 - Course Summary
### Lecture 74: Course Summary