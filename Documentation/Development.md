# Development Environment Manual
## Docker-based Replication
 -  Clone this repository to your local machine using the following command:

    `git clone https://github.com/yabetsg/everewear.git`
- Navigate to the project's root directory:

    `cd everewear`
- Build the containers by running the following command in the projects root directory:
    
    `docker-compose build`
- Run each container in order by following these commands:

    `docker-compose up -d mysql`

    `docker-compose up -d backend`

    `docker-compose up -d frontend`
- Open up http://localhost:8080/ in your browser


## Installation

### Node Installation

- Make sure you have the latest version of Node installed. You can download and install it from <a href="https://nodejs.org/en/download">here</a>.

- Version 16.0.0 - 18.16.1 is tested.


### MySQL Installation

- Visit the MySQL official website and download the MySQL community server <a href="https://dev.mysql.com/downloads/mysql/">here</a>.



### Clone Repository

-  Clone this repository to your local machine using the following command:

    `git clone https://github.com/yabetsg/everewear.git`
- Navigate to the project's root directory:
    
    `cd everewear`
- Navigate to the backend directory:
    
    `cd backend`
-  Run the following command to install the required dependencies in the backend:

     `npm install`
- Navigate to the frontend directory:
    
    `cd ../frontend`
-  Run the following command to install the required dependencies in the frontend:

     `npm install`

### Local Hosting

- To run the project, execute the following command inside of the frontend directory:

    `npm run dev`
- Follow the link provided in the terminal or copy and paste it in your browser.

### Frontend File Structure

<img src="./pictures/frontend-structure.png" width="150"></img>
- public
    - Holds files like images and HTML that you want to include directly in your project without them being processed during the build.
- assets
    - Holds static assets like images, icons and css styles that are used in the app.
- components
    - Holds react components used in the app.
- pages
    - Holds main components that represent a single page, such as home, login, signup, etc.

### Backend File Structure

<img src="./pictures/backend-structure.png" width="150"></img>

- controllers 
    -  Holds files which are responsible for handling HTTP requests, connecting to the database and managing the interaction between the server and the database.

- models 
    - Holds each model in the database.

- prisma 
    - Holds a file that define all the models for the database.

- prisma/.env
    - Holds local database string with username and password

- routes
    - Holds files of each routes of the application.

- views
    - Holds temporary view templates for testing routes on the server side.

- app.js
    - Main file that runs the application.

### Database setup

 - Open up mysql workbench 
 - Choose whatever connection instance you want and connect to it
 - After connecting create a schema called `everewear`
 - After creating a schema add a `.env` file inside of the prisma folder and paste in the following:

    `DATABASE_URL="mysql://username:password@localhost:3306/everewear"`
    
- Replace `username` and  `password` with your own credentials, replace the port number to match your connection.

- Navigate to the backend folder and run the following commands:
   
    `npx prisma generate`
    
    `npx prisma migrate dev`

