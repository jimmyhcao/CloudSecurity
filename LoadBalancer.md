<h1>Setting up a Load Balancer</h1>

<ol>

  
<li> Create a load balancer and assign a static IP address  </li>
<ul>
<li>Search for <code>Load Balancer</code> in search bar on main portal page
<li>Click + Create and use same resource group as other sources

</li>

</ul>

<br><p align="center"><img src="https://i.imgur.com/oBuBTBv.png" height="70%" width="70%">

<li>Add a Health Probe to Regularly Check the VMs</li>
<ul><li>Ensure that virtual machines (VMs) receive traffic by setting up a health probe.</li></ul>
<br><p align="center"><img src="https://i.imgur.com/rZ8yYEN.png" height="70%" width="70%">

<li> Create a Backend Pool with Both VMs Added </li>
<ul><li>Configure a backend pool that includes both VMs.</li></ul>
<br><p align="center"><img src="https://i.imgur.com/FhsT4Uo.png" height="70%" width="70%">
<br><p align="center"><img src="https://i.imgur.com/g7h01f5.png" height="70%" width="70%">


<li>Create a Load Balancing Rule for Port 80 </li>
<ul><li>Forward incoming traffic on port 80 from the load balancer to the Virtual Network.</li></ul>

<br><p align="center"><img src="https://i.imgur.com/aH6Ctg5.png" height="70%" width="70%">
<br><p align="center"><img src="https://i.imgur.com/0mtrYsZ.png" height="70%" width="70%">

<li>Create a New Security Group Rule to Allow Port 80 Traffic</li>


<ul><li>Configure a security group rule to permit port 80 traffic from the internet to your internal Virtual Network.</li></ul>
<br><p align="center"><img src="https://i.imgur.com/zbEK6he.png" height="70%" width="70%">

<li> Remove the Security Group Rule Blocking All Traffic</li>

<ul><li>Delete any security group rule that blocks all traffic on the Virtual Network, allowing traffic from the load balancer to pass through.</li></ul><br>


<li> Verify Accessibility of DVWA App from a Browser </li>
<ul><li>Confirm that the DVWA (Damn Vulnerable Web Application) can be reached from a web browser.</li></ul>
<br><p align="center"><img src="https://i.imgur.com/n28nnVE.png" height="70%" width="70%">


</ol>

<br>
<br>Click here to return to <a href="README.md"> README.MD</a>
