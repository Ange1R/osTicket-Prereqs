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
- Rewrite Module
- C++ Redistributable
- 

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

Step 9: Extract contents into the PHP folder that was just created on the C Drive
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 24 38 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/a640bd4a-547b-44c2-be0d-42cfe5793a0f">
</p>
<br />

Step 10: Download <a href="https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">C++ Redistributable </a> (VC_redist) which is located in the Google Docs folder
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 30 05 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/fc439932-e99d-470c-afad-4dbf7c1815d5">
</p>
<br />

Step 11: Download <a href="https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">MySQL Server (Typical) </a> which is located in the Google Docs folder
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 33 37 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/387030a8-0b07-412b-90d8-742688d22c21">
</p>
<br />

Step 12: Configure MySQL Server
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 36 47 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/4a635dd8-aab6-49eb-bc50-5e304b523547">
</p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 37 32 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/341bf8f0-c5f3-45d4-9053-4c3dc5a75dd1">
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 38 26 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/59d2b56c-9d90-4712-a877-c1e202a6563b">
</p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 39 08 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/affea85b-d35a-45d1-9231-e36781d6856e">
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 39 57 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/79795bed-8fe2-4440-8bd3-ed7eb500f9e0">
</p>
<br />

Step 13: Run IIS as an administrator - Open the PHP Manager - Register new PHP version - Locate and open php-cgi to register PHP
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 41 48 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/6c300d71-6ea6-4f4f-b5c5-9af236efb297">
</p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 43 59 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/486671bd-70ab-4bf9-ac4e-af0300e47a07">
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 45 50 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/cdb23954-407d-4a96-85a0-41226b9c2c90">
</p>
<img width="1433" alt="Screenshot 2023-07-17 at 12 48 55 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/55e88d52-0dd8-4bd7-a46c-deb29d78af02">
<p>
Navigate back to the VM-osTicket homepage in IIS and click "Restart"
<p>
<img width="1433" alt="Screenshot 2023-07-17 at 1 00 53 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/0317c168-5dda-424f-98dc-4875466db286">









