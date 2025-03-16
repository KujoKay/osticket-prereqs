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
