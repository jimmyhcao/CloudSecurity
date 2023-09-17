<h1>Crafting Ansible Playbooks </h1>

<ol>

  
<li>Connect to jump box and connect to the Ansible container </li>
<ul>
<li>Run <code>docker container list a</code> to find the name of the container</code></li>
<li>Start the container using <code>docker start [container name]</code></li>
<li>Get a shell on the container using <code>docker attach [container name]</code> (our container name that was created for this project was <code>unruffled_cohen</code></li></ul>

<br><p align="center"><img src="https://i.imgur.com/A27wKrW.png" height="70%" width="70%">

<li>Create a YAML playbook file to use for our configuration using <code>nano /etc/ansible/pentest.yml</code>   </li>


<li> We must begin our playbook with these lines. </li><br>

```
---
  - name: Config Web VM with Docker
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
<li><code>tasks</code>: Will specify what actions we want to take. Everything listed under tasks will run one at a time. 
</li>
</ul><br>


<li> Continue to add the following modules to our playbook. <br>
 <br> 
<ul><li> Use Ansible <code>apt</code> module to install <code>docker.io</code>. Keep in mind that <code>update_cache</code> will need to be used here as well</li>
<li>Use Ansible <code>apt</code> module to install <code>python3-pip</code> </li>
</ul>
</li><br>

```
  - name: docker.io
    apt:
  		update_cache: yes
      name: docker.io
      state: present

  - name: Install pip3
    apt:
      force_apt_get: yes
      name: python3-pip
      state: present
```


<br>

<li>Use Ansible <code>pip</code> module to install <code>docker</code>  </li><br>

```
  - name: Install Python Docker module
    pip:
      name: docker
      state: present
```

<br>

<li> Use Ansible <code>docker-contianer</code> module to install the <code>cyberxsecurity/dvwa</code> container</li><br>
<ul><li><code>published_ports</code> should be 80 for the container port and 80 for the host port
<li><code>restart_policy:</code> should be <code>always</code> to ensure that the container resarts if the web VM is restarted. If this setting is not on then the container will need to be restarted manually whenever the VM is resarted.</li>
</ul><br>

```
  - name: download and launch a docker web container
    docker_container:
      name: dvwa
      image: cyberxsecurity/dvwa
      state: started
      restart_policy: always
      published_ports: 80:80
```


<br>

<li>Use <code>systemd</code> module to restart docker service when the machine reboots  </li><br>

```
    - name: Enable docker service
      systemd:
        name: docker
        enabled: yes
```




<li> The completed playbook will look like this</li><br>

```
---
- name: Config Web VM with Docker
  hosts: webservers
  become: true
  tasks:
  - name: docker.io
    apt:
      force_apt_get: yes
      update_cache: yes
      name: docker.io
      state: present

  - name: Install pip3
    apt:
      force_apt_get: yes
      name: python3-pip
      state: present

  - name: Install Docker python module
    pip:
      name: docker
      state: present

  - name: download and launch a docker web container
    docker_container:
      name: dvwa
      image: cyberxsecurity/dvwa
      state: started
      published_ports: 80:80

  - name: Enable docker service
    systemd:
      name: docker
      enabled: yes
```


</ol>

<br>
<br>Click here to return to <a href="README.md"> README.MD</a>

