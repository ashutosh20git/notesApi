I am a second year student . Recently I have been taking interest in learning about DevOps . 
Purpose of this project: 
    1. To practice node.js and express.js .
    2. To practice implementation of docker , docker compose .
    3. To implement CI workflow using Github actions for the first time.

Outcomes:
- I got more practical experience with node and express.
- I got more practical exprerience in using docker .
- I learned basics of CI/CD workflow.

I have also started learning TECHNICAL WRITING and hence want to write a document for this as well.

########################################-----------TECHNICAL DOCUMENT---------################################################


PROJECT :  CRUD SERVICE FOR NOTES MANAGEMENT



Techstack used:
    •	Node.js
    •	Express
    •	PostgreSQL(psql)
    •	Git, Github Actions


Platform :
    •	Docker
    •	VS Code IDE
    •	Github

    
Project Overview:
    A containerized CRUD notes management organized into:
      •	Routes
      •	Controllers
      •	Middleware
      •	Database config
    Also contains : 
      •	Dockerfile
      •	Docker-compose.yaml
      •	SQL initial Script
      •	Src folder including the following:      
        1.	Config
        2.	Controllers
        3.	Middleware
        4.	Routes

        
Objectives: 
 Managing notes through REST APIs solves its storage and management problem. 
    App:
      1.	Exposes health endpoint.
      2.	Note endpoints under /api/notes.
    Server:
      1.	Loads environment variables.
      2.	Initialize psql connection.
      3.	Starts Express app.




Core Functionality includes:
  1.	Create a note
  2.	Fetch all notes
  3.	Fetch one note by id
  4.	Update a note
  5.	Delete a note
The above functionalities are implementing in controller layer and mapped in the router layer.
`title` and `content` in controller are present for create and update operations. It returns `404` when note is absent. It also uses PostgreSQL(psql) queries.



Database: PostgreSQL 
    Column Name	   Data Type	   Constraints / Default	  Purpose
    Id  	   SERIAL	   PRIMARY KEY 	   Unique ID for each not     
    title	   VARCHAR(255)	   NOT NULL	   Stores the note title
    content	   TEXT	   NOT NULL	   Stores the notec ontent
    created_at	   TIMESTAMP	   DEFAULT CURRENT_TIMESTAMP	   Stores creation time
    updated_at	   TIMESTAMP_		



Layers Used:
  •  server.js: bootstraps env loading, DB connection, and app startup
  •  app.js: configures middleware, routes, health check, and global error handling
  •  routes/: maps HTTP methods and paths
  •  controllers/: contains business logic and SQL execution
  •  config/db.js: creates PostgreSQL connection pool
  •  middleware/: handles unknown routes and server errors



Architecture Section:
  ClientExpress routeControllerPostgreSQLResponse



Conclusion:
  This project demonstrates the fundamentals of backend development using Node.js, Express.js, PostgreSQL, and Docker. It provides a simple and practical Notes API that supports CRUD operations while following a modular structure and containerized setup. Overall, it serves as a strong beginner-friendly project for understanding API development, database integration, and deployment, with clear scope for future improvements such as authentication, testing, and CI/CD.



##################################################---------------------END-------------------######################################################
