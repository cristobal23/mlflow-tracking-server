# **MLFlow Tracking Server**

This repository uses docker to build **MLFlow Tracking Server** in a very simplified manner. For this purpose, one need to have Docker Engine installed.

Prerequisites: Docker Engine.

## **Run the Server**
First, check the `docker-compose.yaml` to find the env variables that are needed to be set up. You'd need to create `.env` file and add all the following environment variables with appropriate values.

``` bash 
POSTGRES_HOST : ${POSTGRES_HOST}
POSTGRES_PASSWORD: ${POSTGRES_PASSWORD}
POSTGRES_USER: ${POSTGRES_USER}
POSTGRES_DB: ${POSTGRES_DB}
ARTIFACT_ROOT: ${ARTIFACT_ROOT}
```

Once these variables are set, follow these commands to run the tracking server:

```
source .env
docker-compose up
```

Note, to find the local host IP , you can use `ipconfig getifaddr en0` for MacOS and `hostname -I | awk '{print $1}'` for ubuntu, and put that as the environment variable in the `.env` file.



## More Info on Docker Image with Postgres
    <https://github.com/MahdyShirdel/postgres/>