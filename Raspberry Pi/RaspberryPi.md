# To prepare and set up a Raspberry Pi
1. Download Raspberry Pi OS: https://www.raspberrypi.org/downloads/
2. Flash the Raspberry Pi OS onto an SD card: https://www.balena.io/etcher/) 

Etcher is a tool to flash the downloaded Raspberry Pi OS image onto the SD card.

## Set up Wi-Fi
In the "boot" partition of the flashed SD card, locate the wpa_supplicant.conf file.
Open the file in a text editor and add the following lines:
```
country=<your_country_code>
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1

network={
    ssid="<your_wifi_ssid>"
    psk="<your_wifi_password>"
}
```
Replace <your_country_code> with the ISO 3166-1 alpha-2 country code for your country (e.g., US, GB, DE, etc.).

Replace <your_wifi_ssid> with the name of your Wi-Fi network.

Replace <your_wifi_password> with the password for your Wi-Fi network.

## Set up the Raspberry Pi
1. Insert the prepared SD card into the Raspberry Pi's SD card slot.
2. Connect the Raspberry Pi to a power source using a micro USB cable.
3. Connect a monitor, keyboard, and mouse to the Raspberry Pi (if needed).
4. Wait for the Raspberry Pi to boot up. You should see the Raspberry Pi OS desktop 

## Update Raspberry Pi
Open a terminal on the Raspberry Pi or connect via SSH.
Run the following commands to update the Raspberry Pi OS:
```
sudo apt-get update
sudo apt-get upgrade
```
