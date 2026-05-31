Azure VM Credential Recovery (easy)

1. Create a working VM 
	- create a Resource Group
	- create a Virtual Machine
	- connect via RDP to verify it works using vm's public IP address
	- Log into the VM
	- Open secpol.msc (Local Security Policy)
	- Navigate to: Security Settings → Account Policies → Account Lockout Policy
	- Set Account lockout threshold to 3 (or any low number)
	- Sign out
2. "Break" the vm
	- Easy: Type wrong password 3 times in a row (account locks) 
3. Troubleshoot & Fix
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
