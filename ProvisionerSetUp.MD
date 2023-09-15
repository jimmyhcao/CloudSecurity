
<h1>Provisioner Set Up</h1>

<ol>

  
<li> Run the following command to start your container and connect to it. (Note that the prompt changed to "root@90d26a19d0c.)</li><br>

```
docker run -it cyberxsecurity/ansible /bin/bash
```
<p align="center"><img src="https://i.imgur.com/jkr9ND7.png" height="70%" width="70%">

<li>We will now need to create a SSH key using ssh-keygen  </li>
<br><p align="center"><img src="https://i.imgur.com/jkr9ND7.png" height="70%" width="70%">

<li> Run <code>ls .ssh/</code> to view the keys created  </li>
<br><p align="center"><img src="" height="70%" width="70%">

<li>Run <code>cat .ssh/id_rsa.pub</code> to view your public key. Copy your public key string   </li>
<br><p align="center"><img src="" height="70%" width="70%">

<li> From the Azure home page, go into one of the VM's detail page. On the left panel navigate to "reset password" and enter the public key that was copied. </li>
<br><p align="center"><img src="" height="70%" width="70%">

<li>Test connection of our Jump Box Ansible Container. Since only TCP connections are enabled for SSH in our security group rule, ICMP packets will be denied, making ping fail   </li>
<br><p align="center"><img src="https://i.imgur.com/7Km5wBY.png" height="70%" width="70%">

<li> However, if we connect to our VM with SSH, we will be able to accept the key.</li><br>
Run

```
ssh <username>@<webVM-IP>

#For our example we ran 
ssh HomeLab@10.0.0.5
```

<br><p align="center"><img src="https://i.imgur.com/kkz3qEW.png" height="70%" width="70%"><br>


<li> Run <code> exit</code> to close the SSH connection and return to the Ansible container. From here run <code>ansible</code>  </li>
<br><p align="center"><img src="" height="70%" width="70%">

<li> At this point we must make two changes to the configuration files to allow Ansible make connections. This is because Ansible needs to know which administrative username to use when making SSH connections. For our example <b>HomeLab</b> was our administrative username we created, so it will need to be added to the configuration file. </li><br>
All of hte Ansible configuration files are located in the <code>/etc/ansible</code> directory. we can view these files by running <code> cd /etc/ansible</code> followed by <code>ls</code>
<br><p align="center"><img src="https://i.imgur.com/musHynk.png" height="70%" width="70%">

<li>   </li>
<br><p align="center"><img src="" height="70%" width="70%">
</ol>

<br>
<br>Click here to return to <a href="https://github.com/jimmyhcao/CloudSecurity-InProgress/blob/255bd281943dc73bf4b25b1e440dda6173dbe091/README.md"> README.MD</a>
