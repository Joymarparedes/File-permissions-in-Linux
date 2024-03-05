<h1>File permissions in Linux</h1>



<h2>Description</h2>
The research team at my organization needs to update the file permissions for certain files and
directories within the "projects" directory. The permissions do not currently reflect the level of
authorization that should be given. Checking and updating these permissions will help keep their system secure.
<br />

<h2>Check file and directory details:</h2>

The following code demostrates how I used Linux commands to determine the existing permissions set for  a specific directory in the file system: <br/>

<img src="https://i.imgur.com/2I1Q8T6.png" height="80%" width="80%" alt="Create Virtual Machine"/>
<br />
The first line of the screenshot displays the command I entered. and the other lines display the 
 output. The code list all contents of the "projects" directory. I used the ls command with the
 -la option to display a detailed listing of the file content that also returned hidden files. The
 output of my command indicates that there is one directory named "dreafts", oned hidden file 
 named. "project_c.txt, and five othe project files. The 10-character string in the first 
 column represents the permissions set on each file or directory. 
<br />
installing Windows server 2019 on virtual machine :  <br/>
<img src="https://i.imgur.com/Pqa1zWX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<h2>Describe the permissions string</h2>

The 10-character string can be deconstructed to determine who is authorized to access the
file and their spacific permissions. The characters and what they represent are as follows:

- 1st character: This chracter is either a "d" or hyphen (-) and idicates the file typed. if it's
  a "d", it's a directory . if it's a hyphen (-), it's a regular file. 

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
