# Wanderlust-Project
The three-tier project includes a frontend on React, a backend on Node, and a Mongo Database.

NAME - Yatin Gambhir 

DATE - 19 April 2024

Step 1: It is a three-tier project: a frontend on React, a backend on Node, and a Mongo DB. I have added a Dockerfile to both folders, i.e., FRONTEND and BACKEND.

Step 2: Also, for more advanced concepts, I have added Jenkinsfile for the CI/CD automation.

Step 3: Run the three docker containers in the same network to enable communication between them. So for this, follow the below steps and run the following commands:
        
        #Create a docker network
        docker network create <network-name>

        #Run the mongo db container
        docker run -d --name mongo -p 27017:27107 --network <network-name> mongo:latest

Step 4: I have also added the default file of NGINX to enable reverse proxy, which will redirect to the main application. (OPTIONAL)

**CODE TAKEN FROM krishnaacharyaa/wanderlust**

THANKYOU!!
        
        

