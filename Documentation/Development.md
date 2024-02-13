# Development Environment Manual
## Docker-based Replication
 - Make sure you have <a href="https://docs.docker.com/get-docker/">Docker</a> installed on your machine
 -  Clone this repository to your local machine using the following command:

    `git clone https://github.com/yabetsg/everewear.git`
- Navigate to the project's root directory:

    `cd everewear`


- create a `.env` file inside the backend folder and paste in the following keys:

    `DATABASE_URL="mysql://root:pass123@mysql:3306/everewear"`

    `SECRET_KEY = "secretkey"`

- Build the containers by running the following command in the projects root directory:

    `docker-compose build`
- Run each container in order by following these commands:

    `docker-compose up -d mysql`

  `docker-compose up -d frontend`
  
    `docker-compose up -d backend`

- Issue: You might face an issue where backend might fail to run, in that case you will need to open the docker app and run the backend container manually

  
- Open up http://localhost:8080/ in your browser to run the project


## Installation

### Node Installation

- Make sure you have the latest version of Node installed. You can download and install it from <a href="https://nodejs.org/en/download">here</a>.

- Version 16.0.0 - 18.16.1 is tested.


### MySQL Installation

- Visit the MySQL official website and download the MySQL community server <a href="https://dev.mysql.com/downloads/mysql/">here</a>.

### MySQL Workbench Installation 
- Install MySQL workbench <a href="https://www.mysql.com/products/workbench/">here</a>. 


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



### Database setup

 - Open up mysql workbench

<img src="./pictures/workbench.png" width="270"></img>

- Press the plus icon to add a connections.

<img src="./pictures/workbench_conn.png" width="270"></img>

 - The test connection should look like this or you can type in your own info in the fields.
 - Click `Store in keychain` to set a password. If you chose to follow the image above set your password to `pass123`.
- After you have set a password press `Test connection`.

 - After connecting create a schema called `everewear`
 - After creating a schema add a `.env` file the backend folder and paste in the following:

    `DATABASE_URL="mysql://username:password@localhost:3306/everewear"`
    
- Replace `username` and  `password` with your own credentials, replace the port number to match your connection.

- If you followed the image above then your url should look like this:

    `DATABASE_URL="mysql://root:pass123@localhost:3306/everewear"`

- Navigate to the backend folder and run the following commands:
   
    `npx prisma generate`
    
    `npx prisma migrate dev`

### Local Hosting

- To run the project, execute the following command inside of the frontend directory:

    `npm run dev`
- Follow the link provided in the terminal or copy and paste it in your browser.

### Frontend File Structure

<img src="./pictures/frontend-structure.png" width="150"></img>
- public
    - Contains files like images and HTML that you want to include directly in your project without them being processed during the build.

- tests
    - Contains unit test for the frontend

- assets
    - Contains static assets like images, icons and css styles that are used in the app.
- components
    - Contains react components used in the app.
- context
    - Contains Components that serve as data providers throughout the app
- pages
    - Contains main components that represent a single page, such as home, login, signup, etc.

### Backend File Structure

<img src="./pictures/backend-structure.png" width="150"></img>
- tests
    - Contains unit test for the backend
    
- controllers 
    -  Holds files which are responsible for handling HTTP requests, connecting to the database and managing the interaction between the server and the database.

- models 
    - Holds each model in the database.

- prisma 
    - Holds a file that define all the models for the database.

- .env
    - Holds local database string with username and password

- routes
    - Holds files of each routes of the application.

- views
    - Holds temporary view templates for testing routes on the server side.

- app.js
    - Main file that runs the application.
    
### Linting:

### Frontend & Backend
Navigate to the backend directory:

`cd everewear`

Run the following command to run linting process:

`npm run lint`
