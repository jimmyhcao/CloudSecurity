<h1>Creating Virtual Machines (VMs) </h1>
<ol>

  
<li>From homescreen, create a resource and search for "virtual machine". Then navigate to the Virtual machine icon</li>
<br><p align="center"><img src="https://i.imgur.com/S1PKpj7.png" height="70%" width="70%">

<br><li>When creating a virtual machine, ensure that the subscription and resource group is the same as our virtual network and security group. In this step we will be naming our VM. For our first VM we will be giving it the name "JumpBox" so we can easily distinguish it from the other VMs. Organizations may choose different OS images based on organizational needs, however for this project to keep costs low we will go with the bare minimum needed for this project to function. Our Jump Box will only require 1 CPU and 1 G of RAM. </li>
<br><p align="center"><img src="https://i.imgur.com/rtIbfJ9.png" height="70%" width="70%">

<br><li>After entering in basic information, we can see there is also an <b>Administrator account</b> set up at the bottom of the page on the Basics tab. Since security is our most upmost concern, we will approach this with a "ground up security approach", in which we implement security measures in a system or organization from the very beginning, starting with the foundational elements and principles.

<br>Enabling password authentication for SSH on a server is considered insecure due to the vulnerability of passwords being susceptible to brute-force attacks. From this point forward, our cloud server access will exclusively rely on cryptographic SSH keys, password authentication will not be allowed.
</li>

<i>SSH authentication works by generating a key pair with the private key being stored on your computer while the public key is stored on the server you want access to. When attempting to gain access the SSH protocol will check if the key pair is a match, once verified the user will be authenticated access.</i>
<p align="center"><img src="https://i.imgur.com/OvzQROD.png" height="70%" width="70%">

<br><li>To generate a key pair we will need to run <code>ssh-keygen</code> into a <b>Git Bash</b> terminal. To display our public key, run the command <code>cat ~/.ssh/id_rsa.pub</code>. Highlight and copy the SSH key for later use. </li>
<ul>
<li><code>id_rsa</code></li> is our private key (do not share)
<li><code>id_rsa.pub</code></li> is our public key
  </ul>
<br><p align="center"><img src="https://i.imgur.com/blgd5YN.png" height="70%" width="70%">
<br><p align="center"><img src="https://i.imgur.com/dknvmdq.png" height="90%" width="90%">


<br><li>Next we will use our newly generated public key and attach it to our Jump Box. Under the Administrator account, we will create a username HomeLab for simplicity. This is where we will paste our public key that we had copied earlier.      </li>
<br><p align="center"><img src="https://i.imgur.com/ShwgSJu.png" height="70%" width="70%">


<br><li> Move to the <b>Networking</b> tab and set the following settings for Virtual network, network security group etc.  </li>
<br><p align="center"><img src="https://i.imgur.com/ms78hZu.png" height="70%" width="70%">

<br><li> Review and create      </li>
<br><p align="center"><img src="https://i.imgur.com/b8cDCzc.png" height="70%" width="70%">

<br><li> We will now see our Jump Box virtual machine on our main page   </li>
<br><p align="center"><img src="  https://i.imgur.com/7L4n511.png " height="70%" width="70%">

<br><li>  We'll need to establish two more virtual machines, Web-1 and Web-2, which will serve as servers within our internal network. These procedures will resemble the process of creating our Jump Box VM, albeit with some minor distinctions and important considerations to keep in mind. </li>
<ul>
<li>VMs will need to be in the same resource group as everything else</li>
<li>VMs need to be in the same region as our resource group and security group</li>
<li>The administrator username will be identical to that of our Jump Box VM to make it easier to remember </li>
<li>These web servers will need to have 1 CPU and 2 G of RAM</li>
</ul>

<br><p align="center"><img src="https://i.imgur.com/zNAgnJT.png" height="70%" width="70%">
<br><p align="center"><img src="https://i.imgur.com/jgeE7EE.png" height="70%" width="70%">
<br><p align="center"><img src="https://i.imgur.com/w5triW6.png" height="70%" width="70%">

<br> We now have a total of 3 virtual machines on our network.
</ol>

<br>
<br>Click here to return to <a href="https://github.com/jimmyhcao/CloudSecurity-InProgress/blob/255bd281943dc73bf4b25b1e440dda6173dbe091/README.md"> README.MD</a>
