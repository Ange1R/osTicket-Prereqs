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
- MacOS

<h2>List of Prerequisites</h2>

- Microsoft Azure
- Microsoft Remote Desktop Application (macOS users)
- PHP Manager
- Item 4
- Item 5

<h2>Installation Steps</h2>

Step 1: Within Azure, create the resource group and virtual machine that will be used to run the ticketing system
<p>
<img width="1239" alt="Screenshot 2023-07-17 at 10 06 20 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/9125b727-e411-4a0f-8152-909f096bf84b">
</p>
<img width="1239" alt="Screenshot 2023-07-17 at 10 12 30 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/f4acd0ab-da37-4828-a40e-ad4b1df9c9c3">
<p>
<img width="1239" alt="Screenshot 2023-07-17 at 10 16 31 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/7043c4f4-1a59-459d-9414-c48a7d7f2e61">
</p> 
<br />

Step 2: Copy the public IP address that was created for VM-osTicket and start a session using the Microsoft Remote Desktop application and the credentials that were used when creating the virtual machine
<p>
<img width= "1239" alt="Screenshot 2023-07-17 at 10 50 05 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/4d79f282-ed42-40e2-9d42-ce10d59ba5c9">
</p>
<img width="1434" alt="Screenshot 2023-07-17 at 10 55 24 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/944a3596-000c-4b98-8787-15fdc7a25217">
</p>
<br />

Step 3: Once your VM is up and running, navigate to Control Panel > Programs from the start menu and choose the option "Turn Windows features on or off" listed under Programs and Features. We will be installing/enabling Internet Information Services (IIS) in Windows with CGI which will allow us to run up osTicket through a web server
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 11 15 53 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/11e9dc80-3742-4dbf-b875-20c5ea91f9c5">
</p>
<br />

Step 4: Scroll down to locate "Internet Information Services", match all of the checked boxes in the screenshots below, and click OK to install IIS
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 11 27 20 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/c0d665ed-714b-4f5c-a5df-3a9ba5b3480e">
</p>
<img width="1433" alt="Screenshot 2023-07-17 at 11 30 24 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/1c46d7a4-ce08-4d03-9706-716387741cc7">
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 11 31 54 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/7488fb7a-237d-425e-8ccc-241d1d327845">
</p>
<br />

Step 5: Download <a href="https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">PHP Manager </a> for IIS which is located in the Google Docs folder
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 09 40 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/04e89e41-6e2b-4d3d-aa0b-18c98ddf0b6d">
</p>
<br />

Step 6: Download <a href="https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">Rewrite Module </a> which is located in the Google Docs folder
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 08 06 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/90aa4a65-aacc-4dda-aa72-06e33c5096b2">
</p>
<br />

Step 7: On the C Drive create a folder named PHP
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 14 24 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/7f26b6ce-1c24-4166-910d-38cb1865dfb6">
</p>
<br />

Step 8: Download <a href="https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">PHP 7.3.8 </a> which is located in the Google Docs folder (be patient when downloading, download will appear in Downloads folder when ready)
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 22 44 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/2819a2f2-53ef-4688-ad36-bf6e1e71265f">
</p>
<br />

Step 9: Extract contents into the PHP folder that was just created in the C Drive
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 24 38 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/a640bd4a-547b-44c2-be0d-42cfe5793a0f">
</p>
<br />

Step 10: 

