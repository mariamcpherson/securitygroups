<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs)</h1>
<p>
Network Security Groups (NSGs) are a type of security feature commonly used in cloud computing environments, particularly in Infrastructure-as-a-Service (IaaS) platforms like Microsoft Azure and Amazon Web Services (AWS). NSGs act as a virtual firewall to control inbound and outbound network traffic to and from resources deployed within a virtual network.
</p>
<p>
The primary purpose of Network Security Groups is to control and filter network traffic based on rules defined by administrators. These rules are typically specified using a set of security rules that define allowed or denied traffic based on source and destination IP addresses, ports, and protocols. NSGs work at the network layer (Layer 4) of the OSI model, making them capable of filtering traffic based on TCP, UDP, and ICMP protocols.
</p>
<p>
Using Network Security Groups is an essential aspect of securing cloud-based infrastructures. They help ensure that only authorized network traffic is allowed to reach resources, reducing the attack surface and protecting sensitive data and applications from unauthorized access.
</p>
<p>
In this tutorial, we will experiment with Network Security Groups.
</p>  <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Windows Server 2022

<h2>Pre-requisites</h2>

- Direct Directory installed in Windows Server VM in Azure and set as Domain Controller
- Windows 10 VM in Azure joined to the Domain Controller


<h2>High-Level Steps</h2>

- Create a Security Group in Windows Server VM
- Create "accounting" folder in Windows Server M and set permissions
- Assign User to Security Group
- Step 4

<h2>Actions and Observations</h2>

<p>
- Step 2:
<p>
We will start by creating a new Organizational Unit, named _SECURITY_GROUPS, for organization purposes, and inside we will crate a new Security Group, named ACCOUNTANTS. Once you've created the Organizational Unit (Explained in the Active Directory Tutorial), right-click on it and select New → Group. Name it ACCOUNTANTS, and in Group Type, select Security.
</p>

<img src="https://github.com/mariamcpherson/securitygroups/assets/139581822/bc274955-fb5e-42b8-8eb8-d2bd92c0c4d3"/>
</p>

<img src="https://github.com/mariamcpherson/securitygroups/assets/139581822/8a36a6bd-2552-4545-920b-187946f85091"/>
</p>

<p>
- Step 2:
<p>
Now we will create a new file folder in the Domain Controller VM (Windows Server) named "accounting" in C:\, and then we will assign the sharing permissions so that only members of the ACCOUNTANTS security group have read and write access to the files within that folder. In order to assign the corresponding permission, right click on the "accounting" folder, Properties → Sharing → Share..., then type ACCOUNTANTS, and assign Read/Write.
</p>

<p>
<img src="https://github.com/mariamcpherson/securitygroups/assets/139581822/c07821bf-a633-42a8-97b8-68b4e66a8844"/>
</p>

<p>
- Step 3:
</p>

<p>
We have no users inside the ACCOUNTANTS Security Group to access the "accounting" folder. Let's test that we did everything correctly and make one of our Domain Users a Member of the ACCOUNTANTS security group. In my case, I chose 
</p>
<p>
<p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
