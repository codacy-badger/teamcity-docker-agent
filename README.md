## TeamCity Agent Image Dockerfile

[![CircleCI](https://circleci.com/gh/codacy/teamcity-docker-agent.svg?style=svg)](https://circleci.com/gh/codacy/teamcity-docker-agent)
[![MicroBadger](https://images.microbadger.com/badges/image/codacy/teamcity-agent.svg)](https://microbadger.com/images/codacy/teamcity-agent "Get your own image badge on microbadger.com")

This project contains the Dockerfile and all necessary scripts to build the Docker image and run a TeamCity Build Agent inside the container.

You can pull the ready-to-use image from the Docker Hub repository
                                     
`docker pull jetbrains/teamcity-agent`

If you need to build your own image, you need to perform the following:

1) Pull our minimal agent image and re-tag it 
```
docker pull jetbrains/teamcity-minimal-agent
docker tag jetbrains/teamcity-minimal-agent teamcity-minimal-agent
```

If you want to start with your own base agent image, see our [instructions](https://github.com/JetBrains/teamcity-docker-minimal-agent) on how to build it.
If you change the operation system, update the following line in the in Dockerfile appropriately:  
```
apt-get install -y docker-engine=1.10.3-0~wily 
```

3) Run the `docker build` command:
```
docker build -t teamcity-agent
```

See our [detailed instructions] (https://hub.docker.com/r/jetbrains/teamcity-agent/) on how to use the image in the Docker Hub repository .
