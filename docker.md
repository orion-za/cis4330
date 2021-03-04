<h3>Installing Docker</h3>

At https://www.docker.com/products/docker-desktop you download the appropriate version of Docker for your operating system. On Linux, the easiest way to install Docker is by downloading and running a convenience script using the following commands:
	
	$ curl -fsSL https://get.docker.com -o get-docker.sh
	$ sh get-docker.sh

After the installation is complete you can optionally add your user to the “docker” group with the following command:

```sudo usermod -aG docker <your-user>```
This will allow you to run docker without root privileges.

<h3>Running a Container</h3>

To demonstrate how containers work we will create a simple Nginx server. To do this we run the command

```
$ docker container run –publish 80:80 --detach nginx
```
[Imgur](https://i.imgur.com/RNgPSCG.jpg)

Since we don’t have the nginx image locally yet, Docker will automatically download the latest version from Docker Hub. The ``` --publish``` flag lets us map a port on our host machine to a virtual port in the container; in this case we mapped port 80 on our host to port 80 in the container. The –detach flag runs the container in the background so we can regain control of the command line immediately.

We can see a list of currently running containers with the docker ```container ls command```:

[Imgur](https://i.imgur.com/f0pCfHw.jpg)
	
Here we can see some information about the nginx containter we just run, including its container ID, port mapping and a name that was automatically generated.

We can stop the container using the ```docker container stop``` command:
	
 [Imgur](https://i.imgur.com/b4EueUm.jpg)
 
By running ```docker container ls``` again we can confirm that the container has indeed stopped running.

By running the nginx container again without detaching it we can observe the logs as we visit the page it is hosting at localhost in a browser:

[Imgur](https://i.imgur.com/cQfAJ3c.jpg)

[Imgur](https://i.imgur.com/fE78LPW.jpg)
 															
Let’s run the container in the background one more time so we can run another command to learn a bit more about it.

By running the ```docker container top``` command we can see the proccesses running inside the container:

[Imgur](https://i.imgur.com/GJXmLJg.jpg)

Notice how only two processes are running. This tells us something very important about containers: they are isolated from the host system. None of the processes running on our host system are visible to the container.

If we run a regular ```ps aux``` command on our host system we can observe another important fact about containers:

[Imgur](https://i.imgur.com/2E4lYUE.jpg) 
  
Here we can see that an nginx process is running. In other words, containers are just processes to the host. This is a key difference between VMs and containers. Because containers are processes we can start and stop them and run several at a time without straining the host system too much.
