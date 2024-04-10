# Dockerlearning

#     # Docker Commands from Widnows Docker Host
        #  To login to Docker hub
            > docker login
            
        #  To Pull image
            > docker pull <name of image>
            
        #  To view Image in local docker host
            > docker images
            
        #  To create containers 
            > docker run --name <name of containter like app1> -p 80:80 -d nginx
            
        #  To view running container
            > docker ps
            
        #  To Remove image from local docker host
            > docker rmi <imageid> # use "dokcer images" command to get imageid            
            
        #  To Stop container
            > docker stop <name of container>
            
        #  To View all containers ( running or stop)
            >docker ps -a
            
        #   To Start container
            > docker star <name of container>
            
        #  To Delete the container
            > docker stop <name of container>
            > docker rm <name of container>

        #  To create Dockerfile
            # Create a notepad file and paste the command in below format. 
            # After that remove the extension and make sure the name of file should be named as Dockerfile ( Capital D and lowercase f)
            
            FROM nginx:latest
            COPY nginx.conf /etc/nginx/nginx.conf
            EXPOSE 80
        #  To build the image from source code file 
              >  Open command prompt
              >  
