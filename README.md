# Portfolio-project-4
*Containerizing python application using docker*

**What is Containerization?**
  
  *Containerization is a software deployment process that bundles an application’s code with all the files and libraries it needs to run on any infrastructure.*
  *Containerization enables software developers to build, deploy, and manage applications more efficiently and effectively.*
  
  **Why to containerize an application?** 
  
  *Portability: Containerization enables software developers to deploy applications in multiple environments without rewriting the program code.*
  
  *Scalability: Containers are lightweight software components that run efficiently. Therefore, software developers can easily add multiple containers for different 
                applications on a single machine.*
                
  *Isolation:   Containerization provides isolation between different services/application running within same machine*
    
  **What is docker and what are its components** 
  
  *Docker is an open-source platform that enables developers to build, deploy, run, update and manage containers. 
   Containers are standardized, executable components that combine application source code with the operating system (OS) libraries and dependencies required to run that 
   code in any environment*

  The Docker Engine is the core component of Docker and consists of three parts:

   Server:    It is the Docker daemon called dockerd. It can create and manage Docker images, containers, networks, etc.
   
   REST API:    It is used to instruct the Docker daemon what to do.
   
   Command Line Interface (CLI):    It is a client that is used to enter Docker commands
  
*In this setup, we are going to use 2 docker containers , one for our application and another for nginx*

**How it works?**

* Incoming traffic will first reach the host on port 80 where we run 2 containers.

* The traffic will then be forwarded to nginx container using port mapping 80:80 from host to nginx container.

* We need to expose port 80 outside nginx container (Dockerfile).

* The application will run on application container on port 9090.

* By default, all ports will be open for the containers to communicate between each other.

* From nginx the traffic will be forwarded to application container and our clients will be able to access our application.

**STEPS**

Host an python application (without using docker i.e without containerization)

Step 1: Run a python application

Step 2: Host a python web application using uwsgi and its default development web server (passing all parameters in command line)

Step 3: Host a python web application using uwsgi and its default development web server (using an .ini file to mention the parameters)

Step 4: Host a python web application using uwsgi and nginx as web server which acts as reverse proxy (.sock and .ini file)

How to containerize the same python application using docker

Step 5: StepInstall docker

Step 6: Run application container by creating its image using Dockerfile

Step 7: Run nginx container by creating its image using Dockerfile

  
