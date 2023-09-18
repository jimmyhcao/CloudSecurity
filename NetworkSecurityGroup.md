
<h1>Creating Network Security Group</h1>

<ol>

  
<li>From Azure's homescreen, click create a resource and search for "network security group". Navigate to the network security group icon and click create  </li>
<br><img src="https://i.imgur.com/BVAy7Re.png" height="70%" width="70%">

<br><li> Ensure that the resource group we created earlier is selected and then name your network security group. We will name ours <b>HomeLABSG</b></li>
<br><img src="https://i.imgur.com/LryYNSo.png" height="70%" width="70%">

<br><li>After creating the network security group, click on the resource to make configurations. We can find our settings on the left panel. We will configure <b>inbound security rules in this next step</b></li>
<br><img src="https://i.imgur.com/K05XPxJ.png" height="70%" width="70%"><br>

<br><li>After clicking on the inbound security rules on the left panel, click on the <b>+ Add</b> button on the top of the middle screen. A panel will appear on the right side of the screen where we can set the rules for inbound traffic. For increased security, we will create a deny rule that will deny:<br>
<ul>
<li>From any source IP
<li>From all source ports using the wildcard (*)
<li>To any destination IP
<li>To any destination ports using the wildcard (*)
<li>Any protocol used
</ul>
<br><img src="https://i.imgur.com/QGL00eB.png" height="70%" width="70%"><br>
<br>Since we are setting the priority for this rule at a higher number, it will be applied last


<br><li>Our VNet is now protected by a network security group rule that blocks all inbound traffic</li>
<br><img src="https://i.imgur.com/beKUAvg.png" height="70%" width="70%">




</ol>

<br>
<br>Click here to return to <a href="https://github.com/jimmyhcao/CloudSecurity-InProgress/blob/255bd281943dc73bf4b25b1e440dda6173dbe091/README.md"> README.MD</a>
