# Pihole Dnscrypt Vpn
Docker Compose file for creating a vpn with dns-over-https resolver in the backend

# About
A docker compose file that turns host into a wireguard vpn server with dns resolution through pihole for blocking adds and stopping trackers. This is then further sercured via dnscrypt which will create a dns-over-https to encrypt traffic being sent to dns providers

# How to start up

* Step 1: Git Clone the repo
* Step 2: edit the .env file to fit your settings, the most important things here are the IP variable and the PUID and GUID variables
* Step 3: `run docker-compose up`

# How to Check if Working

Check everything is running by entering the pihole ip specified in the docker-compose file in your web browser and log in to the website

Next connect a device to the wireguard and see if the pihole page is accessible through the same ip. 
The ip for pihole should be only accesible through the vpn as it's all contained in the virtual docker network specified in the docker-compose file



# Acknowledgements
Credit goes to losuler for the initial docker-compose file and inspiration 
- https://github.com/losuler/pihole-dnscrypt-docker

Pihole for well Pihole! As well as their example to run through host machine 
 - https://github.com/pi-hole/docker-pi-hole/blob/master/docker-compose.yml.example

For helping figure out the routing of dns through wireguard
- https://github.com/IAmStoxe/wirehole/blob/master/docker-compose.yml