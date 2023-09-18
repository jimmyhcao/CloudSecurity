<h1> Project: Building a Secure Cloud ☁️ Network with VMs and Containers</h1>
<br>
In an age of cloud dominance, safeguarding your network is paramount. Our GitHub project focuses on creating a robust cloud network using VMs and containers. This project equips IT professionals, developers, and cybersecurity enthusiasts with knowledge and tools to secure cloud operations. This introduction outlines the project's significance, explores cloud networking, VMs, containers, and cybersecurity, and sets the stage for our comprehensive resources and tutorials. Join us to build a safer digital world where innovation and security thrive together.

<br>This project will cover the following tools and services<br>

<li>Microsoft Azure
<li>Docker
<li>Ansible
</li>

<h2>Getting Started</h2>
To get our project kicked off, we will need to create and sign into out Microsoft Azure account. After which we will create a <b>Resource Group</b>
<br>
<h3>Resource Groups</h3>
Azure resource groups organize related resources for a project, making them easily identifiable by name. They encompass all the necessary elements, such as networks, firewalls, and virtual computers.

<br><p align="center"><i>Screen shot of completed Resource Group</i>
<br><img src="https://i.imgur.com/ejBDnoP.png" height="70%" width="70%">

<br>
A step by step guide on building a Resource Group can be found <a href="ResourceGroup.md"> here</a><br>



<br>
<hr>
<h3>Virtual Network</h3>
A virtual network, often called a VLAN or VPN, creates isolated network segments within a physical network for improved management and security. Azure Virtual Network is Microsoft Azure's service for secure, isolated cloud networks, enabling control over IPs, subnets, and security for connecting Azure services like VMs, databases, and web apps.

<br>Creating a virtual network would be the next step in this project

<br><p align="center"><i>Screenshot of completed Virtual Network</i>
<br><img src="https://i.imgur.com/uhwmAng.png" height="70%" width="70%">

<br>
A step by step guide on creating Azure's Virtual Network can be found <a href="VirtualNetwork.md"> here</a><br>
<br>
<hr>
<h3>Network Security Group (NSG)</h3>
An NSG is a fundamental component of Azure's network security. It acts as a basic network-level firewall that allows or denies inbound and outbound traffic to network interfaces, VMs, or subnets within a virtual network. NSGs work at the transport layer (Layer 4) of the OSI model and can be used to define rules that control the flow of network traffic based on source IP, destination IP, port, and protocol. You can use NSGs to filter traffic both inbound and outbound at the network level.


<br><p align="center"><i>Screenshot of Network Security Group</i>
<br><img src="https://i.imgur.com/6x74y2C.png" height="70%" width="70%">

<br>A step by step guide on creating Azure's Network Security Group can be found <a href="https://github.com/jimmyhcao/CloudSecurity-InProgress/blob/8111494103e82d812e491f857fe1b625d573b25f/NetworkSecurityGroup.md"> here </a><br>

<hr>
<h3>Virtual Machines (VMs)</h3>
Now that we have our virtual network and security group created to protect it, we can continue building our cloud infrastructure by adding virtual machines (VMs) to our network. Virtual computing is a fundamental component of today's internet infrastructure, where many servers you encounter daily are virtual. Virtual computers share components with physical ones but are defined by software. When setting up a virtual machine, you'll configure hardware aspects, including:<br>
<br><li>RAM
<li>Storage (SSD/HDD)
<li>Disks
<li>CPU</li>
<br>Within the realm of virtual computing, these elements are simulated through software. When setting up a virtual machine (VM), we specify its "hardware" attributes, which encompass details such as RAM, storage capacity, and CPU. Following this configuration, we install an operating system, enabling the VM to function as a standard computer.<br>
<br>In this phase, our goal is to establish three virtual machines (VMs), with one serving as a jump box, also referred to as a bastion host. This jump box will act as the gateway for accessing our cloud network and any other VMs residing within it. We will be configuring our Jump Box VM to access our two additional VMs through SSH authentication.

<br><p align="center"><i>Basic diagram of our objective during this step</i>
<br><img src="https://i.imgur.com/5KhC9SS.png" height="70%" width="70%">


<br>Enabling password authentication for SSH on a server is considered insecure due to the vulnerability of passwords being susceptible to brute-force attacks. From this point forward, our cloud server access will exclusively rely on cryptographic SSH keys; password authentication will not be allowed.
</li>

<h4>SSH Authentication Explained:</h4>
SSH authentication works by generating a key pair, with the private key stored on your computer, while the public key is stored on the server you want to access. When attempting to gain access, the SSH protocol will check if the key pair is a match. Once verified, the user will be authenticated and granted access.
<p align="center"><img src="https://i.imgur.com/OvzQROD.png" height="70%" width="70%">

<br><a href=""> Download</a>




<hr>
<h3>Docker Container</h3> 
Docker is an open-source platform that allows developers to package applications and their dependencies into containers. These containers are lightweight, portable, and isolated, ensuring that applications run consistently across different environments. Docker simplifies development, testing, and deployment by providing a consistent and reproducible environment for applications, making it easier to manage and scale software across various platforms.

<br>In this project phase, we will embark on configuring your jump box to execute Docker containers and undertake the installation of a specific container.

<br><p align="center"><i></i>
<br><img src="https://i.imgur.com/OZDDfaf.png" height="90%" width="90%">


<br>As we strive for a comprehensive and consistent automated configuration approach, we will leverage Docker to deploy Ansible, a provisioning tool. This strategy guarantees the uniform execution of our provisioning scripts across all environments. Consequently, our automated configurations will maintain precise consistency with each execution, minimizing any potential variations in configurations.

<br>At this point in our project, we will be completing a couple of steps:
<ul>
<li>Download Docker container with Ansible onto our Jump Box VM
  <li>Create a Playbook with instructions to download Docker, Python, and DVWA (Damn Vulnerable Web Application)
    <li>Distribute our playbook to our Web-1 and Web-2 VMs using Ansible</li>
</ul>

<br><p align="center"><i></i>
<br><img src="https://i.imgur.com/uX3lc9d.png" height="70%" width="70%">







<br><p align="center"><i></i>
<br><img src="" height="70%" width="70%">
<br><a href=""> Download</a>

