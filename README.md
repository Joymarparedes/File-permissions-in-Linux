<h1>Active Directory Home Lab</h1>



<h2>Description</h2>
In this project an Active Directory home lab Enviroment is created using Oracle Virtual Box. Configuring and running this
lab helped me develop an understanding of how active directory and windows networking works.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>VirtualBox</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Windows server 2019</b> 

<h2>Program walk-through:</h2>

<p align="center">
we create our first virtual machine which is going to be our domain controller and is going to house active directory: <br/>
<img src="https://i.imgur.com/aJzy5sv.png" height="80%" width="80%" alt="Create Virtual Machine"/>
<br />
<br />
installing Windows server 2019 on virtual machine :  <br/>
<img src="https://i.imgur.com/Pqa1zWX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Setting up internal NIC with these specifications for this lab: <br/>
<img src="https://i.imgur.com/JLaRThB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next we are going to install active directory using "Add Roles and Features Wizard":  <br/>
<img src="https://i.imgur.com/vTHLwdE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
After the installation we have to make sure to go through "Post-deployment Configuration":  <br/>
<img src="https://i.imgur.com/MiloSEJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next we install RAS:  <br/>
<img src="https://i.imgur.com/uDqnAg8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 And then we install our NAT:  <br/>
<img src="https://i.imgur.com/tT3Ksga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 After RAS and NAT are installed and configured with continue with installing DHCP Server :  <br/>
<img src="https://i.imgur.com/VF8NfGy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
After we install DHCP server we go ahead and create our scope with the specifications provided
 in this case we use these ones for the lab:  <br/>
<img src="https://i.imgur.com/4PVCR9V.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Next we have a provided list of users and we are going to use PowerShell to run this
 script which will allow us to create multiple users with the information provided on the .txt file:  <br/>
<img src="https://i.imgur.com/Ui9puD3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  We are using PowerShell and the provided script to automate this process:  <br/>
<img src="https://i.imgur.com/v1iBUQ8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 After Powershell is done you will notice that all these users have been created:  <br/>
<img src="https://i.imgur.com/4wvjaxT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 The last thing we are doing is creating our Client:  <br/>
<img src="https://i.imgur.com/0MQKQRM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
We attach it to internal network so we can get a DHCP adress from the domain controller:  <br/>
<img src="https://i.imgur.com/v4UzcN7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 After our Client is completed we check the Ethernet adapter and also ping an adress on the internet to make sure our infrastructure is working:  <br/>
<img src="https://i.imgur.com/kyGU7in.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Now that we now that our client is working correctly, we just rename it with the pertinent information and make it a member of the domain:  <br/>
<img src="https://i.imgur.com/ERctLK9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
We can also make sure the Client is working correctly by checking its connection to DHCP and also in the Active Directory:  <br/>
<img src="https://i.imgur.com/EmpB4B9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
