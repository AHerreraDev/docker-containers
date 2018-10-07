### Docker commands

`docker container run -it -p 80:80 nginx --name myEnginex nginx`
it = interactive, -p = publish, 80:80 = your port:server port

`docker container ls` only running containers
`docker container ls -a` all containers 
`docker container rm ID` remove container

`docker images` list images
`docker image rm ID` remove image

`docker pull nginx` downloads nginx image