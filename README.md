Azure VM Credential Recovery (easy)

<b>Sign in to Azure</b>
Sign in to the <a href="https://portal.azure.com/auth/login/">Azure portal.</a>

<b>Create a working Virtual Machine</b> 
1. create a Resource Group

<img width="670" height="408" alt="0" src="https://github.com/user-attachments/assets/c2980c19-3656-4fb1-8500-6d0351160baf" />

<img width="904" height="599" alt="1" src="https://github.com/user-attachments/assets/0d34f235-507f-4b70-b4a1-e4749da22c23" />

2. create a Virtual Machine. Under Services, select Virtual machines.

<img width="565" height="274" alt="3vm" src="https://github.com/user-attachments/assets/1dcc535f-a0c9-4853-a9b1-5ffb9a966b08" />

<img width="950" height="589" alt="2" src="https://github.com/user-attachments/assets/6faf3a7b-95d2-459b-81dd-425dba769b95" />

3. connect via RDP using vm's public IP addressto verify it works 
<img width="936" height="676" alt="3" src="https://github.com/user-attachments/assets/e0d16b21-b250-4ef9-bf91-ce1665962d8c" />

4. once logged in open secpol.msc (Local Security Policy). Navigate to: Security Settings → Account Policies → Account Lockout Policy. Set Account lockout threshold to 3 (or any low number). Sign out

   <img width="901" height="588" alt="4" src="https://github.com/user-attachments/assets/c53dee0d-60e1-463c-b398-54e6402e0765" />

   <img width="821" height="585" alt="5" src="https://github.com/user-attachments/assets/f42d1a4f-3305-49cd-96c6-c49986853aaa" />


5. "Break" the vm. Type wrong password 3 times in a row (account locks)

<img width="958" height="687" alt="6" src="https://github.com/user-attachments/assets/b6118183-7a88-4d7e-bf23-b44ecd0a573c" />

<img width="952" height="689" alt="7" src="https://github.com/user-attachments/assets/50071e5a-3daa-400e-a11d-1bf0035c73da" />

6. Troubleshoot & Fix:
	- go to VM > help > Boot diagnostics
	- verify VM screen screenshot shows login screen (normal), then it means VM itself is running and the problem is credentials
	- to reset the password go to VM > help > Reset password
	- set Mode to Reset password
	- enter username (you're resetting password for)
	- enter new password
	- update
4. Verify the fix worked
	- wait 2-3 minutes (optional refresh/restart VM)
	- try RDP again with the new password
	- success! You're logged in
	- the Fix worked!
