---
toc: true
layout: post
description: Running gitlab-runner on docker-desktop.
categories: [markdown]
title: An Example Markdown Post
---
# gitlab-runner on docker-desktop
> Guide from internet
Credit where credit is due [[1]](https://raaviblog.com/how-to-run-gitlab-runner-inside-a-docker-container-and-register-to-gitlab-running-in-docker-desktop-on-windows/)

Open a terminal and run the following commands

(1) 
```
docker volume create gitlab-runner-config 
```
(2)
```
docker run -d --name gitlab-runner --restart always -v /var/run/docker.sock:/var/run/docker.sock -v gitlab-runner-config:/etc/gitlab-runner gitlab/gitlab-runner:latest
```
Read teh container ID, and paste it in the following command
```
docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <REPLACE GITLAB CONTAINER ID HERE>
```
The result should be something like:

172.17.0.2

Now register the runner
```
docker run --rm -it -v gitlab-runner-config:/etc/gitlab-runner gitlab/gitlab-runner register
```
In your gitlab page, go to **Setings>CI/CD>Runners**
There you can check your URL and token

Paste them in the Terminal when asked for it, give your runner a description, and if you use tags, then enter them there.