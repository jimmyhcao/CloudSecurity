3<h1>Crafting Ansible Playbooks </h1>

<ol>

  
<li>Connect to jump box and connect to the Ansible container </li>
<ul>
<li>Run <code>docker container list a</code> to find the name of the container</code></li>
<li>Start the container using <code>docker start [container name]</code></li>
<li>Get a shell on the container using <code>docker attach [container name]</code></li>
  </ul>

<br><p align="center"><img src="" height="70%" width="70%">

<li>Create a YAML playbook file to use for our configuration using <code>nano /etc/ansible/pentest.yml</code>   </li>
<br><p align="center"><img src="" height="70%" width="70%">

<li> We must begin our playbook with these lines. </li>

```
---
  - name: My first playbook
    hosts: webservers
    become: true
    tasks:
```
<b>Breakdown</b>
<ul>
<li><code>---</code>: Denotes that this is a YAML file
<li><code>- name</code>: Will be the name of the playbook
<li><code>hosts</code>: Is the group of servers in the hosts file that actions will run on
<li><code>become true</code>: This will run all actions as root on the server. We must run items with root to install software and make system changes
<li><code>tasks</code></li>: Will specify what actions we want to take. Everything listed under tasks will run one at a time. 




  
</ul>


<br><p align="center"><img src="" height="70%" width="70%">





<li>   </li>
<br><p align="center"><img src="" height="70%" width="70%">

<li>   </li>
<br><p align="center"><img src="" height="70%" width="70%">

<li>   </li>
<br><p align="center"><img src="" height="70%" width="70%">

<li>   </li>
<br><p align="center"><img src="" height="70%" width="70%">


</ol>

<br>
<br>Click here to return to <a href="https://github.com/jimmyhcao/CloudSecurity-InProgress/blob/255bd281943dc73bf4b25b1e440dda6173dbe091/README.md"> README.MD</a>

