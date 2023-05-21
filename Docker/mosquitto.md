# To install Mosquitto MQTT on Docker
## 1.Pull the Mosquitto Docker Image
```
docker pull eclipse-mosquitto
```
## 2.Create a Docker Container
```
docker run -d --name mosquitto -p 1883:1883 -p 9001:9001 eclipse-mosquitto
```
## 3.Verify the Installation
```
docker ps
```

# To set up user authentication
## 1.Access the Mosquitto Docker container's shell
```
docker exec -it mosquitto sh
```
## 2.Create a Password File
```
mosquitto_passwd -c /mosquitto/config/passwd <username>
```
## 3.Configure Mosquitto to Use the Password File
```
vi /mosquitto/config/mosquitto.conf
```
  Add the following lines to the configuration file:
```
allow_anonymous false
password_file /mosquitto/config/passwd
```
## 4.Restart the Mosquitto Service
```
  pkill -f mosquitto
```
