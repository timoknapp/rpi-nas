# Raspberry PI NAS
Setup your own NAS on a Raspberry Pi

![dashboard](dashboard.jpg)

## Prerequisite
- Docker
- OpenMediaVault (if wanted) [here](https://www.openmediavault.org/)

## Getting Started
```
git pull https://github.com/tea-mo903/rpi-nas.git
cd rpi-nas
```
Replace Placeholders in docker-compose file:
- ${PATH_TO_DISK} with related Path on your PI
- ${USER_ID} with uid of ``id `whoami` ``
- ${GROUP_ID} with gid of ``id `whoami` ``
```
docker-compose up
```
Opening a browser with the IP of your PI should show the Heimdall dashboard. A configured dashboard would like like one above.

## Components
Following show all the applications of the `docker-compose.yml` related to their exposed ports on the host.

| Application | Port | URL |
| ------------| ---- | --- |
| [Heimdall Dashboard](https://github.com/linuxserver/Heimdall) | 80, 443 | http://localhost, https://localhost |
| [Plex](https://github.com/linuxserver/docker-plex) | 32400 | http://localhost:32400/web/index.html |
| [Portainer](https://github.com/portainer/portainer) | 9000 | http://localhost:9000 |
| [CloudCmd](https://github.com/coderaiser/cloudcmd) | 8008 | http://localhost:8008 |
| [pyLoad](https://github.com/linuxserver/docker-pyload) | 8088 | http://localhost:8088 |

## Contributing
Feel free to modify, add, fork: [simply](CONTRIBUTING.md)
