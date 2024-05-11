# Dockerlearning

#     # Docker Commands 
#     #  To show the docker version information
        docker --version

#     #  To login to Docker hub
        docker login
        
#     #  To log out from Docker hub
        docker logout
            
#     #  To Pull image
        docker pull <name of image>
            
#     # To view Image in local docker host
        docker images
            
#     # To create containers 
        docker run --name <name of containter like app1> -p 80:80 -d nginx
            
#     # To view running container
        docker ps
            
#     #  To Remove image from local docker host
        docker rmi <imageid> # use "dokcer images" command to get imageid            
            
#     # To Stop container
        docker stop <name of container>
            
#     # To View all containers ( running or stop)
        docker ps -a
            
#     #  To Start container
        docker start <name of container>
            
#     # To Delete the container
        docker stop <name of container>
        docker rm <name of container>

#     # To create Dockerfile
            # Create a notepad file and paste the command in below format. 
            # After that remove the extension and make sure the name of file should be named as Dockerfile ( Capital D and lowercase f)
            
            FROM nginx:latest
            COPY nginx.conf /etc/nginx/nginx.conf
            EXPOSE 80
#     # To build the image from source code file 
              # Copy and paste the Dockerfile to the location where the source code is kept.
              # Open command prompt and switch to directory where source code files are kept. 
              
              >  docker build -t <your-docker-hub-id>/<image-name>:<tag> .
              # in the above command there is a dot at the last. This dot copies all the files from the location
              
              Replace your docker hub account Id
              
              > docker build -t eglitmyk>/myappimage .

#     # To push the local docker image to Docker Hub 
             # As a best practice, images should be tagged before pushing to the docker hub 
             > docker tag <your-docker-hub-id>/<image-name> <your-docker-hub-id>/<image-name>:<tag>
             
             # To push the local docker image to docker Hub
             > docker push <your-docker-hub-id>/<image-name>:<tag>

#     # To connect to container or get inside the container and execute commands in container 
             > docker exec -it container-name /bin/sh
         
