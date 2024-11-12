---
title: Docker
layout: default
parent: Getting Started
nav_order: 4
---

## Docker

TIDAL can be used by installing the [TIDAL Docker image](https://hub.docker.com/r/ameliaes/tidal/) and launching the R Shiny application locally (rather than using and uploading data to the tool online).

### Installation

1. **Install Docker.** Before you can run the app, you need to have [Docker Desktop](https://www.docker.com/get-started/) installed on your computer (macOS, Windows or Linux). Docker allows you to run the app in an isolated container without needing any extra setup.
2. **Pull the Docker image.** Once Docker is installed and running, open your Command Line Interface (Command Prompt on Windows, Terminal on macOS/Linux), and run the following command to download the TIDAL R Shiny app image:
```bash
docker pull ameliaes/tidal:1.0
```
3. **Run the Docker container.** After the image is downloaded, start the container by running this command in your CLI:
```bash
docker run -d -p 3838:3838 ameliaes/tidal:1.0   
```
This will start the app inside Docker and map port **3838** on your computer to the app’s port inside the container.
4. **Access the TIDAL app.** Open your web browser (Chrome, Firefox, Safari, etc.). Go to [http://localhost:3838](http://localhost:3838) to open the TIDAL R Shiny app.

### Troubleshooting

#### 1. Port Already in Use:
   If you get an error about port 3838 being in use, try this instead:
   ```bash
   docker run -d -p 8080:3838 tidal-modelling/tidal-app:latest
   ```
   Then access the app at [http://localhost:8080](http://localhost:8080).

   Alternatively, check if a docker container is already running on port 3838 and stop it:
   ```bash
   docker ps
   docker stop <CONTAINER ID>
   ```

#### 2. Connection Refused:
   If you can’t access the app, check if the container is running with:
   ```bash
   docker ps
   ```
   If it’s not listed, run the `docker run` command again.

#### 3. Docker Command Not Found:
   If Docker isn't installed, follow the installation steps again for your operating system.

