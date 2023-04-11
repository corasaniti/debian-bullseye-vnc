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
docker run -d -p 5900:5900 -e "VNC_PASSWORD=choose-password" debian-bullseye-vnc
```

#### Alternatively Pull and Run Container from Docker Registry
``` 
docker run -d -p 5900:5900 \
           --name bullseye-vnc \
           --hostname bullseye-vnc \
           -e TZ=Europe/Rome \
           -e "VNC_PASSWORD=choose-password" \
           corpie/debian-bullseye-vnc:latest          
```
