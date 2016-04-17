# perfect-web-stack
The perfect Web Stack for building Websites, Web Applications, Web API's and combination solutions for just about every project. The "perfect web stack" is a heavily opinionated web stack which in our eye's is perfect.

## Introduction
While the description of the “perfect web stack” above may annoy many developers out there, perhaps claiming that there is no “perfect” stack, I beg to differ. You see choosing a web stack for your next web development project is a very subjective process as most times it is based on your own personal journey as a developer. Having said that, it would be unwise to begin a new project without investigating current trends in web development as this is a landscape which changes often.

With close to 15 years’ application development experience in both the corporate and start-up worlds, I have had the good fortune of being exposed to pretty much every single web technology there is. This exposure varies from full-blown enterprise solutions through to many hundreds of test projects as I have explored this ever-changing but wonderful world of web development.

The “perfect web stack” is, in my humble opinion, the perfect combination of web technologies that currently exists for me and I strongly believe that it could become the best web stack for your next web development project.

## Important Notes
This document is a work in progress and serves to document the information that has been floating around in my head over the years. In an effort to share my findings and create a reference point for our future projects I am building out this repo with a step by step guide of how I approach web application development. This is being done in parallel to an exciting new start-up I am currently developing.

Due to the nature of development, this document will grow along side the development of a real world application so it may be sometime before it is considered complete. If you find there is information missing that you need assistance with, please feel free to email me, Chris, at spacerockapps@gmail.com and I will gladly assist with any questions you may have.

## Cheat Sheets

