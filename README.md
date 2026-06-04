<p align="center">
<img width="200" height="200" alt="10021-icon-service-Virtual-Machine" src="https://github.com/user-attachments/assets/191ae456-9eb1-48b7-8044-d02aafde51ab" />

</p>

<h1>Azure Virtual Machine Credential Recovery (easy)</h1>
This lab demonstrates credential recovery within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 11 (win11-25h2-pro)

<h2>High-Level Setup and Troubleshooting Steps</h2>

- Step 1: Create a virtual machine in Azure
- Step 2: "Break" the vm
- Step 3: Troubleshoot & fix
- Step 4: Verify the fix worked

<h2>Setup and Troubleshooting Steps</h2>
<br />

<p>
<b>Step 1: Create a virtual machine in Azure</b>
</p>
<br />

<p>
<img width="670" height="408" alt="0" src="https://github.com/user-attachments/assets/c2980c19-3656-4fb1-8500-6d0351160baf" />
<img width="670" height="408" alt="1" src="https://github.com/user-attachments/assets/0d34f235-507f-4b70-b4a1-e4749da22c23" />
</p>

<br />

<p>
Sign in to the <a href="https://portal.azure.com/auth/login/"><b>Azure portal</b></a> and search/select a <b>Resource Group</b>, a container that will hold all the resources for the project. Select <b>create</b> and fillout the values for <b>Subscription</b>, <b>Resource group name</b>, and <b>Region</b>. Select <b>Review + Create</b>, and <b>Create</b>. It should take a couple of seconds to create a resource group. 
</p>

<br />

<p>
<img width="565" height="274" alt="3vm" src="https://github.com/user-attachments/assets/1dcc535f-a0c9-4853-a9b1-5ffb9a966b08" />
</p>

<p>
<img width="731" height="298" alt="2vm" src="https://github.com/user-attachments/assets/3083a5a6-6d7a-4f33-884d-a7429162bba8" />
</p>
	
<p>
Under Azure services select <b>Virtual machines</b> and select <b>Create > Virtual machine</b>. 
</p>
<br />
	
<p>
<img width="787" height="485" alt="4vm" src="https://github.com/user-attachments/assets/72fd508c-50f4-440a-8717-f9acb02d84f3" />
</p>
<br />

<p> Once the <b>Create a virtual machine</b> page opens, choose <b>Subscription</b> and previously created <b>Resource Group</b>. Fillout the values for <b>Virtual machine name</b> and <b>Image</b> - Windows 11 Pro, version 25H2 - x64 Gen2 under <b>Instance details</b>, the page will fill in the other fields with defaults.
</p>
<br />

<p>
<img width="804" height="249" alt="5vm" src="https://github.com/user-attachments/assets/fc24ffe4-79f3-4030-8082-d1e692c305ef" />
</p>

<p>
Under <b>Administrator account</b>, provide a username and a password.
</p>
<br />

<p>
<img width="515" height="207" alt="6vm" src="https://github.com/user-attachments/assets/f726dfba-352a-4e9a-ab47-83f9a1aba135" />
</p>

<p>
Under <b>Licensing</b> make sure to check the box for "I confirm I have an eligible Windows 10/11 license with multi-tenant hosting rights." Leave the remaining defaults and select the <b>Review + create</b> button at the bottom of the page.
</p>
<br />

<p>
<img width="950" height="589" alt="2" src="https://github.com/user-attachments/assets/6e5f0d4d-6333-4ec1-9206-bc56fad4ffd7" />
</p>

<p>
After validation runs, select the <b>Create</b> button at the bottom of the page. Deployment should take 2-3 minutes.
</p>
<br />

<p>
Create a remote desktop connection to the virtual machine. These directions tell you how to connect to your VM from a Mac computer. On a Windows computer, follow <a href="https://learn.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal"><b>Connect to virtual machine</b></a> steps. 
</p>

<p>
<img width="697" height="275" alt="wapp" src="https://github.com/user-attachments/assets/48e4ecc1-d777-4b6e-8fd6-fb17177bfd06" />
</p>
<br />

