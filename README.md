# VNC-Browser 
A Lightweight, Ready-to-Use Web Browsing Environment in Docker with VNC Access

**Leave a star ⭐ if you like this project 🙂 thank you.**

[![Docker Pulls](https://img.shields.io/docker/pulls/mrcolorrain/vnc-browser?style=flat-square&link=https://hub.docker.com/r/mrcolorrain/vnc-browser)](https://hub.docker.com/r/mrcolorrain/vnc-browser)
[![Docker Stars](https://img.shields.io/docker/stars/mrcolorrain/vnc-browser?style=flat-square&link=https://hub.docker.com/r/mrcolorrain/vnc-browser)](https://hub.docker.com/r/mrcolorrain/vnc-browser)
[![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/MRColorR/vnc-browser/docker-ci.yml?style=flat&link=https%3A%2F%2Fgithub.com%2FMRColorR%2Fvnc-browser%2Factions)](https://github.com/MRColorR/vnc-browser/actions)


## Info :information_source:
VNC-Browser is a minimal, customizable, Linux-based Docker image designed to provide a lightweight environment for browsing the web via VNC.
This Docker image encapsulates a lightweight, VNC-accessible web browsing environment built on top of Debian and Alpine Linux. It packages a VNC server, noVNC for browser-based VNC access, and the Chromium and Firefox web browsers, providing a compact solution for remotely browsing the web. Whether you're looking to browse securely or need a browsing environment within a containerized setup, VNC-Browser has you covered.

**Key Features ✨**

- **VNC-Ready**: Ready for use with any VNC client or through a web browser using noVNC, offering a user-friendly interface.
- **Lightweight**: Built on Alpine Linux and Debian Slim, ensuring minimal resource usage.
- **Customizable**: Set VNC password, initial website URL, auto-start settings, etc. via environment variables to build custom environments (e.g. webkiosk)
- **Accessible**: Access the VNC server directly or through a browser using noVNC.

## Available images 📦

- `mrcolorrain/vnc-browser:alpine` (with Firefox browser)
- `mrcolorrain/vnc-browser:debian` (with Chromium browser)

## Quick Start 🚀
You can run it easily using its default or by passing the appropriate environment variables.

- ### Docker CLI 🐳
  ```bash
  docker run -d -p 5900:5900 -p 6080:6080 --name vnc-browser -e VNC_PASSWORD="mypassword" mrcolorrain/vnc-browser:debian
  ```

- ### Docker Compose 🐳
  ```yaml
  version: "3.9"
  services:
    vnc-browser:
      container_name: vnc-browser
      image: mrcolorrain/vnc-browser:debian
      ports:
        - "5900:5900"
        - "6080:6080"
      environment:
        VNC_PASSWORD: "mypassword"
      restart: unless-stopped
    ```
All you have to do is
```bash
cd scripts/
```
or
```bash
cd ./scripts
```
Then do 
```yaml
docker compose up
```
