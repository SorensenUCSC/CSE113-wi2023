---
title: "Docker Setup"
layout: single
classes: wide
---

In order for your homeworks to be graded, they must run on the docker, which will have the same environment as our teaching servers. We will use the docker image from CSE113 (Winter 2022) for this class. This is an introduction to setting up docker. Please let us know if you have other references that you think could be useful!

**The docker has a very simple Ubuntu OS. If you use a linux/MacOS/WSL environment then it will likely work. However, please double check that code works on the docker imagine just to be sure. If it does not run, then it can't be graded.**

**Please make sure you understand the storage model of Docker as not all storage is persistant! It is always a good idea to back up your work in progress, e.g., using git. But please don't make your homework git repos public!**

_This write up has been contributed to by several students: Reese Levine, Yanwen Xu, and Neal Chokshi; please let me know if you have any other suggestions!_

------

## Install Docker

Follow instructions [here](https://docs.docker.com/get-docker/). The destop version is recommended. The following instructions outline how to use docker primarily through the CLI, but the desktop app provides the same functionality and may be easier to use.

## Download the Container

After Insalling Docker, run the following command: 

```
docker pull reeselevine/cse113:latest
```

When running, the container includes everything necessary for the homework to work correctly, namely `python3`, C++ compilers, and `make`. It also includes two text editors, `vim` and `emacs`. If you’d like another text editor included in the image, please let us know.

## Development

Homework skeletons will be available to download using `wget`. Download the homework and `unzip` it. You can either work on your code outside the container, using a text editor or IDE of your preference, or you can work on your code inside the container using a terminal based text editor like vim or emacs.

There is good support using VSCode with docker given it's [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension. This allows you to hook into the docker environment within VSCode, letting you access files and the terminal just as you would on your host system.

When you’re ready to start the container **make sure you’re in the top level homework directory** (for example, for homework 1 your current directory should be “homework1_packet”, or wherever you extracted the code to). `pwd` should return something ending with `/homeworkX_packet`. When you mount this directory within docker the permissions will change, so make sure you aren't in a directory that you don't want to lose access to. Once you are ready, run the following command depends on your system:

### On Linux/macOS
```
docker run -v "$(pwd)":/assignments -it reeselevine/cse113:latest bash
```

### On Windows 

with Powershell (should work on both [Powershell 7](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.2) and Windows Powershell):

```
docker run -v ${pwd}:/assignments -it reeselevine/cse113:latest bash
```

with cmd (Command Prompt): 

```
docker run -v %cd%:/assignments -it reeselevine/cse113:latest bash
```

You should be running inside the container at this point. Running `ls` should list your files. At any point, to exit the container just type `exit`. Once you exit the container you can re-run the existing container either via the Docker Desktop UI by clicking the "run" icon within the list of available containers, or by the following commands in a terminal/powershell/cmd instance:

First list the available containers to get the assigned name from the NAMES column. 
```
docker ps -a
```

Start the container. Add -i if you want an interactive shell. Once the container is started you can start using it if you passed -i, or connect to the container in VSCode.
```
docker start <name> -i
```


At this point, you can edit your code and run it by following the instructions on the homework. Any changes you make to your files inside the container will persist when the container exits.

We recommend keeping your homework files under source control using git or another tool, since this will help with keeping track of your changes and making sure you don’t lose your work.



## More Details About Docker

While the details of running docker containers are unnecessary for this course, it might be helpful to understand what each part of the above commands are doing.

* `docker pull` downloads the specified container, which in this case is `reeselevine/cse113:latest`, where `reeselevine/cse113` is the image name and latest is the tag. Docker allows multiple tags for the same image, but for this course we will most likely only be using the default latest tag for images.

* `docker run` is a combined command to both create+start a container.

* `docker start` lets you start a container that has already been created

* `-v` mounts a volume from the host (your computer) to the docker container. We are mounting the current host machine directory to the directory `/assignments` inside the container.

* `-it` gives us an interactive, terminal based session. Without this, the container would immediately exit.


## Useful Docker commands

* `docker container prune` Each `docker run` creates a new container, it will stop when you exit. **Do not create a new container each time you want to work on your project**. Using docker run for the initial setup and then exiting and calling start whenever you want to resume development is the recommended workflow. Having a bunch of Docker containers can take a lot of space, fast. Some time it is useful to prune all stopped containers by running `docker container prune` to gain some space. 
