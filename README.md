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
- Installation Files

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
5. Now that you have accessed your virtual machine, you will need to   
</p>
<p>
<img src="https://github.com/user-attachments/assets/50f2852d-bec0-44c2-924f-97dc139cc7c6"/>
<img src="https://github.com/user-attachments/assets/0a0926fb-9216-4df4-bd5d-45e1040df43a"/>
</p>
