---
layout: page
title: DockerContainers
permalink: /entwickler/DockerContainers
tags: Entwickler
lang: en, de
---

# **DOCKER**CONTAINERS

The server is based on several docker containers that are started with a docker-compose file. This will start the containers in a virtual LAN and map only the ports to be accessec from outside that are configured in the `docker-compose.yml`

For small tasks like making the LDAP accessible from outside all that needs do be done is making the necessary setting in the `docker-compose.yml`.

If you want to know how the containers work inside check out the folders where you fill find the build-process in the `Dockerfile` and the `entrypoint.sh`.

The `mount` folder will keep all the Samba-data. Feel free to mount your storage solution in your network to this folder.

More Detailled Information will be added here after we have published the stable version.
