### Docker commands

`docker container run -it -p 80:80 nginx --name myEnginex nginx`
it = interactive, -p = publish, 80:80 = your port:server port

`docker container ls` only running containers

`docker container ls -a` all containers 

`docker container rm ID` remove container

`docker container stop NAME`

`docker container rm NAME -f` remove a running container

`exit` exit the container

`docker container exec -it NAME bash` bash into your server

## Bind files in nginx server into a local directory. This allows the user to edit files in the container

`docker container run -d -p 8080:80 -v $(pwd):/usr/share/nginx/html --name nginx-website nginx`

`docker images` list images

`docker image rm ID` remove image

`docker pull nginx` downloads nginx image

## Create a Dockerfile

`FROM nginx:latest`

`WORKDIR /usr/share/nginx/html`

`COPY . .` copy to the image

## Create a docker image && push to dockerhub

`docker image build -t username/any_name .` username in dockerhub/any_name

`docker push username/any_name` push to your dockerhub

`docker login` if you need to authenticate

## Upload your code/files to Github, create a VM, SSH into the VM and clone your repository, then:

`docker compose up` run/install the app in a server 

`docker compose down` stop the app

## Dockers in GCP Compute Engine

Make sure to install GIT and docker/compose

`docker run docker/compose:1.13.0 version` or latest

```
docker run --rm \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v "$PWD:/rootfs/$PWD" \
    -w="/rootfs/$PWD" \
    docker/compose:1.13.0 up
```

