This repository was created for self learning purpose.

## #  Docker

### What is it?
 - It is a tool which is used to automate the deployment of applications in lightweight containers so that applications can work efficiently in different environments.

### What is a Docker File?
- It is a text document that contains all the commands a user could call on the command line to assemble an image.
- We create a Docker File, build it, create the image and run in docker container.
 
### Remarks
- A docker file create a Docker image using the build command.
- A docker image contains all the project's code.
- Using Docker image, any user can run the code in order to create Docker containers.
- Once a Docker image is build, it's uploaded in a registry or a Docker Hub.
- From the Docker Hub, user can get the Docker Image and buil new containers.


### Most common used instructions
#### From:
- This command allows you to create a base image such as an operating system, a programming language, etc. All the instructions executed after this command take place on this base image.

#### Run:
- Used to run specified commands. You can use several RUN instructions to run different commands.

#### CMD:
- Specifies the instruction that is to be executed when a Docker container starts.

#### Entrypoint:
- Used to set executables that will always run when the container is initiated. Unlike CMD command, ENTRYPOINT commands cannot be ignored or overrridden.

#### WORKDIR:
- To specify your working directory inside the container.

#### Copy:
- To copy files or folder from your local machine to the docker container.

#### Add:
- Similar to COPY instruction, you can use ADD instruction to copy files or folders from your local machine to docker container. However, ADD also allows you to copy files from a URL as well as a tar file.

#### Expose:
- It informs that the container is listening to the specified port in the network. The default protocal is TCP.

### Example:

```yaml
FROM alpine
COPY sample-files /myFiles
CMD ["sleep","2m"]
```


In the example above, we are pulling alpine image, copy our folder called "sample-files" and paste in a new folder called myFiles, after that, when the container is up, it will run the command sleep for two minutes.


### How to create and run an image:

In the directory of the project, run

1 - 
```yaml
docker build -t sample-img -f .
```
where,

-t = image name:tag
-f DockerFileName, by default if you are using a docker file named DockerFile, you don't need to specify only '.'

2 - 
```
docker images
``` 
to see the images created

3 - 
```
docker run <imgid>
```
where <imgid> is the image id


### Docker compose
- It is a tool to help define and share multi-container applications. It's an important tool for any application that needs multiple microservices, as it allows each service to easily be in a separately managed container.

### How to use Docker compose?
- We can use a YAML file to configure your application's service.
- The configuration for a docker compose file is done in  `docker-compose.yml`
- You don't need to place this at the root of your project like DockerFile. In fact, it can go anywhere, as it doesn't depend on any other code. However, if you're building the images locally, it will need to go in a project folder with the code being built.

