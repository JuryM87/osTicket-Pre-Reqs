<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>What is osTicket?</h2>
It's a widely used trusted open source ticketing system. It manages, organizes, and archive all support requests and response in one place while providing your customer with great communication and accountability.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure Virtual Machine
- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- Heidi SQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites </h2>

- Azure Virtual Machine
- osTicket Installation Files

<h2>Installation Steps</h2>

<img src="https://i.imgur.com/VNGku7k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First, Create Resource Group on Microsoft Azure. Think of Resource Groups as a folder. We will name our Resource Group RG-osTicket. Now, it is time to create a virtual machine under the RG. Think of the virtual machine as a computer on the internet or harddrive you can access within your own computer. We will be using Windows 10 with 4vCPUs. We can name this VM "VM-osTicket".

Create a username and password for your VM. You will be logining in to it like a regular computer ! So, take notes to not forget your login credentials. I set my username to be "labuser" and "set your own password".

Now that our machine is ready, we will connect to it using Remote Desktop Connection. before that, let us grab the public IP address of the VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/7GiGbIy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we are connected, let us enable IIS (Internet Information Services) IIS is a Microsoft web server that runs on Windows operating system and is used to exchange static and dynamic web content with internet users. IIS can be used to host, deploy, and manage web applications using technologies such as ASP.NET and PHP.

Start Menu > Windows Feature > Type- Internet Information Services > Click- World Wide Web Services > Click- Application Development Features > Click- CGI
</p>
<br />

<p>
<img src="https://i.imgur.com/lPTyHjZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
</p>
<p>
<a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> Now it's time to download and install the necessary files for osTicket and Heidi SQL
</p>
<br />
<img src="https://i.imgur.com/8lJoTkk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Begin with Installation Files (Click on the hyperlink above for Installation Files)
  
- Download and Install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
- Download and Install the Rewrite Module (rewrite_amd64_en-US.msi)
- Create a directory C:\PHP
  
<img src="https://i.imgur.com/WNmZkaW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
- From the Installation Files, download and install VC_redist.x86.exe.
- From the Installation Files, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
  
<img src="https://i.imgur.com/SWjNLJ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Open IIS Manager as an Admin User, Register the PHP using the PHP folder

<img src="https://i.imgur.com/71M6tbj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Next download osTicket, extract the content to the folder c:\inetpub\wwwroot. Rename the folder "Upload" to "osTicket".
<img src="https://i.imgur.com/ATeTD8U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


- In IIS Manager, open PHP Manager. We need to enable three extensions by the name of 
- php_imap.dll 
- php_intl.dll 
- php_opcache.dll 

<img src="https://i.imgur.com/DJCmF9T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- Reload IIS Manager and Click "Sites > Default > osTickets. On the right side, click " Browse *:80" to open the osTicket web-interface.
- Make it a habit to Click-Restart in IIS to relect all changes made

<img src="https://i.imgur.com/lGIssF4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Awesome, now lets return to c:\inetpub\wwwroot\osticket\include, here look for the file named "ost-sampleconfig.php" We will rename it to "ost-config.php". 
- Once that is completed, right click the file, open properties, under the secruity tab, "Disable Inheritance" 
- Then Remove all new permissions, and give everyone permissions.

<img src="https://i.imgur.com/lAjli0e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- Download and Install HeidiSQL From the Installation Files
- Open Heidi SQL
- Create a new session, root/Password (That you created)
- Connect to the session
- Create a database called “osTicket”
We are Almost There! Let's return to osTicket in the web-interface. Name the Helpdesk to what makes you content. Anything will do. Just remember your login credentials.

<img src="https://i.imgur.com/5u2Qt08.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Continue Setting up osticket in the browser

- MySQL Database: osTicket
- MySQL Username: root
- MySQL Password: Password1
- Click “Install Now!”

<img src="https://i.imgur.com/NxS4nvK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/dF9uk1p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
