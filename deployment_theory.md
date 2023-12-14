<!-- ################################################  Cove Page ################################################### -->

<b><h1 align="center">Concepts to get started with deployment</h1></b>

<p align="center"><b>First of all we will cover basics of the deployment and the basic techniques that we should know before starting deployment along with the brief history</b></p>

<!-- ######################################## Deployment Basics & Introdution ###################################### -->

<h2 align="center">Deployment Basics & Introdution</h2>
<details>


<summary style="text-align:center;">Click to Expand</summary>

---

<i> “Application or software deployment is the process of installing, configuring, updating, and enabling one application or suite of applications that make a software system available for use. </i>”

<b> Things we should know before starting deployments.</b></br>
Before starting deployment we should have knowledge of linux OS , dockers & docker compose.. There are also some other technologies used in deployment but to take a start we have to learn linux OS and dockers first.



<p align="center"><b>Lets start linux, docker and docker-compose and understand the concepts one by one.</b></p>

</details>


---
<!-- ##################################################### Linux #################################################### -->

<h2 align="center">Linux OS (Ubuntu)</h2>
<details>
<summary style="text-align:center;">Click to Expand</summary>

---

<h2>  What is Linux and why do we prefer Linux? </h2> </br>
Linux is an open source command line operating system. It is convenient to use and has the following benefits.
<uol> <h3> <li> High throughput: </li> </h3> 
 Throughput means multiple tasks executed per unit time. It means we have running multiple applications and the operating system needs to respond fast. Linux responds fast in a specific amount of time.
<h3> <li> Free and open source: </li> </h3>
Linux is free and open source. You can see the source code used to create linux (kernel).
<h3> <li> Stability and reliability: </li> </h3> 
Linux is a UNIX based OS and UNIX was originally designed to provide an environment that is powerful, stable and reliable yet easy to use. Linux systems are widely known for stability and reliability. Many linux servers on the internet have been running for years without failure or even being started.
<h3> <li> Security: </li> </h3>
Linux is the most secure OS. As  it is UNIX based and UNIX provides the most powerful and secure platforms.
<h3> <li> Flexibility: </li> </h3>
Linux is very flexible. We can create our own operating system by using the linux kernel.
<h3> <li> Cost and maintenance: </li> </h3>
Linux cost and maintenance is lower than the other operating systems in terms of licensing fee, software/hardware purchase and maintenance cost and system support service and administrative cost. </uol>



Here are some very common commands that are very necessary and  we have to remember before starting deployments.

| Command | Description |
| ------- | ----------- |
| `cd/` | Move to root directory|
| `ls` | To see the content of directory|
| `ls -a` | Show all the content of directory including hidden content.|
| `cd {name directory/folder}` | To get in to the specific directory by name. |
| `clear` | Clear the commands from the terminal page |
| `cd..` | To one step back (means to back) |
| `mkdir {folder/directory name}` | To make a new folder /directory. |
| `touch {file name}` | To make a new file |
| <b> Edit file using vi editor </b> </br> <ol> <li> `vi {file name}` </li> </br> <li> `i` </li> </br> <li> `esc` </li> </br> `shift + :` </li> </br> <li> `wq` </li> </ol> | <ol> <li> Use vi with file name to open editor </li> </br> <li> Press “i” to insert and edit the file. </li> </br> <li> Press “esc” button to come out of the editor </li> </br> Press shift+: to end the process of modification. </li> </br> <li> Press ‘w’ means write and then ‘q’ means quit. </br> In this way file will be edited. </li> </ol> |
| <b> Edit file using nano editor </b> </br> <ol> <li> `nano {file name}` </li> </br> <li> `ctrl+x` </li> </br> <li> `'y'` or `'n'` </li> <ol> | <ol> <li> Press nano and file name, the editor will be opened and you can edit the file. <li> </br> <li> To save file press "ctrl+x". </li> </br> <li> Press ‘y’ for yes and ‘n’ for no.</br> In this way file will be edited and saved. </li> |
| `cat {file name}` | To read the content in the file. |
| `cp {file name}/path/` | To copy files by providing a path. |
| `mv {file name}/path/` | To move files from one place to another. |
| `rm {file name}` | To remove or delete files. |
| `man {command}` | To check the properties and details of command. |
| `find /file path/ -name {file name}` | To find a file from a specific path. |
| `hostname -I` | To check the system IP address. |
| `cat /poc/cpuinfo` | To check system information. |
| `sudo apt update` | To update the apt package. |
| `sudo su` | To login as a super user as admin. |
| `apt-get install {package name}` | To install a specific package. |
| `exit` | To signout from the super user. |
| `who` | Shows who is currently logged in. |
| `whoami` | Show system name |
| `chmod 777 {file name}` | File read, write, execute permissions to everyone |
| `chmod 755 {file name}` | Full permission to owner, read permissions for others |
| `chmod 766 {file name} ` | Full permission to owner, read and write for others |
| `chown [user] {file name} ` | Change file ownership |
| `chown {user}:{group} {file name} ` | Change file owner and group
| `top` | Show all running processes |
| `kill [process_id]` | Kill the process by ID |
| `pkill [process_name]` | Kill the process by name | 
| `killall [process_name]` | Kill all processes by name |

Here are some shortcus that we will mostly use in linux while deployment.


| Shortcut | Description |
| ------- | ----------- |
| `Command+{pres tab two times}` | To check the possibilities of command write the command and press tab two times. |
| `ctrl+a` | To go at the start of command |
| `Ctrl+e` | To go at the last of the command |



