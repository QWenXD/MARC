# M. A. R. C.
# Marker Allocation Reconciliation Configurator 
A web-based tool that allows marker coordinator organize markers 

## Technology used
**Backend**

Node.js || Express Server || Squelize ORM || SQLite || Mocha testing || POSTMAN (API testing)

**Frontend**

Node.js || React || Nodemailer || HTML || CSS

## Architecture

The repository contains two Node.js projects. Each is in its own directory:
+ Backend_NodeJS 
+ Frontend_React 

One Node.js instance hosts the back-end server, its API & Sqlite-database.

The other Node.js instance hosts the GUI front-end. 

Both Node.JS instances listen on localhost only. For public access, they are intended to be placed behind a reverse caching proxy (such as Apache). 

There is a live example hosted at https://marcdev.duckdns.org on a Debian linux virtual machine. It will only be live until august 2021. 

 *(It is hosted in south Auckland by SiteHost who have donated the hosting.)*


# Backend Installation Instructions:

## Clone the repository
From a command line, perform the following:

`git clone https://github.com/uoa-compsci-399/MARC.git`

`cd MARC/Backend_NodeJS` 


`npm install` *This will install dependencies.  (express, sqlite, etc)*


## Start the back-end server

`npm start` *(will load the Node.js development server. It will listen on localhost)*.


![image](https://user-images.githubusercontent.com/69673783/113281683-65cd2580-9342-11eb-8ccf-88ad27b1777f.png)

# Frontend Installation Instructions
In a different terminal, switch to the `Frontend_React` directory. For example:

`cd MARC/Frontend_React`

## Install React's dependencies

`npm install`

This may take some time. Once it is complete, launch the React application with:

`npm start`


# Dependencies
Npm knows which dependencies to install because the *package.json* file already has the dependencies registered. 


# Testing
There's a github workflow script which executes integration tests using our Mocha framework. There are no significant tests written (due to time limits)
However, we tested all the api endpoints with POSTMAN

# Future plans
Authentication needs to be merged into the mainline branch.

Marc should be cable of detecting a wide variety of business-logic scenarios, which leads to better & more useful visual filters and automatic emails.

Auto-allocation tools can be implemented either globally or partially.

Previous-semester's Marc databases could be used to pre-compute 'students who had previously marked this course' & other information.

# Acknowledgements
Building Backend based on 
* https://bezkoder.com/node-js-express-sequelize-mysql/

Building Frontend based on 
* https://bezkoder.com/react-crud-web-api/





