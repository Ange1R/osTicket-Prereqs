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
- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- C++ Redistributable
- MySQL Server
- osTicket
- HiediSQL

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
Navigate back to the VM-osTicket homepage in IIS and click "Restart" located on the right side menu 
</p>
<img width="1433" alt="Screenshot 2023-07-17 at 1 00 53 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/0317c168-5dda-424f-98dc-4875466db286">
<p>
<br />
  
Step 14: Download <a href="https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">osTicket </a> which is located in the Google Docs folder then extract the "upload" folder (located in the osTicket zip file) into the Windows (C:) > inetpub > wwwroot file path 
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 10 22 58 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/b2ea4098-4b52-4894-b9a5-df54357dfbd2">
</p>
<img width="1433" alt=Screenshot 2023-07-18 at 10 26 37 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/c7328dde-01e5-425d-95de-62be51681266">
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 10 30 50 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/c03f0b52-bf94-4447-ac2c-f307494c51e9">
</p>
<img width="1433" alt=Screenshot 2023-07-18 at 10 32 29 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/e6d95b3c-b97e-4b92-8d63-309c0a73158d">
<p>
Rename the "upload" folder to "osTicket"
</p>
<img width="1433" alt=Screenshot 2023-07-18 at 10 35 25 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/815bbcd8-c666-42a9-b806-945dfb04f653">
<p>
Navigate back to the VM-osTicket homepage in IIS and click "Restart" located on the right side menu
</p>
<img width="1433" alt=Screenshot 2023-07-18 at 10 37 22 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/1c511391-d38b-4789-bde8-fee190044f7e">
<p>
Navigate to osTicket Home in IIS by hitting the down arrows on "Sites" and "Default Web Site" on the left side menu
</p>
<img width="1433" alt=Screenshot 2023-07-18 at 10 40 42 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/6da95bbe-078a-47e1-b050-1a5d076c9da9">
<p>
Once there, select "Browse *:80(http)" which is located on the right side menu which will open osTicket Installer on your web browser
</p>
<img width="1433" alt=Screenshot 2023-07-18 at 10 42 51 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/c1158e85-de85-4dc2-b8e5-5eb1e53fa1a2">
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 10 45 35 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/c1a60224-53bf-4a9c-9dbf-ea655c82ebd1">
</p>
<br />

Step 15: Navigate back to osTicket Home in IIS - select PHP Manager - select "Enable or disable an extension" - and enable php_imap.dll, php_intl.dll, and php_opcache.dll
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 10 49 07 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/01b32106-39df-4853-977c-b7867d50ff6f">
</p>
<img width="1433" alt=Screenshot 2023-07-18 at 10 50 50 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/61a64daf-caf8-405a-b944-8f9e16f38768">
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 10 55 57 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/41e6c988-41aa-4335-98b3-2962cf1b0f0c">
</p>
Refresh the browser with osTicket and the extensions that were enabled should have a green check mark now
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 10 58 53 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/547fdded-9197-4e8a-8127-759074be36ce">
</p>
<br />

Step 16: Locate the file "ost-sampleconfig.php" which is in the Windows(C:)>inetpub>wwwroot>osTicket>include file path and rename it to "ost-config.php"
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 03 57 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/f2d1dfb3-6321-4f44-858a-ce4ad7bd85ab">
</p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 04 09 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/e0cc2161-da09-41f6-9c82-3ea74629b6c9">
<p>
<br />

Step 17: Open up the properties for ost-config.php - choose the Security tab - open advanced settings
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 09 30 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/2dae2501-2691-4cab-96ce-294bab13d5f2">
</p>
Disable inheritance once in the advanced settings section (remove all inherited permissions)
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 11 21 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/b4c5371b-906e-41aa-9c30-c17201b5df21">
</p>
Click "Add" to add permissions
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 12 57 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/dccd98ff-dae1-4ba8-b34b-6671708cf55a">
</p>
Select a principal - Enter "Everyone" in the space provided - Check names and click OK
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 17 19 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/35801aed-7a09-470f-9acf-d78bf0b9ee00">
</p>
Check all boxes for permissions and click OK
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 18 16 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/346eb80c-fcc7-46b2-81c6-ec64aec14f7b">
</p>
<br />

Step 18: Go back to the browser with osTicket, click continue, and fill in the information in the system settings and admin user sections
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 33 20 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/3ad062c8-9cd6-43b6-a6d6-c93d3fa24f94">
</p>
<br />

Step 19: Download/Install <a href="https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">HeidiSQL </a> which is located in the Google Docs folder
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 37 42 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/01d40584-4774-42b7-9f47-f39d1d20206c">
</p>
Open HiediSQL - select "New" in the left hand corner - enter the password that was created when registering MySQL Server (keep in mind the username is root) - select Open
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 43 11 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/5c4f9719-b06e-4449-85cb-b298d37e8939">
</p>
Create a new database named "osTicket"
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 46 02 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/31e65138-b1f1-45d0-904e-f99429b3b396">
</p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 46 58 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/6a45926d-0e72-4025-928b-625e54b83401">
<p>
<br />

Step 20: Go back to the browser with osTicket and fill in the Database Settings section with the database just created and username and password used for MySQL Server - Install
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 52 20 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/1dc833e0-d678-4235-82e0-5f68067c0cda">
</p>
<img width="1433" alt=Screenshot 2023-07-18 at 11 53 41 AM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/87db2807-b88b-4642-9c5b-3ef3c5f09e36">
<p>
CONGRATULATIONS 🎉, hopefully it installed with no errors!
</p>
<br />

CLEAN-UP

Step 1: Delete C:\inetpub\wwwroot\osTicket\setup
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 12 01 55 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/6b7eda1f-45fd-455a-8225-3121659f400f">
</p>
<br />

Step 2: Navigate back to ost-config.php (located in Windows(C:)>inetpub>wwwroot>osTicket>include file path) - Open properties - Choose the Security tab - Advanced - Edit - Uncheck all boxes excluding the Read options - Click Apply and OK
<p>
<img width="1433" alt=Screenshot 2023-07-18 at 12 05 45 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/122eb357-4ca1-4bbb-ab4d-b5568a07547d">
</p>
<img width="1433" alt=Screenshot 2023-07-18 at 12 08 44 PM" src="https://github.com/areyes302/osticket-prereqs/assets/139584521/388b76f4-34b0-4ff7-885c-d9c8b061ed92">
<p>
<br />

You're all done! ✔️  osTicket is now installed
