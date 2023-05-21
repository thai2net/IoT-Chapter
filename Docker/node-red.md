# To install Node-RED on Docker
## 1. Pull the Node-RED Docker Image
```
docker pull nodered/node-red
```
## 2. Create a Docker Container
```
docker run -d -p 1880:1880 --name mynodered nodered/node-red
```
## 3. Verify the Installation
```
docker ps
```
