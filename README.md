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

- Create an Azure Virtual Machine, Windows 10, 4 vCPUs 1
- Install | Enable IIS in Windows (CGI & HTTP Features)
- Register PHP within IIS
- Install and configure osTicket
- Install HeidiSQL and complete osTicket 
  
<h2>Installation Steps</h2>
<img />

![250393230-3dfb0b5b-74a9-48c4-88e6-460a52d07527](https://github.com/JCallerx/osticket-prereqs/assets/143349237/231a6db2-e8de-4172-90d1-15ddcee81e39)


</p>
<p>
The image above shows all the prerequisites downloaded to begin our installation of osTicket.  The steps I took to get to this result are the following:
  
 - A virtual machine created in Azure with 2-4 Virtual CPUs
 - Install | Enable IIS in Windows with CGI and Common HTTP features
 - Install PHP manager for IIS, Rewrite Module, PHP 7.3.8, VC_redist.x86.exe, and MySQL 5.5.62
 - Created a directory for PHP on the c drive
  
</p>
<br />

<p>

![250301935-c44b2489-daa9-4b1c-b60e-bb3439c20dc2](https://github.com/JCallerx/osticket-prereqs/assets/143349237/3f5ae848-4838-46ad-a313-df993a6a273e)


</p>
<p>
In this step, I registered PHP from within IIS. The steps taken are the following:

  - Open IIS as an administrator (type in start menu IIS and right-click to run as administrator)
  - Click on PHP manager
  - Register new PHP version: Browse and go to the c drive to register with PHP we created in our first few steps
  - Reload IIS ( you can choose to end and start the server or you can choose to restart it)
</p>
<br />

<p>



![1](https://github.com/JCallerx/osticket-prereqs/assets/143349237/54c4f059-b99b-45d0-bf2b-4b088bdc2837)

</p>
<p>
In this image, you find the completed installation of osTicket v1.15.8 following these final steps in our installation from our prerequisites. 
  
  - Install the osTicket file
  - Extract and copy the "upload" folder to c:\inetpub\wwwroot
  - In the c:\inetpub\wwwroot, I renamed "upload" to "osTicket"
  - Reload IIS and restart the server 
  - On IIS click "Browse *:80"
  - Add extensions that are not enabled, to do so follow these steps:
      - Go to IIS > sites > default > osTicket
      - Double click PHP manager
      - Click "Enable or disable an extension"
          - Enable: php_imap.dll
          - Enable: php_intl.dll
          - Enable: php_opcache.dll
          - Refresh the osTicket site browser, observe the changes
  - Rename: ost-config.php
  - Assign Permissions: ost-config.php
  - Continue Setting up osTicket in the browser
  - Install HeidiSQL
  - Complete installation of osTicket in the browser
 
</p>
<br />
