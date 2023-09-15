<h1>Setting Up Docker Containers</h1>
<br>A container in the cloud is a lightweight, standalone, and portable environment that packages an application along with its dependencies, allowing it to run consistently across different cloud infrastructure and computing environments. Containers enable efficient deployment, scaling, and management of software applications in the cloud by isolating them from the underlying infrastructure and ensuring consistent execution regardless of where they are deployed.

<br>During this phase of the project, we will be setting up Docker on our Jump Box so we can install containers on it. Docker will enable us to efficiently manage and deploy containers, making our applications more portable and easier to scale. Once Docker is configured on the Jump Box, we will proceed to containerize and deploy our applications, streamlining the deployment process and ensuring consistency across different environments.
<ol>

  
<li>We will begin by making a connection to our Jump Box through SSH  </li>
<br><img src="https://i.imgur.com/lzfNmUC.png" height="70%" width="70%">

<br><li> Next, we will need to install Docker with the commands</li>
```
sudo apt update
sudo apt install docker.io
```
<br><img src="" height="70%" width="70%">

<br><li>Once Docker has completed downloading, verify that Docker service is running using the command
```
sudo systemctl status docker
```

</li>
<br><img src="https://i.imgur.com/YRRNAFL.png" height="70%" width="70%">
<br> Note that if Docker service is not running, it can be started with the following command: 
```
sudo systemctl start docker
```

<br><li>After verifying that Docker service is running, run the following command with sudo to pull the "cyberxsecurity/ansible" container from Docker Hub: 
```
sudo docker pull cyberxsecurity/ansible
```
<br>This command will download the specified container image from Docker Hub to your local system. Once the image is pulled, you can proceed to create and run containers based on it for your Ansible tasks.

</li>
<br><img src="https://i.imgur.com/OZDDfaf.png" height="70%" width="70%">

<br>Ansible is an open-source automation tool that simplifies IT infrastructure management and configuration through code, making it crucial for automating tasks and maintaining consistency in our Dockerized environment.



<br><li> Launch the Ansible container and connect to it using the following Docker command:
```
docker run -ti cyberxsecurity/ansible:latest bash
```
 </li>
<br><img src="https://i.imgur.com/x9on3sf.png" height="70%" width="70%">

<br>This command initiates the Ansible container, allocates a pseudo-TTY for interaction, and starts a bash shell inside the container. This allows you to access the container's command-line interface and execute Ansible commands for our project needs.



<br><li>We will now need to create a new security group rule that will allow our Jump Box full access to our VNet. For now we will need an inbound rule that will allow SSH connections from our Jump Box's private IP address.</li>
<br><img src="  https://i.imgur.com/JvXlaki.png " height="70%" width="70%">

<br><img src="https://i.imgur.com/Byv930Z.png" height="70%" width="70%">




</ol>

<br>
<br>Click here to return to <a href="https://github.com/jimmyhcao/CloudSecurity-InProgress/blob/255bd281943dc73bf4b25b1e440dda6173dbe091/README.md"> README.MD</a>
