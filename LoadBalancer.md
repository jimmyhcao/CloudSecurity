<h1>Setting up a Load Balancer</h1>

<ol>

  
<li> Create a load balancer and assign a static IP address  </li>
<ul>
<li>Search for <code>Load Balancer</code> in search bar on main portal page
<li>Click + Create and use same resource group as other sources

</li>

</ul>

<br><p align="center"><img src="https://i.imgur.com/oBuBTBv.png" height="70%" width="70%">

<li>Add health prove to regularly check the VMs to make sure they receive traffic   </li>
<br><p align="center"><img src="https://i.imgur.com/rZ8yYEN.png" height="70%" width="70%">

<li> Create backend pool with both VMs added to it </li>
<br><p align="center"><img src="https://i.imgur.com/FhsT4Uo.png" height="70%" width="70%">
<br><p align="center"><img src="https://i.imgur.com/g7h01f5.png" height="70%" width="70%">


<li> Create a load balancing rule to forward port 80 from the load balancer to the Virtual Network  </li>
<br><p align="center"><img src="https://i.imgur.com/aH6Ctg5.png" height="70%" width="70%">
<br><p align="center"><img src="https://i.imgur.com/0mtrYsZ.png" height="70%" width="70%">

<li> Create a new security group rule to allow port 80 traffic from the internet to your internal Virtual Network  </li>
<br><p align="center"><img src="https://i.imgur.com/zbEK6he.png" height="70%" width="70%">

<li> Remove security group rule that blocks all traffic on Virtual Network to allow traffic from load balancer through  </li>


<li> Verify DVWA app can be reached from browser  </li>
<br><p align="center"><img src="https://i.imgur.com/n28nnVE.png" height="70%" width="70%">


</ol>

<br>
<br>Click here to return to <a href="README.md"> README.MD</a>
