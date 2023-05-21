# To install Node-RED and Mosquitto on a Raspberry Pi
## Install Node-RED
Open a terminal on the Raspberry Pi or connect via SSH.
Run the following command to install Node-RED:
```
bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)
```
Follow the on-screen prompts to complete the installation. It may take a few minutes to complete.

## Install Mosquitto
Open a terminal on the Raspberry Pi or connect via SSH.
Run the following command to install Mosquitto:
```
sudo apt-get update
sudo apt-get install mosquitto
```
Start Mosquitto:
```
sudo systemctl status mosquitto
```
