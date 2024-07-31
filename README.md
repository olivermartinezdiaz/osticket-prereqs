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

- Internet Information Services (IIS)
- MySQL 5.5
- Add All Simple Versions of x86 PHP Up To v7.3
- Install osTicket v1.15.8
- Reload iis (Open IIS, Stop and Start The Server
- Enable Extensions In iis
- osTicket Refresh On Browser
- File Clean Up For Optimal Use

<h2>Installation Steps</h2>

<h2> Adding Internet Information Services

<p>

<img src="https://i.imgur.com/C4u4X0U.png" alt="osTicket logo"/>


>
</p>
<p>
STEP 1: Install Or Enable Internet Information Services In The Control Panel.
<img src="https://i.imgur.com/cpltf0k.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/6JYTGl6.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/AIj4xty.png" alt="osTicket logo"/>

  <h2> Put 127.0.0.1 into the browser to verify steps were inputted correctly 
<img src="https://i.imgur.com/aMVPvn9.png" alt="osTicket logo"/>

STEP 2: Download and install files

PHP Manager for IIS
<img src="https://i.imgur.com/nHP8nK7.png" alt="osTicket logo"/>

Rewrite Module 
<img src="https://i.imgur.com/PpZ5gxK.png" alt="osTicket logo"/>

PHP 7.3.8
<img src="https://i.imgur.com/7M3A5lQ.png" alt="osTicket logo"/>

VC_redist.xe86.exe
<img src="https://i.imgur.com/iBqE8hH.png" alt="osTicket logo"/>

MySQL 5.5.62.
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration -> Create a username and password you will need this to install Osticket.
<img src="https://i.imgur.com/PKBaRFr.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/ZJHuuGe.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/lLWuL1V.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/D88RE1p.png" alt="osTicket logo"/>

Step 3: Open IIS as an Admin, Register PHP from within IIS,
Reload IIS (Open IIS, Stop and Start the server)
<img src="https://i.imgur.com/P7DwYWt.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/zJGN1HI.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/gA0rqo0.png" alt="osTicket logo"/>
>
</p>
<p>

</p>
<br />


<h2> Step 4:Install osTicket v1.15.8
Download osTicket from the Installation Files Folder
Extract and copy “Upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
</p>
<img src="https://i.imgur.com/kXUj3qp.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/6KCXTw7.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/YR9VRQX.png" alt="osTicket logo"/>
</p>

<h2>Step 5:Go to sites -> Default -> osTicket
On the right, click “Browse *:80” If steps were followed correctly the OSticket installer screen should open
<img src="https://i.imgur.com/x8Eh4Ew.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/qd9DKfT.png" alt="osTicket logo"/>


>
</p>
<p>
Step 6:Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browse, observe the changes
</p>
<img src="https://i.imgur.com/FqeoKkf.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/iwC3lr0.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/wxAr9YI.png" alt="osTicket logo"/>
</p>
Step 7: Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
<img src="https://i.imgur.com/aQQJnc4.png" alt="osTicket logo"/>


Step 8: Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All
<img src="https://i.imgur.com/WIDPueB.png" alt="osTicket logo"/>
>
</p>
<p>
Step 9:Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)
From the Installation Files, download and install HeidiSQL.
Open Heidi SQL
Create a new session, root/Password1
Connect to the session
Create a database called “osTicket”
Continue Setting up osticket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: Password1
Click “Install Now!”
<img src="https://i.imgur.com/5ZksyTn.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/b25YDie.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/KjwNt4n.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/dxaZUfh.png" alt="osTicket logo"/>
<img src="https://i.imgur.com/DPRPIyB.png" alt="osTicket logo"/>
>
</p>
<p>
Step10:Congratulations, hopefully it is installed with no errors!
Browse to your help desk login page: http://localhost/osTicket/scp/login.php
<img src="https://i.imgur.com/fDxNQDr.png" alt="osTicket logo"/>

<h2> Cleaning Up Files
Delete: C:\inetpub\wwwroot\osTicket\setup
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
<img src="https://i.imgur.com/25lIoCR.png" alt="osTicket logo"/>
