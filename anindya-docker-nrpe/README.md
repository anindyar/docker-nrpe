# docker-nrpe [![](https://badge.imagelayers.io/totem/docker-nrpe:latest.svg)](https://imagelayers.io/?images=totem/docker-nrpe:latest 'Get your own badge on imagelayers.io')
NRPE Docker Container

## About
Provides NRPE Server within docker container. This allows remote monitoring of docker hosts from nagios/Icinga. In additiona to the totem/nrpe container. This container has some modification that adapts the check_load warning (-w) and critical (-c) threasholds automatically based on the number of cores the server has. 

## Status
Ready for production

## Images
The docker-nrpe image is available on docker hub [anindyaroy/nrpe:version1.0](https://hub.docker.com/r/anindyaroy/nrpe/). It is setup using hub's automated build process.

## Running
In order to run the NRPE container , use command :

```
/usr/bin/docker run --privileged -v /:/mnt/ROOT --name nrpe --rm -p 5666:5666 anindyaroy/nrpe:version1.0

```

Once up, you can monitor server using nagios/icinga. 

Note: In order to monitor multiple disks, simply mount them under /mnt directory.
