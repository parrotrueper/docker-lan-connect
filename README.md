# Connect a docker container to a specific LAN

To configure, first determine what ip address to ping

`nmcli`

Replace the IP address in `docker-compose.yml`

Determine what device on the host to connect to.

for wired

`nmcli device | grep ethernet`

or for wifi

`nmcli device | grep wifi`

Replace the desired device for the `parent` entry in `docker-compose.yml`

Then build and run:

`docker compose -f docker-compose.yml up --build`

