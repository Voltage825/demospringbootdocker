# Demo Spring Boot Docker 
A Demo to show off Spring boot in a docker image
______
## Technologies used:

<b>Spring boot</b> - The spring framework's attempt to make a easy to use template with opinionated technologies. - [Spring Boot.](https://projects.spring.io/spring-boot/)
<br>

![Docker Logo][logo_docker]<br>

<b>Docker</b> - A containerisation platform for all operating systems. - [Docker](https://www.docker.com/)


--------
## How to:

Start off with a normal spring boot project [Starter](http://start.spring.io/).
I chose maven with spring boot web starter. 
Then used Spotify's [Docker-maven-plugin](https://github.com/spotify/docker-maven-plugin) and added all my Information into the POM as per the guide.

 ```Bash
 mvn clean package docker:build # to build the image
 
 docker images                          # to see that its in your docker images
 docker run  -p 8080:8080 [image_name]  # to see it run use -d to make it run in the background
 docker ps                              # to see running containers (use -a to see the stopped ones too)
 docker stop [container_name]           # to stop your container
 docker rm [container_name]             # to remove that container
 docker rmi [image_name]                # to remove the image
 
 #Extras:
 docker attach [container_name]         # connects your terminal to the std_out of the container
 docker exec -it [container_name] sh    # gives you bash access to your container
 ```
 More info at [Docker commands Page](https://docs.docker.com/engine/reference/commandline/)
--------
[logo_docker]: https://upload.wikimedia.org/wikipedia/commons/7/79/Docker_%28container_engine%29_logo.png "Docker wooololololo"
Docker logo By dotCloud, Inc. [<a href="http://www.apache.org/licenses/LICENSE-2.0">Apache License 2.0</a>], <a href="https://commons.wikimedia.org/wiki/File%3ADocker_(container_engine)_logo.png">via Wikimedia Commons</a>