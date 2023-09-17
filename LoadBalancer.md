<h1>Setting up a Load Balancer</h1>

<ol>

  
<li> Create a load balancer and assign a static IP address  </li>
<ul>
<li>Search for <code>Load Balancer</code> in search bar on main portal page
<li>Click + Create and use same resource group as other sources
<li>

</li>

</ul>

<br><p align="center"><img src="https://i.imgur.com/oBuBTBv.png" height="70%" width="70%">

<li>Add health prove to regularly check the VMs to make sure they receive traffic   </li>
<br><p align="center"><img src="" height="70%" width="70%">

<li> Create backend pool with both VMs added to it </li>
<br><p align="center"><img src="" height="70%" width="70%">

<li> Create a load balancing rule to forward port 80 from the load balancer to the Virtual Network  </li>
<br><p align="center"><img src="" height="70%" width="70%">

<li> Create a new security group rule to allow port 80 traffic from the internet to your internal Virtual Network  </li>
<br><p align="center"><img src="" height="70%" width="70%">

<li> Remove security grou rule that blocks all traffic on Virtual Network to allow traffic from load balancer through  </li>
<br><p align="center"><img src="" height="70%" width="70%">

<li> Verify DVWA app can be reached from browser  </li>
<br><p align="center"><img src="" height="70%" width="70%">


</ol>

<br>
<br>Click here to return to <a href="README.md"> README.MD</a>
