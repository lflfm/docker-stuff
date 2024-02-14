# Docker stuff

[reference](https://www.youtube.com/watch?v=zfNqp85g5JM)

docker run --name firefox2 -p 5800:5800 -p 5900:5900 -e VNC_PASSWORD=foobar jlesage/firefox:v1.17.0  
then connect via any vnc client.

in linux, we can also forward the display:  
xhost +local:docker  
docker run -it --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix repo/some-gui-dockerized-app

docker init

[Test containers package](https://testcontainers.com/)

scan the current directory for vulnerabilities - Comes with Docker Desktop, but I had to download from https://github.com/docker/scout-cli/releases  
docker scout quickview fs://.  
docker scout compate fs://. --to dreamofcode/bitbooks-api:latest  
docker scout compate dreamofcode/bitbooks-api:1.0 --to dreamofcode/bitbooks-api:1.1  
docker scout recommendations dreamofcode/bitbooks-api:latest  
