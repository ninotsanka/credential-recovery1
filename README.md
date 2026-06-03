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
Under Azure services select <b>Virtual machines</b> and select <b>Create > Virtual machine</b>. 

<img width="731" height="298" alt="2vm" src="https://github.com/user-attachments/assets/3083a5a6-6d7a-4f33-884d-a7429162bba8" />

</p> Once the <b>Create a virtual machine</b> page opens fillout values for <b>Virtual machine name</b> and <b>Image</b> - Windows 11 Pro, version 25H2 - x64 Gen2 under <b>Instance details</b>
<br />

<p>

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="731" height="298" alt="2vm" src="https://github.com/user-attachments/assets/3083a5a6-6d7a-4f33-884d-a7429162bba8" />

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="731" height="298" alt="2vm" src="https://github.com/user-attachments/assets/3083a5a6-6d7a-4f33-884d-a7429162bba8" />

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="731" height="298" alt="2vm" src="https://github.com/user-attachments/assets/3083a5a6-6d7a-4f33-884d-a7429162bba8" />

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

____________________________________________________________________________________________________________________________

2. create a Virtual Machine. Under Services, select Virtual machines.

<img width="565" height="274" alt="3vm" src="https://github.com/user-attachments/assets/1dcc535f-a0c9-4853-a9b1-5ffb9a966b08" />

<img width="950" height="589" alt="2" src="https://github.com/user-attachments/assets/6faf3a7b-95d2-459b-81dd-425dba769b95" />

3. connect via RDP using vm's public IP address to verify it works 
<img width="936" height="676" alt="3" src="https://github.com/user-attachments/assets/e0d16b21-b250-4ef9-bf91-ce1665962d8c" />

4. once logged in open secpol.msc (Local Security Policy). <br>-Navigate to: Security Settings → Account Policies → Account Lockout Policy. <br>-Set Account lockout threshold to 3 (or any low number). <br>-Sign out

   <img width="901" height="588" alt="4" src="https://github.com/user-attachments/assets/c53dee0d-60e1-463c-b398-54e6402e0765" />

   <img width="821" height="585" alt="5" src="https://github.com/user-attachments/assets/f42d1a4f-3305-49cd-96c6-c49986853aaa" />


5. "Break" the vm. Type wrong password 3 times in a row (account locks)

<img width="958" height="687" alt="6" src="https://github.com/user-attachments/assets/b6118183-7a88-4d7e-bf23-b44ecd0a573c" />

<img width="952" height="689" alt="7" src="https://github.com/user-attachments/assets/50071e5a-3daa-400e-a11d-1bf0035c73da" />

6. Troubleshoot & Fix:
<br>-go to VM > help > Boot diagnostics
<br>-verify VM screen screenshot shows login screen (normal), it means VM itself is running and the problem is credentials

<img width="992" height="537" alt="8" src="https://github.com/user-attachments/assets/286736d4-f9f7-4eb8-ab4a-b495ecad9351" />

<br>To reset the password <br>-go to VM > help > Reset password <br> -set Mode to Reset password <br>-enter username (you're resetting password for) <br>-enter new password <br>-update

<img width="994" height="598" alt="9" src="https://github.com/user-attachments/assets/cd432a71-dfa4-4cf2-8717-62e4220eb70e" />

7. Verify the fix worked
	<br>- wait 2-3 minutes (optional refresh/restart VM)
	<br>- try RDP again with the new password

<img width="711" height="550" alt="10" src="https://github.com/user-attachments/assets/fa363264-1938-45da-863d-8e7d90d53e7e" />

<br>- success! You're logged in
<img width="900" height="583" alt="11" src="https://github.com/user-attachments/assets/44c497e4-e0f6-41a5-b652-58304219e785" />
<img width="894" height="567" alt="12" src="https://github.com/user-attachments/assets/b34c069c-2ce1-4a0a-9fdd-814e3a391e19" />

<br>- the Fix worked!
