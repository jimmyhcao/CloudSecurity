<h1>Creating Virtual Machines (VMs) </h1>
<ol>

  
<li>Create a Virtual Machine (JumpBox)
  
 <ul><li>From homescreen, create a resource and search for "virtual machine". Then navigate to the Virtual machine icon.</ul> 
</li>
<br><p align="center"><img src="https://i.imgur.com/S1PKpj7.png" height="70%" width="70%">

<br>
<ul>
<li>Ensure the subscription and resource group match your virtual network and security group.
<li>Name your VM, e.g., "JumpBox," for easy identification.
<li>Choose an OS image based on your project needs.
<li>Configure the VM with 1 CPU and 1 GB of RAM.
</ul>
 </li>
<br><p align="center"><img src="https://i.imgur.com/rtIbfJ9.png" height="70%" width="70%">

<br><li>Generate an SSH Key Pair
<ul><li>Open a Git Bash terminal and run <code>ssh-keygen</code> to generate a key pair.
  <li>Display the public key with <code>cat ~/.ssh/id_rsa.pub</code>.
    <li>Highlight and copy the SSH public key for later use.
      <li>Note: <code>id_rsa</code> is the private key (do not share), and <code>id_rsa.pub</code> is the public key. </ul>

<br><p align="center"><img src="https://i.imgur.com/blgd5YN.png" height="70%" width="70%">
<br><p align="center"><img src="https://i.imgur.com/dknvmdq.png" height="90%" width="90%">


<br><li>Attach Public Key to the JumpBox VM   </li>
<ul>
<li>In VM settings, under the Administrator account, create a username (e.g., HomeLab).
  <li>Paste the previously copied public key into the designated field.
</li>
</ul>
<br><p align="center"><img src="https://i.imgur.com/ShwgSJu.png" height="70%" width="70%">


<br><li>Configure Networking Settings</li>
<ul>
  <li>Move to the Networking tab and set the appropriate settings for Virtual network, network security group, etc.</li>
</ul>
<br><p align="center"><img src="https://i.imgur.com/ms78hZu.png" height="70%" width="70%">

<br><li> Review and create </li>
<ul><li>Review your VM configuration settings to ensure they match your requirements.</li></ul>
<br><p align="center"><img src="https://i.imgur.com/b8cDCzc.png" height="70%" width="70%">

<br><li> We will now see our Jump Box virtual machine on our main page   </li>

<br><p align="center"><img src="https://i.imgur.com/7L4n511.png" height="70%" width="70%">

<br><li>Create Web-1 and Web-2 VMs  </li>
<ul>
<li>Repeat the above steps to create two more VMs, Web-1 and Web-2, for your internal network.</li>
<li>Ensure these VMs are in the same resource group and region.</li>
<li>Use the same administrator username as the JumpBox for consistency. </li>
<li>Configure each web server with 1 CPU and 2 GB of RAM.</li>
</ul>

<br><p align="center"><img src="https://i.imgur.com/zNAgnJT.png" height="70%" width="70%">
<br><p align="center"><img src="https://i.imgur.com/jgeE7EE.png" height="70%" width="70%">
<br><p align="center"><img src="https://i.imgur.com/w5triW6.png" height="70%" width="70%">

<br> WYou now have a total of 3 virtual machines in your network.
</ol>

<br>
<br>Click here to return to <a href="README.md"> README.MD</a>
