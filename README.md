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

- Microsoft Azure
- Virtual Machine
- Internet Information Services (IIS)
- osTicket Installation Files: https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD

<h2>Installation Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/2afb8b71-8e70-4f89-a45d-a66a0fc3a06e"/>
</p>
<p>
1. The first thing you wanna do when making the virtual machine is create a new resource group, naming it "osTicket". As shown in the image above, name the virtual machine "osticket-vm" and choose "Windows 10 Pro, version 22H2" for the system.  
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/61f0561f-ebfc-44ad-a94d-7eebc3e49594"/>
</p>
<p>
2. For the size of the virtual machine, it is HIGHLY recommended that it has 2 vcpus and 8GiB of memomry minimum. Choosing the Standard_D2s-v3 will do just fine. Under "Administer Account", choose a simple and easy to remember username and password. Under "Licensing", make sure to check the box so the virtual machine can pass validation. After that, click "Review + Create".
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/06d37fc0-6fcf-4346-81d4-4707634ce09b"/>
</p>
<p>
3. After the virtual machine is reviewed and passes validation, click "Create" and your virtual machine will begin the process of being created! It will take some time and automatically start running. 
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/ba081390-f1e5-4673-bde3-fd6d54794ba2"/> 
<img src="https://github.com/user-attachments/assets/5bb37c3a-8b45-4c38-95aa-a04a84b44b8f"/>
</p>
<p>
4. Once your virtual machine is finished, you will need the Public IP address to access it. You can click the virtual machine and see the Public IP address on the right side of the screen, as shown in the image above. Copy the IP address and open up Remote Desktop Connection. Once the IP address is confirmed, you will need to use the credentials you created and you will be put into the virtual machine. 
</p>

<p>
5. Now that you have accessed your virtual machine, you will need to download the osTicket Installation Files within the virtual machine. Once you have done that, unzip the folder onto your desktop.
</p>

<p>
6. Access your control panel and choose "Uninstall a program". Next, click on "Turn Windows features on or off". From there, we will turn on "Internet Information Services" (IIS).
</p>
<p>
<img src="https://github.com/user-attachments/assets/50f2852d-bec0-44c2-924f-97dc139cc7c6"/>
<img src="https://github.com/user-attachments/assets/0a0926fb-9216-4df4-bd5d-45e1040df43a"/>
</p>

<p>
7. Once you find Internet Information Services, click on the box to turn it on. Next, click the "+" sign to expand the folder and find "World Wide Web services". Expand that folder and find "CGI". Click on the box to activate it. 
</p>
<p>
<img src="https://github.com/user-attachments/assets/758814a2-0de5-44e0-b15d-888a84ac1833"/>
<img src="https://github.com/user-attachments/assets/0a03cfd3-00a3-4d03-a4c5-0eea259a909a"/>
</p>

<p>
8. From the "osTicket-Installation-Files" folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi). Go through the install process and complete the installation.
</p>

<p>
9. From the "osTicket-Installation-Files" folder, install the Rewrite Module (rewrite_amd64_en-US.msi). 
</p>

<p>
10. Create a folder in the C drive called PHP (C\:PHP).
</p>

<p>
11. From the "osTicket-Installation-Files" folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the "C:\PHP" folder. The destination should look like the image below.
</p>
<p>
<img src="https://github.com/user-attachments/assets/a77c292c-1fa1-4828-b25c-0ae22a7ade18"/>
</p>

<p>
12. From the "osTicket-Installation-Files" folder, install VC_redist.x86.exe.
</p>

<p>
13. From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi). Choose "Typical Setup", launch the configuration wizard, then choose "Standard Configuration". For the root password, it is absolutely CRUCIAL that you remember it. In this case, you can just use "root" as the password (For real life situations, use a much more complex password). Once you typed the password, click "Next" then execute the process.
</p>
<p>
<img src="https://github.com/user-attachments/assets/703fc5b5-5db4-45fd-aa4c-a812b99e5e88"/>
<img src="https://github.com/user-attachments/assets/489d2e5b-ea92-4039-9abb-7e3f05430845"/>
</p>

<p>
14. Now that you have everything installed and set up, next step is open IIS as an administrator. Once you have that open, click on "PHP Manager". Next, click "Register new PHP version" and you'll be given a prompt to provide a path to the php executable file. Click the three dots and the path should be "C:\PHP\php-cgi.exe"
</p>
<p>
<img src="https://github.com/user-attachments/assets/2dc727b5-3565-4571-b962-21c4b658985c"/>
<img src="https://github.com/user-attachments/assets/bbcc42c2-a07f-4685-8a90-05ee90152d6f"/>
<img src="https://github.com/user-attachments/assets/288b0f0b-b0ea-4876-bef8-05b75d3e74be"/>
</p>

<p>
15. Once that is completed, you must reload IIS. All you have to do is stop the server, wait a moment, then start it again.
</p>
<p>
<img src="https://github.com/user-attachments/assets/d10adb79-0dd3-4f3e-a7c6-20cbf97b7bf2"/>
</p>

<p>
16. Now you will install osTicket. From the "osTicket-Installation-Files" folder, unzip “osTicket-v1.15.8.zip” and copy the "upload" folder into “c:\inetpub\wwwroot”. Once you do that, rename the "upload" folder to "osTicket". After this is done, reload IIS again. 
</p>

<p>
17. After reloading IIS, click on "Sites", go to "Default Web Site", then "osTicket". On the right side, click "Browse *.80".
</p>
<p>
<img src="https://github.com/user-attachments/assets/93e67cd0-2791-4b94-af3a-b1032b5cccc4"/>
</p>

<p>
18. Once you click "Browse *.80", you should see what the image below shows. That means everything is work so far! There are some extensions that need to be enabled.
</p>
<p>
<img src="https://github.com/user-attachments/assets/51776907-d3f1-4aad-9e4a-dd2582722a15"/>
</p>

<p>
19. Return to IIS, click on "Sites", then "Default Web Site", then "osTicket". From there, double click "PHP Manager", then go to "Enable or disable an extension". We will want to enable the following extensions: php_imap.dll, php_intl.dll, php_opcache.dll
</p>
<p>
<img src="https://github.com/user-attachments/assets/7ccbba2f-b008-4210-91bf-feb276d819df"/>
<img src="https://github.com/user-attachments/assets/315eb907-71ea-4bea-becd-c8056c2d07da"/>
<img src="https://github.com/user-attachments/assets/4a18e77c-f4c6-4ce3-897a-286717fd4e73"/>
</p>
