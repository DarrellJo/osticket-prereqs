# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial provides a step-by-step guide on the prerequisites and installation process of osTicket, an open-source help desk ticketing system. To begin, we need to create a Virtual Machine (VM) using the Microsoft Azure Portal. Afterwards, we will utilize the Remote Desktop Connection to access our newly created VM. Please note that if you are using a Mac, you will need to install Microsoft Remote Desktop. To simplify the process, I have included all the necessary installation files for osTicket. Please click the link provided to access the files and proceed with the installation. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure Virtual Machine
- [osTicket Installation Files](https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)
- [Remote Desktop](https://apps.apple.com/us/app/microsoft-remote-desktop/id1295203466?mt=12) 


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To start, we will proceed with the installation and enabling of IIS (Internet Information Services) in Windows. Additionally, we will enable CGI and Common HTTP Features. Please follow the steps below:

   - Navigate to the Control Panel on your Windows system.
   - Click on "Programs and Features."
   - Locate and select "Turn Windows features on or off."
   - A window will appear displaying a list of features. Scroll down and find "Internet Information Services (IIS)." Check the box next to it to enable IIS.
   - Expand the "Internet Information Services (IIS)" option.
   - Expand "World Wide Web Services."
   - Expand "Application Development Features."
   - Enable CGI by checking the box next to it.
   - Also, ensure that all the features for "Common HTTP Features" are enabled.

By following these steps, you will successfully install and enable IIS in Windows, including CGI and the necessary features for Common HTTP Features.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Please follow these instructions to proceed with the next steps:

  Navigate to the location where the installation files are provided.
    I recommend downloading all of the files as a zip file for easier handling. To do this, right-click on the installation 
  files located next to "Shared with me" and click on "Download."
    Once the zip file is downloaded, extract its contents to a desired location on your system.

Now, we will proceed with the installation of PHP Manager for IIS and Rewrite Module:

   - Locate the downloaded files and find the installer for PHP Manager for IIS.
   - Double-click on the installer to start the installation process.
   - Follow the on-screen instructions to complete the installation of PHP Manager for IIS.
   - Repeat the following steps for Rewrite Module.

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
   - Create a new folder on the C:\ drive by right-clicking on an empty space and selecting "New" -> "Folder." Name the folder "PHP".

   - Now, navigate back to the location where you downloaded the files. Locate the PHP 7.3.8 files.

   - Select all the contents of the PHP 7.3.8 folder and move them into the newly created PHP folder on the C:\ drive.

   - After moving the files, find the "VC_redist.x86.exe" file and start the installation process by double-clicking on it. Follow the on-screen instructions to complete the installation.
  
    - Next, locate the downloaded files for MySQL 5.5.62. Start the installation process by running the installer.

    - During the installation of MySQL 5.5.62, choose the "Typical Setup" option.

    - In the Configuration Wizard, select the "Standard Configuration" option.

    - Create a password for the MySQL database. Since this is a lab environment, you can choose a password like "Password1" for simplicity.
</p>
<br />
