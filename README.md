<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create Virtual Machine in Azure
- Connect Virtual Machine to Remote Desktop
- Enable IIS in Windows (Remote Desktop)
- Install Web Platform Installer (Remote Desktop)
- Add My SQL 5.5 (Remote Desktop)

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/aObAFZ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download osTicket. Extract and copy the “upload” folder INTO c:\inetpub\wwwroot. Within c:\inetpub\wwwroot, Rename “upload” to “osTicket." 
Open IIS Manager, select Go to sites -> Default -> osTicket
On the right, click “Browse *:80.

</p>
<br />

<p>
<img src="https://i.imgur.com/gyv3WbS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable Extensions in IIS. Go back to IIS, sites -> Default -> osTicket. Double-click PHP Manager. Click “Enable or disable an extension.”
Enable: php_imap.dll; php_intl.dll; php_opcache.dll
Refresh the osTicket site in your browse, observe the changes. Rename: 
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
Assign Permissions: ost-config.php. Disable inheritance -> Remove All; New Permissions -> Everyone -> Apply
Refresh osTicket. 

</p>
<br />

<p>
<img src="https://i.imgur.com/FGLByvT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue Setting up osTicket in the browser. [(Name:Helpdesk; Insert eamail (email from customers)]
Default email (receives email from customers)
Download and Install HeidiSQL (Create a new session, root/Password1, Connect to the session, Create a database called “osTicket”)
Continue Setting up osticket in the browser.
MySQL Database: osTicket
MySQL Username: root
MySQL Password: Password1
Click “Install Now!”


</p>
<br />
