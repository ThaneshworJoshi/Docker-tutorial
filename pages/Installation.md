# DOCKER Turotial

## Learn Docker By Real World Example:


<img src="../img/game1.jpg" alt="Alt Text" width="200"/>
<img src="../img/game2.jpg" alt="Alt Text" width="200"/>
<img src="../img/game3.jpg" alt="Alt Text" width="200"/>

Imagine you're an avid video game enthusiast with a passion for three distinct games: Game A, Game B, and Game C. Each game has unique system requirements and configurations that need to be managed delicately.

Ordinarily, handling the specific demands of each game can be cumbersome. Switching between games might entail repetitive installations or removals of various components. Fortunately, Docker presents an elegant solution to streamline this process.

Docker allows you to create individualized "containers" for each game. Each container functions as a self-contained unit housing all the prerequisites necessary for the respective game to operate seamlessly. Thus, you'll have a dedicated "Game A Container" equipped with suitable graphics software, a designated "Game B Container" encompassing essential libraries, and an exclusive "Game C Container" preconfigured to precise specifications.

When you're ready to immerse yourself in a gaming session, you can effortlessly select the relevant container for the desired game and initiate it on your machine, all without any interference between them.

Moreover, the versatility of Docker extends to collaborative gaming experiences. You have the capability to share these containers with your friends. If they wish to partake in Game A, you can provide them with the corresponding "Game A Container," enabling them to enjoy the game on their own system without grappling with intricate setup procedures.

Docker's prowess lies in its ability to maintain game segregation, guaranteeing smooth execution for each game while preempting any adverse interactions. It's akin to possessing a set of bespoke gaming lockers, facilitating swift transitions between your favorite titles at your leisure.

In the realm of software development, Docker serves as a comparable tool. Developers employ Docker to encapsulate their applications within containers, mirroring the concept of your gaming containers. This approach simplifies the deployment of applications across diverse computers or servers, eradicating concerns about compatibility hurdles. Essentially, Docker furnishes a transportable, self-contained environment for each distinct application.


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

