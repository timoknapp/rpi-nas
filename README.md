# Raspberry PI NAS
Setup your own NAS on a Raspberry Pi

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

## Components
- Heimdall Dashboard
- Plex
- Portainer
- CloudCmd
