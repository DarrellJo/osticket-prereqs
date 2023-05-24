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

<h2>Operating Systems Used</h2>

- Windows 10 (21H2)

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
</p>

<ol>
    <li>Navigate to the Control Panel on your Windows system.</li>
    <li>Click on "Programs and Features."</li>
    <li>Locate and select "Turn Windows features on or off."</li>
    <li>A window will appear displaying a list of features. Scroll down and find "Internet Information Services (IIS)." Check the box next to it to enable IIS.</li>
    <li>Expand the "Internet Information Services (IIS)" option.</li>
    <li>Expand "World Wide Web Services."</li>
    <li>Expand "Application Development Features."</li>
    <li>Enable CGI by checking the box next to it.</li>
    <li>Also, ensure that all the features for "Common HTTP Features" are enabled.</li>
</ol>

<p>
    By following these steps, you will successfully install and enable IIS in Windows, including CGI and the necessary features for Common HTTP Features.
</p>
<br />

<p>
    <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
    Please follow these instructions to proceed with the next steps:
</p>

<ol>
    <li>Navigate to the location where the installation files are provided.</li>
    <li>I recommend downloading all of the files as a zip file for easier handling. To do this, right-click on the installation files located next to "Shared with me" and click on "Download."</li>
    <li>Once the zip file is downloaded, extract its contents to a desired location on your system.</li>
</ol>

<p>
    Now, we will proceed with the installation of PHP Manager for IIS and Rewrite Module:
</p>

<ol>
    <li>Locate the downloaded files and find the installer for PHP Manager for IIS.</li>
    <li>Double-click on the installer to start the installation process.</li>
    <li>Follow the on-screen instructions to complete the installation of PHP Manager for IIS.</li>
    <li>Repeat the following steps for Rewrite Module.</li>
</ol>

<br />

<p>
    <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
    <ol start="5">
        <li>Create a new folder on the C:\ drive by right-clicking on an empty space and selecting "New" -> "Folder." Name the folder "PHP".</li>
        <li>Now, navigate back to the location where you downloaded the files. Locate the PHP 7.3.8 files.</li>
        <li>Select all the contents of the PHP 7.3.8 folder and move them into the newly created PHP folder on the C:\ drive.</li>
        <li>After moving the files, find the "VC_redist.x86.exe" file and start the installation process by double-clicking on it. Follow the on-screen instructions to complete the installation.</li>
        <li>Next, locate the downloaded files for MySQL 5.5.62. Start the installation process by running the installer.</li>
        <li>During the installation of MySQL 5.5.62, choose the "Typical Setup" option.</li>
        <li>In the Configuration Wizard, select the "Standard Configuration" option.</li>
        <li>Create a password for the MySQL database. Since this is a lab environment, you can choose a password like "Password1" for simplicity.</li>
    </ol>
</p>
<br />

<p>
    <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
    To proceed with the remaining steps, please follow the instructions provided:
</p>

<ol>
    <li>Open IIS (Internet Information Services) as an administrator. You can do this by searching for "IIS" in the Windows Start menu, right-clicking on "Internet Information Services (IIS) Manager," and selecting "Run as administrator."</li>
    <li>Register PHP from within IIS:
        <ol>
            <li>In the IIS Manager, select the server name in the left-hand navigation pane.</li>
            <li>Double-click on "Handler Mappings."</li>
            <li>In the Actions pane on the right-hand side, click on "Add Module Mapping."</li>
            <li>Fill in the following information in the dialog box:
                <ul>
                    <li>Request Path: *.php</li>
                    <li>Module: FastCgiModule</li>
                    <li>Executable: C:\PHP\php-cgi.exe (Path to your PHP installation)</li>
                    <li>Name: PHP_via_FastCGI</li>
                </ul>
            </li>
            <li>Click "OK" to save the module mapping.</li>
        </ol>
    </li>
    <li>Reload IIS:
        <ol>
            <li>Open IIS Manager.</li>
            <li>Stop the server by clicking on the "Stop" button in the Actions pane on the right-hand side.</li>
            <li>Start the server by clicking on the "Start" button in the Actions pane.</li>
        </ol>
    </li>
    <li>Install osTicket v1.15.8:
        <ol>
            <li>Download osTicket from the Installation Files Folder.</li>
            <li>Extract the contents of the downloaded file.</li>
            <li>Copy the "upload" folder to "C:\inetpub\wwwroot" directory.</li>
            <li>Within the "C:\inetpub\wwwroot" directory, rename the "upload" folder to "osTicket".</li>
        </ol>
    </li>
    <li>Reload IIS:
        <ol>
            <li>Open IIS Manager.</li>
            <li>Stop the server by clicking on the "Stop" button in the Actions pane on the right-hand side.</li>
            <li>Start the server by clicking on the "Start" button in the Actions pane.</li>
        </ol>
    </li>
    <li>Go to sites -> Default -> osTicket:
        <ol>
            <li>In IIS Manager, expand the server name in the left-hand navigation pane.</li>
            <li>Expand "Sites" and then select "Default Web Site."</li>
            <li>Under "Default Web Site," find the "osTicket" folder and click on it.</li>
            <li>On the right-hand side, click on "Browse *:80".</li>
        </ol>
    </li>
</ol>
<br />

<p>
    <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
    Note that some extensions are not enabled:
    <br />
    <br />
    <ul>
        <li>Go back to IIS Manager.</li>
        <li>Navigate to sites -> Default -> osTicket.</li>
        <li>Double-click on PHP Manager.</li>
        <li>In the PHP Manager window, click on "Enable or disable an extension."</li>
        <li>Enable the following extensions by checking the corresponding checkboxes:
            <ul>
                <li>php_imap.dll</li>
                <li>php_intl.dll</li>
                <li>php_opcache.dll</li>
            </ul>
        </li>
        <li>Click "Apply" or "OK" to save the changes.</li>
        <li>Refresh the osTicket site in your browser to observe the changes.</li>
    </ul>
</p>
<br />

<p>
    <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
    To continue setting up osTicket and perform the necessary actions, please follow these steps:
</p>

<ol>
    <li>Rename the file:
        <ul>
            <li>Open File Explorer and navigate to "C:\inetpub\wwwroot\osTicket\include\".</li>
            <li>Locate the file "ost-sampleconfig.php".</li>
            <li>Rename it to "ost-config.php".</li>
        </ul>
    </li>
    <li>Assign permissions to "ost-config.php":
        <ul>
            <li>Right-click on "ost-config.php" and select "Properties".</li>
            <li>In the "Security" tab, click on "Disable inheritance" and choose "Remove all inherited permissions from this object".</li>
            <li>Click on "Add" to add new permissions.</li>
            <li>In the "Select Users or Groups" window, type "Everyone" and click "Check Names".</li>
            <li>Select "Everyone" and click "OK".</li>
            <li>Check the box for "Full control" under the "Allow" column for the "Everyone" group.</li>
            <li>Click "OK" to save the changes.</li>
        </ul>
    </li>
    <li>Continue setting up osTicket in the browser:
        <ul>
            <li>Open your preferred browser and access the osTicket site.</li>
            <li>Click on "Continue" to proceed with the setup.</li>
            <li>Fill in the required information, such as the database details (MySQL username, password, host, and database name).</li>
            <li>Click on "Install Now" to start the installation process.</li>
            <li>Once the installation is complete, you will be redirected to the osTicket login page.</li>
        </ul>
    </li>
</ol>

<p>
    Congratulations! You have successfully installed osTicket and completed the necessary setup steps. You can now log in and start using osTicket for your ticketing system.
</p>

