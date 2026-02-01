# LinuxServer Docker Mod for FFmpeg

A Docker mod for the linuxserver images that adds ffmpeg

## Usage

Add the following environment variable to your docker-compose.yml or docker run command:

```yaml
environment:
  - DOCKER_MODS=yourusername/docker-ffmpeg-mod:latest
```

Full example:

```yaml
services:
  nginx:
    image: lscr.io/linuxserver/nginx:latest
    environment:
      - DOCKER_MODS=yourusername/docker-ffmpeg-mod:latest
    restart: unless-stopped
```