[See sails Cheat Sheet](#sailscheatsheet)  
[See MongoDB Cheat Sheet](#mongodbcheatsheet)  
[See VS Code Cheat Sheet](#vscodecheatsheet)  
[See Atom Cheat Sheet](#atomcheatsheet)  
[See npm Cheat Sheet](#npmcheatsheet)  
[See ExpressJS Cheat Sheet](#expresscheatsheet)  
[See Node.js Cheat Sheet](#nodejscheatsheet)


## Perfect Web Stack Technologies

There are a number of technologies that make up the perfect web stack. These are listed below in no particular order. First 3 or 4 things that come to mind as to why I have chosen each one is listed but often the reason are very detailed and will be expended on in future updates to this document.

*Note: Development environment platform options are excluded form the perfect web stack as no matter what your preference is between Windows, Mac or Ubuntu the technologies can be used in developing web applications on any platform.*

### Web API
**sails**: Rapid prototyping, intuitive libraries, write less API plumbing code, extensible and customizable.  
Website: http://sailsjs.org/

### Web Server
**Node.js**: Fast, lightweight, stability, JavaScript.  
Website: https://nodejs.org

### Website Server Side
**Express**: Minimalist, Website plumbing, widely used.  
Website: http://expressjs.com/

### Website Client Side
**AngularJS**: Modular, Dependency injection, widely used, large component library  
Website: https://angularjs.org/

### Database
**MongoDB**: Scalability, flexibility, JSON, lightweight  
Website: https://www.mongodb.org/

### Server Operating System
**Ubuntu Server**: Stability, affordability, availability of cloud host providers.  
Website: http://www.ubuntu.com/server

### Cloud Hosting Provider
**Digital Ocean**: Affordability, ease of use, reliability.  
Website: https://www.digitalocean.com/

### Text Editor / IDE
**Visual Studio Code**: Lightweight, GitHub integration, code highlighting, search capabilities  
Website: https://www.visualstudio.com/en-us/products/code-vs.aspx

## Cherry Picking and Getting Setup-to-go

While not all web development projects are created equally, their requirements are often very similar. The goal with the perfect web stack is to have everything we need to carry out most web development projects. Once we have everything we need, we can "Cherry Pick" components and build out our project with a big smile on our face knowing that we are building on a solid and proven foundation. Below are some examples of the type of web projects where you will find the perfect web stack has everything you need to build with confidence.

* Awesome website for a business.
* Slick line of business applications for your company.
* Amazing "Software as a Service" system.
* Pretty much anything web-based.

Most web application require a core setup of features. Once these core features are in place, everything else is just details. Below are some of the core features you will be able to get cooking with, with the perfect web stack.

* Scalable and Flexible application architecture.
* Secure access through forms and token based authentication mechanisms.
* True separation of concerns with API's and "MVC" design patterns.
* Isomorphic applications with JavaScript everywhere.
* Hacker-proof front-ends and API's using best of breed coding standards.
* Validation methods ensuring data integrity on the client and server.

We I talk about "Getting Setup-to-go" what I mean is getting your project to the point of being able to build out all its features based on a baseline set of code implementation. With this baseline you should be able to easily copy and paste components to scaffold new features and modify them accordingly.

## Getting Started with the Perfect Web Stack

 To guide you through the process of getting started with the perfect web stack I will be documenting my process while I build out an application which has the following core set of requirements. Now obviously all projects are different, but this one I am building requires the use of all the components that make up the perfect web stack. Below I have listed some of the requirements I need to meet. Feel free to cherry pick what you need.

 * Build a RESTfull API to be consumed by internal and external services including the website.
 * Build a custom authentication database.
 * Secure the API using web tokens.
 * Build a website with a public facing side optimised for search engine discoverability.
 * Build a web application as a Single Page Application (SPA).
 * Allow users to login to the web app from the website.
 * Ensure all web form data collected is validated on both the client and server.

## Initial Setup

1. Create a GitHub repository.
2. Clone the repository to a local development directory.
3. Generate the sails Web API. [See sails Cheat Sheet](#sailscheatsheet)
4. Create directory for the Web project.
5. Generate a package.json file. [See npm Cheat Sheet](#npmcheatsheet)
6. Generate the Express website. [See Express Cheat Sheet](#expresscheatsheet)
7. Open both projects using VS Code. [See Visual Studio Code Cheat Sheet](#vscodecheatsheet)

## Database setup using MongoDB

1. Create a MongoDB database.
2. Create a users collection.
3. Create a database user with read and write access.

For further details, [see the MongoDB Cheat Sheet](#mongodbcheatsheet)

## Web API Setup using sails

1. Configure the API to use the MongoDB Server.
2. Create a simple model and controller for users.
3. Add attributes to the user model specifying type and if required.
4. In Postman, create CRUD collection for the "users" collection.
5. Test that all CRUD operations are working

For further details, [see the sails Cheat Sheet](#sailscheatsheet)

### User Authentication

1. Install the bcrypt npm package

## <a name="sailscheatsheet"></a>sails Cheat Sheet

### Create a new sails project
```javascript
sails coolprojectname --no-linker --no-frontend
```

### Start the sails application
```javascript
sails lift
```

### Configure the Sails Migrate setting

Whenever you lift a Sails application Sails needs to know how to handle the data migration if there have been any schema changes. Without configuring your preferred option, Sails will prompt you with this question. I find this rather annoying so I prefer to set this once and then change it in code if I want to do anything different. My go to option for migrate is: "alter".
In the config/models.js file, update the "migrate" property. You should be able to just uncomment the line that is already there.

### Configure sails to use MongoDB
1. In the config/connections.js file, update the someMongodbServer properties.
2. In the config/env/development.js file, update the "models" option and set the "connection" property to: "someMongodbServer"

#### Sample Settings
```javascript
someMongodbServer: {
    adapter: 'sails-mongo',
    host: '127.0.0.1',
    port: 27017,
    user: 'coolusername',
    password: 'coolpassword',
    database: 'cooldatabasename'
  },
```

### Generate a REST API controller and model
```javascript
sails generate api coolentityname
```

Please refer to the sails website for detailed information on their framework. http://sailsjs.org

## <a name="expresscheatsheet"></a>Express Cheat Sheet

### Install Express
```javascript
npm install express --save
```

Please refer to the Express website for detailed information on their framework: http://expressjs.com

## <a name="nodejscheatsheet"></a>Node.js Cheat Sheet

Please refer to the Node.js website for detailed information on their runtime: https://nodejs.org

## <a name="npmcheatsheet"></a>npm Cheat Sheet

### Initialize a package.json file
```javascript
npm init
```

Please refer to the npm website for detailed information on their package manager: https://www.npmjs.com/

## <a name="vscodecheatsheet"></a>Visual Studio Code Cheat Sheet

### Download Visual Studio Code
https://code.visualstudio.com/download

Please refer to the Visual Studio Code website for detailed information on their Text Editor: https://www.visualstudio.com/en-us/products/code-vs.aspx

## <a name="atomcheatsheet"></a>Atom Cheat Sheet

### Preview Markdown as HTML
Top open a side by side panel showing the HTML generated for the Markdown file you are editing, use the following keyboard shortcut while you have the Markdown file open.
`ctrl-shift-m`

Please refer to the Atom website for detailed information on their Text Editor: https://atom.io/

## <a name="mongodbcheatsheet"></a>MongoDB Cheat Sheet

### Start the MongoDB server
```javascript
mongod
```

### List all databases
```javascript
show databases
```

### Switch to specific database
```javascript
use cooldatabasename
```

### List all collections
```javascript
show collections
```

## Insert a new document
```javascript
db.coolcollectionname.insert( { coolpropertyname: "I am a cool property" } )
```

## Create a database user
Make sure you are using the correct database else the user will be allocated to a "test" database.
```javascript
db.createUser({user: "coolusername", pwd: "coolpassword", roles: [{role: "readWrite", db: "cooldatabasename"}]})
```

Please refer to the Visual Studio Code website for detailed information on their Text Editor: https://www.mongodb.org/

## Known Exceptions and Gotchas

No matter how many times I have built out web applications whether using new methodologies or tried and tested ones, there is always some unexpected issue. In this section I will attempt to highlight any issues I experience during this build and hopefully address these with workable solutions.

### Sails lift command fails with the "pathTo is not defined" error

This normally happens if you are trying to lift a project you have cloned from Github. You see you need to ensure that all local npm modules have been installed before tring to lift the project. So to get those local packed installed for the project, from the project root run the command below.

```javascript
npm install
```

### Lifting sails works but there is an error logged

Even though we created the new sails API project using the --no-frontend switch, for some reason the auto generated config/routes.js file contains a homepage route. Now, unless you want a homepage for your API, which I strongly recommend you don't have, open this file and comments out the following code.
```javascript
'/': {
    view: 'homepage'
  }
```
This should get rid of the error when you lift the sails again.

### Lifting sails fails with the error: unknown adaptor, "sails-mongo"

This is most likely due to you trying to lift a project from a cloned Git project or if you just simply have not installed the sails-mongo npm package. Most often this package is installed globally so some Git cloned projects wont have the package.

Install this package globally by using the following command.

```javascript
npm install sails-mongo -g
```

Alternatively install the package locally by using the following command.
```javascript
npm install sails-mongo --save
```

### Installing the sails-mongo package fails on Windows

If you review the error logs and see reference to something like: "Can't find Python executable", then you will most likely just need to install Python for Windows. Make sure you setup the correct Environment Path variables. This should be an option in the installer but you can always do it manually.

Also, make sure that you install Python version 2.7.11 and not 3.5.1 as gyp does not support Python version 3.5.1

If you are still having hassles, it could be due to the fact that you don't have the necessary Windows DK's installed. Review the errors and install what is required.

## Utilities and Resources

* REST Client for working with Web API: http://www.getpostman.com/
* Code window with tabs (for Windows): https://sourceforge.net/projects/console/files/

## Disclaimer

I am in no way affiliated with any of the technologies mentioned which make up the perfect web stack. This web stack is perfect for me and could be perfect for you, however always make sure you do your own detailed research before deciding on adopting any technologies that are new to you.  
If you don't agree with anything here, please make your voice heard as the perfect web stack should be a collaborative effort of like-minded individuals. Remember though because you may not agree, does not make you or me right or wrong. We are spoilt for choice in todays web development field. Do what makes you happy and productive and allow others that privilege too.
