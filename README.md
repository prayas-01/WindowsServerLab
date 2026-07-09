<h1>Windows Server Lab</h1>

<h2>Description</h2>
Project is a Windows Server environment made with virtual machines to showcase experience with the tools and management features that come with Sevrer 2022.
<br />


<h2>Utilities Used</h2>

- <b>Active Directory</b> 
- <b>Group Policy Management</b>
- <b>File Share & FSRM </b>

<h2>Environments Used </h2>

- <b>Windows Server 2022</b>
- <b>Windows Enterprise 11</b>

<h2>Active Directory</h2>

-Created the USA, Asia and Europe OUs and then the added the OUs of computers, users and servers in each one.
<img src="images/Screenshot (1).png" alt="Active Directory IMG" width="100%" height="80%"> 
-Created a new user named Jack Jack.
<img src="images/Screenshot (2).png" alt="Active Directory IMG" width="100%" height="80%">
-First set a static IP address for the the Windows Server machine so that it could be used as a DNS server. Then intalled a Windows 11 Enterprise VM. Connected the new client machine to the Windows Server domain controller by putting the static IP set earlier into the preffered DNS section of the client. Joined the client by renaming the PC to WORK101 and put the domain name in the configuration(prompted administrator sign in to complete). Then moved the new client machine to USA > Computers. 
<img src="images/Screenshot (6).png" alt="Active Directory IMG" width="100%" height="80%"> 

<img src="images/Screenshot (7).png" alt="Active Directory IMG" width="100%" height="80%"> 
-Logged into the newly joined computer with Jack Jack's account that was created earlier.
<img src="images/Screenshot (4).png" alt="Active Directory IMG" width="100%" height="80%"> 
<h2>GPOs</h2>
-Created GPOs with proper naming conventions and applied them to the OUs according to what would be reasonable for an organization to do.
<img src="images/Screenshot (5).png" alt="Active Directory IMG" width="100%" height="80%"> 
-For example Jack Jack can not open up the control panel since it is not neccesary for his job duties.

<h2>File Share and FSRM</h2>

-Created a shared folder called PROJECT1. Then changed share permissions to allow every user in the domain to be able to connect.
<img src="images/Screenshot (9).png" alt="Active Directory IMG" width="100%" height="80%"> 

<img src="images/Screenshot (10).png" alt="Active Directory IMG" width="100%" height="80%"> 

-Connected to the shared folder PROJECT1 on Jack Jack's account by mapping it as a network drive on his machine.
<img src="images/Screenshot (11).png" alt="Active Directory IMG" width="100%" height="80%"> 

<img src="images/Screenshot (12).png" alt="Active Directory IMG" width="100%" height="80%"> 

-More efficient way would be to create a GPO that automatically maps the drive to the users. So created a GPO and named it accordingly. Then put the location of the folder and the drive letter and applied it to create the GPO. Then linked the GPO to the users OU within the USA OU.
<img src="images/Screenshot (17).png" alt="Active Directory IMG" width="100%" height="80%"> 

<img src="images/Screenshot (18).png" alt="Active Directory IMG" width="100%" height="80%"> 

-Updated the GPO on the client machine.
<img src="images/Screenshot (19).png" alt="Active Directory IMG" width="100%" height="80%"> 
-After restarting the machine the shared folder PROJECT1 is automatically on the mapped to the users' account.
<img src="images/Screenshot (20).png" alt="Active Directory IMG" width="100%" height="80%"> 
-First added File Server Resource Manager tools from the add roles and features wizard in Server Manager. Then opened up FSRM to set a quota on the PROJECT1 folder from earlier.
<img src="images/Screenshot (21).png" alt="Active Directory IMG" width="100%" height="80%"> 

<img src="images/Screenshot (22).png" alt="Active Directory IMG" width="100%" height="80%"> 
-Then went to file screening management and blocked types of files that couldn't be stored on that PROJECT1 folder.
<img src="images/Screenshot (23).png" alt="Active Directory IMG" width="100%" height="80%"> 

<img src="images/Screenshot (24).png" alt="Active Directory IMG" width="100%" height="80%"> 
