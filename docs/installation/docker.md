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
An alternative step to this is to use the Docker Desktop GUI. Please refer to the [Docker Desktop documentation](https://docs.docker.com/desktop/use-desktop/images/) for further information.
3. **Run the Docker container.** After the image is downloaded, start the container by running this command in your Command Line Interface (Command Prompt on Windows, Terminal on macOS/Linux):
```bash
docker run -d -p 3838:3838 ameliaes/tidal:1.0   
```
This may take a while to run. It will start the app inside Docker and map port **3838** on your computer to the app’s port inside the container. An alternative step to this is to use the Docker Desktop GUI. Please refer to the [Docker Desktop documentation](https://docs.docker.com/desktop/use-desktop/images/) for further information.
4. **Access the TIDAL app.** Open your web browser (Chrome, Firefox, Safari, etc.). Go to [http://localhost:3838](http://localhost:3838) to open the TIDAL R Shiny app.
5. **Close docker** When you are finished stop the docker container running on the port:
```bash
docker ps
docker stop <CONTAINER ID>
```

### Troubleshooting

#### 1. "docker: command not found"
   You may need to add docker to your executable path, eg. on a mac:
   ```bash
   export PATH="$PATH:/Applications/Docker.app/Contents/Resources/bin/"
   ```

#### 2. Port Already in Use:
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

#### 3. Connection Refused:
   If you can’t access the app, check if the container is running with:
   ```bash
   docker ps
   ```
   If it’s not listed, run the `docker run` command again.


