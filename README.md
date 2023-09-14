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
A step by step guide on building a Resource Group can be found <a href="https://github.com/jimmyhcao/CloudSecurity-InProgress/blob/63ad031e16fa2e1f13dfa5537d5cf7fdd05295d6/ResourceGroup.md"> here</a><br>


<br>
<hr>
<h3>Virtual Network</h3>
A virtual network, often called a VLAN or VPN, creates isolated network segments within a physical network for improved management and security. Azure Virtual Network is Microsoft Azure's service for secure, isolated cloud networks, enabling control over IPs, subnets, and security for connecting Azure services like VMs, databases, and web apps.

<br>Creating a virtual network would be the next step in this project

<br><p align="center"><i>Screenshot of completed Virtual Network</i>
<br><img src="https://i.imgur.com/uhwmAng.png" height="70%" width="70%">

<br>
A step by step guide on creating Azure's Virtual Network can be found <a href="https://github.com/jimmyhcao/CloudSecurity-InProgress/blob/eecea6118be682c37ee223303b1e40f650c40717/VirtualNetwork.md"> here</a><br>
<br>
<hr>
<h3>Network Security Group (NSG)</h3>
An NSG is a fundamental component of Azure's network security. It acts as a basic network-level firewall that allows or denies inbound and outbound traffic to network interfaces, VMs, or subnets within a virtual network. NSGs work at the transport layer (Layer 4) of the OSI model and can be used to define rules that control the flow of network traffic based on source IP, destination IP, port, and protocol. You can use NSGs to filter traffic both inbound and outbound at the network level.


<br><p align="center"><i>Screenshot of Network Security Group</i>
<br><img src="https://i.imgur.com/6x74y2C.png" height="70%" width="70%">

<br>A step by step guide on creating Azure's Network Security Group can be found <a href="https://github.com/jimmyhcao/CloudSecurity-InProgress/blob/8111494103e82d812e491f857fe1b625d573b25f/NetworkSecurityGroup.md"> here </a><br>

<hr>
<h3>Virtual Machines (VMs)</h3>
Now that we have out virtual network and security group created to protect it, we can continue creating our cloud infrastructure by creating and adding some virtual machines to our network. Virtual computing is prevalent in today's internet infrastructure, where many servers you encounter daily are virtual. Virtual computers share components with physical ones but are defined by software. When setting up a virtual machine, you'll configure hardware aspects, including:<br>
<br><li>RAM
<li>Storage (SSD/HDD)
<li>Disks
<li>CPU</li>
<br>Our objective during this step is to create 3 VMs with one being a jump box used to access our cloud network and any other VMs located inside of it. 


<br><p align="center"><i></i>
<br><img src="" height="70%" width="70%">
<br><a href=""> Download</a>
