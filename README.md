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
