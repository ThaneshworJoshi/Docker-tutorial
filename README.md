# Docker Turorial

## Table of Contents

- [Introduction](#introduction-section)
- [Common Termonology and explanation:
](#terminology-section)
- [Installation](#installation-section)
- [Commands](#commands-section)
- [Conclusion](#conclusion)



# Introduction

## Learn Docker By Real World Example:


<img src="./img/game1.jpg" alt="Alt Text" width="200"/>
<img src="./img/game2.jpg" alt="Alt Text" width="200"/>
<img src="./img/game3.jpg" alt="Alt Text" width="200"/>

Imagine you're an avid video game enthusiast with a passion for three distinct games: Game A, Game B, and Game C. Each game has unique system requirements and configurations that need to be managed delicately.

Ordinarily, handling the specific demands of each game can be cumbersome. Switching between games might entail repetitive installations or removals of various components. Fortunately, Docker presents an elegant solution to streamline this process.

Docker allows you to create individualized "containers" for each game. Each container functions as a self-contained unit housing all the prerequisites necessary for the respective game to operate seamlessly. Thus, you'll have a dedicated "Game A Container" equipped with suitable graphics software, a designated "Game B Container" encompassing essential libraries, and an exclusive "Game C Container" preconfigured to precise specifications.

When you're ready to immerse yourself in a gaming session, you can effortlessly select the relevant container for the desired game and initiate it on your machine, all without any interference between them.

Moreover, the versatility of Docker extends to collaborative gaming experiences. You have the capability to share these containers with your friends. If they wish to partake in Game A, you can provide them with the corresponding "Game A Container," enabling them to enjoy the game on their own system without grappling with intricate setup procedures.

Docker's prowess lies in its ability to maintain game segregation, guaranteeing smooth execution for each game while preempting any adverse interactions. It's akin to possessing a set of bespoke gaming lockers, facilitating swift transitions between your favorite titles at your leisure.

In the realm of software development, Docker serves as a comparable tool. Developers employ Docker to encapsulate their applications within containers, mirroring the concept of your gaming containers. This approach simplifies the deployment of applications across diverse computers or servers, eradicating concerns about compatibility hurdles. Essentially, Docker furnishes a transportable, self-contained environment for each distinct application.

<br/>
<br/>
<br/>

##   Common Termonology and explanation:

## 1. Docker:
   Docker is a platform that allows developers to create, deploy, and run application using containers.
    Containers are like lightweight, isolated virtual machines that can package an application along with its dependencies and run time environment.

## 2. Container:
  A Container is a lightweight and standalone executable pacakge that includes everything needed to run an application, including OS, code , runtime, libraries, and system tools. Containers are isolated from the host system and from other containers, ensuring consistency and portability.

## 3. Image:
An Image is a blueprint or template used to create containers. It is a read-only file that contains the application's code, libraries, and dependencies. You can think of an image as a snapshot of a container before it's running'

## 4. Dockerfile:
  A Dockerfile is a simple text file that contains instructions for building a Docker image. It defines the base image, adds application code, sets up environment variables, and configures the containers.


## 5. Registry:
A Registry is a centeralized repository where Docker images are stored and can be shared. Docker Hub is a popular public registry, but you can also set up private registries for your organization's internal use.

## 6. Pull:
To pull an image means to download it from a registry to your local machine. You can thing of it like downloading an app from an app store

## 7. Push:
Pushing an image means uploading it to a registry. It's like publishing your own app on an app store so others can download and us it.

## 8. Run:
To run a container means to start it using a Docker image. Once you run  a container, it becomes a live instance of that image.

## 9. Volume:
A volume is a special feature in Docker that allows data to be shared between the host system and a container or between multiple containers. It helps to persist data beyond the container's lifecycle.

## 10. Compose: 
Docker Compose is a tool used to define and manage multi-container applications. It allows you to use a YAML file to define the services, networks, and volumes needed for an application.

## 11. Service:
In the context of Docker Compose or Docker Swarm (Docker's native orchestration tool), a service is a definition of how a container should behave, including which image to use, the number of replicas, networking settings, etc.

## 12. Swarm: 
In the context of Docker Compose or Docker Swarm (Docker's native orchestration tool), a service is a definition of how a container should behave, including which image to use, the number of replicas, networking settings, etc.

<br/>
<br/>
<br/>
<br/>

##   Installation Steps:

## Step 1. Install Docker:
   First, you need to install Docker on your computer. Visit the official Docker website (https://www.docker.com/) and download the version suitable for your operating system (Windows, macOS, or Linux). Follow the installation instructions for your OS.

## Step 2. Check if docker  is installed:
  To check if Docker is installed on your system, you can run a simple command in the terminal or command prompt.
  Here's how to do it for different operating systems:
  ### For Linux and macOS:
    Open a terminal and type the following command:
      docker --version

    For Windows:
      docker info

<br/>
<br/>
<br/>
<br/>
<br/>
# Command Lists (questions)


## 1: How to  See the list of Docker images available on your system?
<hr/>
    
    docker images 

    This command will display a list of all the Docker images that have been pulled or built on your machine. 

The output will show you a table with columns 
<br/>
<br/>
<img src="./img/dockerimg.png" alt="Alt Text" width="600"/>

<br/>
<br/>

1.  "REPOSITORY" column represents the name of the image,
2.  "TAG" column shows the tag associated with the image (usually representing different versions)
3.   "IMAGE ID" is a unique identifier for each image
4.   "CREATED" indicates when the image was created and 
5.   "SIZE" shows the disk space used by the image.

<br/>
If you have a lot of images, you might need to scroll up to see the entire list. If you want to see only specific images, you can use docker images <repository> to filter the output based on the repository name.

<br/>
<br/>

## 2: How to see list of running docker containers? 
<hr/>
    To see a list of running Docker containers (not images), you can use the 

    docker ps

This command will display a list of all the running containers on your system. 

By default, 

    docker ps 

will show you only the running containers. The output will display a table with columns

TODO : Image 

<br/>
<br/>

This table provides information about each running container, such as the container ID, the image it is based on, the command used to start the container, the container's creation date, its current status, exposed ports, and the container name.
<br/>
<br/>
If you want to see all containers, including the ones that are stopped, you can add the -a or --all option to the docker ps command:
      
      docker ps -a


This will show you a list of all containers, both running and stopped.


## (Note): Remember that "Docker images" represent the base images from which containers are created, while "Docker containers" are the running (or stopped) instances of those images.


<br/>
<br/>

## 2: How to pull Docker images from a Docker registry (like Docker Hub) to your local machine?
<hr/>
  
      you can use the docker pull command.


 This command will download the specified image or its specific version (tag) if available. Here's how to do it:

<br/>
<br/>

      docker pull IMAGE_NAME[:TAG]


Replace IMAGE_NAME with the name of the image you want to pull, and TAG with a specific version or tag of the image (optional). If you omit the TAG, it will default to the "latest" version of the image.

<br/>
For example, to pull the official "nginx" web server image with the "latest" tag, you can use:

    docker pull nginx:latest


If you want to pull a specific version of the image, replace "latest" with the desired tag. For instance:

    docker pull nginx:1.19

<br/>

Once the download is complete, you can use
         
    docker images 
         
to see the list of downloaded images on your local machine.

<br/>
<br/>

## 3: How to run a Docker container in detached mode?
<hr/>

you can use the -d option with the docker run command.
This will start the container in the background and you'll get back control of your terminal or command prompt without being attached to the container's console output. Here's how you can do it:

 Open a terminal or command prompt and use the following command to run the container in detached mode:

    docker run -d IMAGE_NAME[:TAG]


Replace IMAGE_NAME with the name of the image you want to run, and TAG with a specific version or tag of the image (optional).
<br/>
<br/>
For example, to run an Nginx web server container in detached mode:

      docker run -d nginx:latest

If the image is not already available on your system, Docker will first pull the image from the Docker Hub (or the specified registry) and then start the container in detached mode.
<br/>
<br/>

Once the container is running, you will see a long container ID printed in the terminal, indicating that the container is running in the background. You can use this container ID to manage the container, such as stopping or removing it.

<br/>
<br/>

To list the running containers, you can use the docker ps command:
    
    docker ps

<br/>
<br/>

To stop a detached container, you can use the docker stop command followed by the container ID or name:

    docker stop CONTAINER_ID


## (note)
Keep in mind that running containers in detached mode is useful for background tasks or long-running services. If you want to interact with the container's console, you can run the container without the -d option, but it will be attached to your terminal, and you won't get your shell prompt back until you stop the container or use the appropriate keyboard shortcut to detach from the container (usually Ctrl + P, Ctrl + Q).


<br>
<hr/>

# Work in Progress

More content will be added here soon. Stay tuned!