<p align="center"><b>The most common used commands are discussed aboved for more details about linux please visit <a href= "(https://phoenixnap.com/kb/linux-commands-cheat-sheet)" target= "blank"> Linux in detail </a> </b></p>

</details>


---
<!-- ############################################ Docker & Docker-Compose ########################################### -->

<h2 align="center">Docker and docker-compose</h2>
<details>
<summary style="text-align:center;">Click to Expand</summary>

---

 <b> <h3> Brief History of techniques before docker technology: </h3> </b>
<p> In the bad old days there was a lack of skills and technologies and usually one app was deployed on one server. The main reasons were the resources requirements and different infrastructure and dependencies. There were certain disadvantages of this technique; it was costly because one application was deployed on one server and we needed more resources and a team to manage the services. </br> In 1998  VMware was established to provide us with different applications for virtualization. There were certain benefits with virtualization that we were able to deploy multiple apps on a single server by different OS instances. This technique was much better than the old one and saved a lot of resources. But there were still some issues with this technique that the OS consumes a lot of resources. Each OS instance was using the required resources individually and there was a need for more resources. Also there was licensing cost for different OS instances. There was still a need to establish a technique that will be better than these techniques and provide us with a unique environment. </br> At last the container architecture developed. In which we can manage different applications by using containers by creating a docker engine layer on a single operating system. This technology is very low cost and we can easily manage applications as containerized applications are portable, fast and lightweight. Also we need less hardware resources. We can run the application with all its dependencies. There is no licensing cost for it and we can push our application on a public repository and we can access it over the internet all over the world. </br>
<i> <b> “Docker is a software that manages containers and provides us services for orchestration. Different developers have worked on it to make improvements. It is available for both linux and windows operating systems with two editions, one is the enterprise edition that is paid and different companies purchase this edition with different support contracts for organization use. Second edition is free for community users.” </i> </b> </br> 
To take a start with deployment using docker we need to learn all the basic commands that we will use in deployment while using dockers. Here are the commands that we will use. Just take a look and learn these commands.


| Command | Description |
| ------- | ----------- |
| `sudo apt-get update` | To update the apt package index |
| `sudo apt-get install docker-ce docker- ce-cli containered.io` | To Install latest version of Docker CE and containered. |
| <uol> <li>`docker --version`</li> </br> <li> `docker info` </br> <li> `docker version` </li> </uol> |  Use these commands to check docker information|
| <uol> <li> `docker image ls ` </li> </br> <li>`docker images`</li> </uol> | Show docker images |
| `docker image rm {image name}:{image tag}` | To Delete images from docker. |
| <uol> <li> `docker container ls` </li> </br> <li>`docker ps`</li> | To check running containers. |
| <uol> <li> `docker container ls -a` </li> </br> <li>`docker ps` -a</li> | To check all the containers stopped or running. |
| `docker exec -it {image name or image id} sh` | To get in the container that is already in running state without stopping it. |
| `docker stop {container id or container name}` | To stop a container |
| `docker start {container id or container name}` | To start the container again. | 
| `docker rm {container name or container id}` | To remove or delete containers. |
| `docker container run -d {image name}` | To run containers in detached mode. |
| `docker run -d -p {external port}:{default port} {image or container name}:{tag}` | To publish an application by running the container on a specific port. |
|`docker run -d --name {container name} -p {external port}:{default port} [container name}:{tag}` | To run a container with a specific name. |
|`docker logs {container name or ID}` | To check docker logs to identify bugs. |
| `docker create [image]` | Create a container without starting it. |
| `docker create -it [image]` | Create an interactive container with pseudo-TTY. |
| `docker rename [container] [new-name]` | Rename a container. |
| `docker rm -f [container]` | Force remove a container, even if it is running. |
| `docker events [container]` | View real time events for a container. |
| `docker update [container]` | Update the configuration of a container. |
| `docker stats [container]` | Show live resource usage statistics for a container |
| `docker network ls` | View available networks. |
| `docker login` | Log in to a Docker registry. |
| `docker logout` | Log out of a Docker registry |
| `docker system prune` | Remove unused images, containers, and networks. |
| `docker run -it [image]` | Run an interactive process, e.g., a shell, in a container. |
| `docker exec -it [container] [shell]` | Run a shell inside a running container |
| `docker build [dockerfile-path]` | Create an image from a Dockerfile. |
| `docker build .` | Build an image using the files from the current path. |
| `docker history [image]` | Show history for an image. |
| `docker image prune` | Remove unused images. |


</br>
<p align="center"><b>To get more details about docker kindly visit  <a href= "https://phoenixnap.com/kb/docker-commands-cheat-sheet" target= "blank"> Docker in detail </a> </b></p>


</br>
</br>
<h2 align="center">Docker Compose</h2>

<p> <i> Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration. </i> </br>
Compose works in all environments: production, staging, development, testing, as well as CI workflows. It also has commands for managing the whole lifecycle of your application: </br>
<uol> <li> Start, stop, and rebuild services
<li> View the status of running services </br> </li>
<li> Stream the log output of running services </br> </li>
<li> Run a one-off command on a service </li> </uol> 


</br>
Basic commands of docker compose are as below.  

| Command | Description |
| ------- | ----------- |
| `docker-compose up` | To run docker compose files. |
| `docker-compose up -d` | To run docker compose file in detached mode |
| `docker-compose down` | To stop the services for docker compose file |
| `docker-compose  -v` | To check docker compose information. |


</br>
<p align="center"><b>To get more details about docker kindly visit  <a href= "https://docs.docker.com/compose/" target= "blank"> Docker-Compose in detail </a> </b></p>