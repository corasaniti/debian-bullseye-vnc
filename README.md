## A Debian Bullseye Docker Image with x-server
A Debian Bullseye Docker Image with x-server, Openbox, VNC server, SSH server and other package installed
```
pwgen, curl, iputils-ping, lsb-release, screenfetch, neofetch, exa, nano 
```

#### Build Image From Dockerfile and Run from locally build
```
git clone https://github.com/corasaniti/debian-bullseye-vnc.git
cd debian-bullseye-vnc
docker build -t debian-bullseye-vnc .
docker run -d -p 5900:5900 -p 22:22 -it -e SSHPW=choose-password -e RESOLUTION=1024x768 debian-bullseye-vnc

```

#### Alternatively Pull and Run Container from Docker Registry
``` 
docker run -d -it -p 22:22 -p 5900:5900 \
	--name bullseye-vnc \
	--hostname bullseye-vnc \
	-e SSHPW=choose-password \
	-e RESOLUTION=1024x768 \
	corpie/debian-bullseye-vnc:latest
           
           
```