<p>
<a href="https://apps.apple.com/us/app/windows-app/id1295203466?mt=12"><b>In App Store for Mac</b></a> download Windows App (previously called Remote Desktop). 
</p>
<br />

<p>
<img width="341" height="295" alt="addpc" src="https://github.com/user-attachments/assets/13e16b4f-3f5e-4c8a-b698-312d28b71252" />
</p>
<br />

<p>
Open the app and select <b>+</b> and <b>Add PC</b>. 
</p>
<br />

<p>
<img width="453" height="518" alt="addpcip" src="https://github.com/user-attachments/assets/b0ad74c8-8705-45c4-bee8-209c2bc314e9" />
</p>
<br />

<p>
Fillout <b>PC name</b> (this is the <b>Primary NIC public IP</b> from the virtual machine), add optional <b>Friendly name</b> and select <b>Add</b>. You are now ready to connect to the virtual machine from your desktop.
</p>
<br />

<p>
<img width="936" height="676" alt="3" src="https://github.com/user-attachments/assets/5ea259f7-3179-4553-9a9f-b5bee17dda68" />
</p>
<br />

<p>
Under <b>Saved Devices</b> double click the PC you just added, enter the user credentials you selected for <b>Administrator account</b> when creating the vm, and select <b>Continue</b>. Your remote desktop will load in a minute or so.
</p>
<br />

<p>
<img width="901" height="588" alt="4" src="https://github.com/user-attachments/assets/33c00eb2-f5cb-46e8-aed7-03c269a1b75e" />
</p>
<br />

<p>
Success! You are now connected to a virtual machine.
</p>
<br />

<p>
<img width="821" height="585" alt="5" src="https://github.com/user-attachments/assets/f42d1a4f-3305-49cd-96c6-c49986853aaa" />
</p>
<br />

<p>
Once logged in open secpol.msc (Local Security Policy). Navigate to: Security Settings → Account Policies → Account Lockout Policy, set Account lockout threshold to 3 (or any low number), and Log off.
</p>
<br />

<p>
<b>Step 2: "Break" the vm</b>
</p>
<br />

<p>
<img width="952" height="689" alt="7" src="https://github.com/user-attachments/assets/50071e5a-3daa-400e-a11d-1bf0035c73da" />
</p>
<br />

<p>
To "break" the vm, type the wrong password 3-4 times in a row, the account should lock.
</p>
<br />

<p>
<b>Step 3: Troubleshoot & fix</b>
</p>
<br />

<p>
<img width="992" height="537" alt="8" src="https://github.com/user-attachments/assets/56a83c97-a4d4-4534-a6b1-9f83f256632c" />
</p>
<br />

<p>
In Azure portal, go to VM > <b>help</b> > <b>Boot diagnostics</b> and verify VM screen screenshot shows login screen (normal), it means VM itself is running and the problem is credentials.
</p>
<br />


<p>
<img width="994" height="598" alt="9" src="https://github.com/user-attachments/assets/cd432a71-dfa4-4cf2-8717-62e4220eb70e" />
</p>
<br />

<p>
To reset the password go to VM > <b>help</b> > <b>Reset password</b>, set Mode to <b>Reset password</b>, enter the <b>Username</b> you're resetting password for, enter a new password and select <b>Update</b>.
</p>
<br />

<p>
<b>Step 4: Verify the fix worked</b>
</p>
<br />





____________________________________________________________________________________________________________________________




7. Verify the fix worked
	<br>- wait 2-3 minutes (optional refresh/restart VM)
	<br>- try RDP again with the new password

<img width="711" height="550" alt="10" src="https://github.com/user-attachments/assets/fa363264-1938-45da-863d-8e7d90d53e7e" />

<br>- success! You're logged in
<img width="900" height="583" alt="11" src="https://github.com/user-attachments/assets/44c497e4-e0f6-41a5-b652-58304219e785" />
<img width="894" height="567" alt="12" src="https://github.com/user-attachments/assets/b34c069c-2ce1-4a0a-9fdd-814e3a391e19" />

<br>- the Fix worked!
