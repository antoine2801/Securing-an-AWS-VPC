<h1>Building and Securing an AWS VPC</h1>



<h2>Description</h2>
Create a secure Virtual Private Cloud (VPC) on AWS to establish isolated network environments. Design subnets for public and private resources across different Availability Zones. Configure an Internet Gateway for public access and a NAT Gateway or instance for private subnet internet connectivity. Enhance security using Security Groups and Network Access Control Lists (NACLs) with customized inbound and outbound rules. Explore VPC peering or VPN connections for additional connectivity options. Enable VPC Flow Logs to monitor traffic and ensure high availability by deploying resources across multiple zones. 
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 


<h2>Environments Used </h2>

- <b>AWS</b> 

<h2>Project walk-through:</h2>

<p align="center"> 
 <h3> VPC Infrastructure Design -  State 0 <h3/>
<img src="https://i.imgur.com/XvMtAg9.pngg" height="80%" width="80%" alt="Building and Securing an AWS VPC Steps"/>

 
<img src="https://i.imgur.com/D27Yy76.pngg" height="80%" width="80%" alt="Building and Securing an AWS VPC Steps"/>
 
- <b>A Virtual Private Cloud (VPC) is a logically isolated section of the AWS cloud where you can launch AWS resources in a virtual network that you define. It allows you to have complete control over your virtual networking environment, including IP address ranges, subnets, route tables, and network gateways. With a VPC, you can securely connect your AWS resources to your on-premises network using VPN or AWS Direct Connect. It provides a secure and scalable infrastructure for running your applications in the cloud while maintaining control over your network configuration.</b> 
<br />
<br />

<h3> VPC Infrastructure Design with Subnets -  State 1 <h3/>
<img src="https://i.imgur.com/cUYFkwh.pngg" height="80%" width="80%" alt="Building and Securing an AWS VPC Steps"/>

 
- <b> Subnets are used to divide the IP address range of a VPC into smaller, more manageable networks. Each subnet has its own CIDR block, which determines the range of IP addresses that can be assigned to resources within that subnet </b>

 
- <b> Resilient, within a particular AZ. 1 Subnet => 1 AZ, 1 AZ => 0+Subnets </b>
- <b> IPv4 CIDR is a subset of the VPC CIDR </b>
- <b> Cannot overlap with other subnets </b>
- <b> Subnets can communicate with other subnets in the VPC </b>
- <b> Reserved IP addresses (5 in total) </b>
- <b> Network Address (10.16.16.0) </b>
- <b> 'Network+1' (10.16.16.1) - VPC Router </b>
- <b> 'Network+2' (10.16.16.2) - Resverd DNS </b>
- <b> 'Network+3' (10.16.16.1) - Resverd Future Use </b>
- <b> Broadcast Address 10.16.31.255 - Last IP in subnet </b>
<img src="https://i.imgur.com/QLIjXTH.png" height="80%" width="80%" alt="Building and Securing an AWS VPC Steps"/>
<img src="https://i.imgur.com/MTx65Zc.png" height="80%" width="80%" alt="Building and Securing an AWS VPC Steps"/>
<img src="https://i.imgur.com/Ot82sML.png" height="80%" width="80%" alt="Building and Securing an AWS VPC Steps"/>

<br />
<br />




</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
