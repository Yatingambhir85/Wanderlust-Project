This is the backend part of the application.

NAME: Yatin Gambhir
DATE: April 19, 2024

Step 1: Create a network as mentioned in the outside README file to enable communication between the containers.

Step 2: In that network run the docker container from the Dockerfile present in the repository.

      #Build the docker image
      docker build -t wanderlust-backend .

      #Run the container
      docker run -itd --name wanderlust-backend-project -p 5000:5000 --network <network-name> wanderlust-backend

Step 3: Now our backend container is running, we have to copy the data/sample_posts.json file to mongo db container.

    #Copy the sample_posts.json to mongo container
    docker cp ./data/sample_posts.json mongo:/data/sample_posts.json

    #Import the sample_post.json file to the mongodb
    docker exec -it mongo bash
    mongoimport --db wanderlust --collection posts --file /data/sample_posts.json --jsonArray

Step 4: In the .env file change the MONGO_DB_URI to http://mongo:27017/wanderlust

Step 5: You can also run this from the Jenkinsfile. All the above commands are written in the Jenkinsfile for automation. (OPTIONAL)

THANKYOU!!
