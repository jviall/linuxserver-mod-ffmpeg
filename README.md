# Docker FFmpeg Mod for Lidarr

A Docker mod for the linuxserver/lidarr image that adds ffmpeg support for post-import scripts.

## Usage

Add the following environment variable to your docker-compose.yml or docker run command:

```yaml
environment:
  - DOCKER_MODS=yourusername/docker-ffmpeg-mod:latest
```

Full example:

```yaml
services:
  lidarr:
    image: lscr.io/linuxserver/lidarr:latest
    container_name: lidarr
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=Etc/UTC
      - DOCKER_MODS=yourusername/docker-ffmpeg-mod:latest
    volumes:
      - /path/to/config:/config
      - /path/to/music:/music
      - /path/to/downloads:/downloads
    ports:
      - 8686:8686
    restart: unless-stopped
```

## What it does

This mod installs ffmpeg in the Lidarr container, allowing you to use ffmpeg in post-import scripts for audio processing tasks.
