# deploy-on-localhost-with-docker-01

Dockerfile > Docker Images > Docker Container > Access the App

Step 1 :
Create a new Directory 
<br>

Commands : (In linux)
mkdir myapp 
cd myapp 
(going to the directory - myapp)
<br>

Step 2 : 
Create a file named "index.html"

<br>
Commands : (In linux)
echo "Hello World" > index.html
<br>

Step 3 : 
Create a file named Dockerfile
<br>
Commands :
touch Dockerfile 
<br>

Step 4 : 
Open the "Dockerfile" file in vs code editor or text editor you prefer and addd the following lines 

<br>
Commands : 
FROM nginx 
COPY index.html /usr/share/nginx/index.html
<br>

Step 5 : 
Start docker and Build docker image from docker file 

<br>
Commands : 
docker build -t myapp . 
(this command bnuilds a new docker image with the tag "myapp" using the Dockerfile in the current directory)
<br>


<br>
Step 6 : 
Run docker container from the image 
docker run -p 80:80 myapp 
(this tells the docker to run myapp container and map port 8080 on your local machine to port 80 inside the container)
<br>


Step 7 : 
Access the app 
Open a web browser and navigate to http://localhost:8080 to see the context inside the index.html displayed in your web browser. 
<br>

