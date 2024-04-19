This is the frontend part of the application.

NAME: Yatin Gambhir
DATE: April 19, 2024

Step 1: Create a network as mentioned in the outside README file to enable communication between the containers.

Step 2: In that network, run the docker container from the Dockerfile present in the repository.

      #Build the docker image
      docker build -t wanderlust-frontend .

      #Run the container
      docker run -itd --name wanderlust-frontend-project -p 5173:5173 --network <network-name> wanderlust-frontend
      
Step 3: In the .env file change the VITE_API_PATH to http://public-ip-of-server:5000.

Step 4: You can also run this from the Jenkinsfile. All the above commands are written in the Jenkinsfile for automation. (OPTIONAL)

THANKYOU!!
