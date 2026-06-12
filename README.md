# Admin File Sharing
## Description
I learned How to share files with multiple users including how to deny and allow access.
## Objectives
- Know how to create shared folders
- Know how to deny and grant access to folders to users
## Skills Learned
- File paths (C:\)
- Shared folders
- Share permissions
- NTFS permissions
- Permission inheritance
- Explicit Allow vs Deny
- Effective permissions
- Password resets
- User context testing
- Basic access troubleshooting
## Steps
1. Create two test users on Windows 11 Home using Command Prompt. (command "net user 'name' 'password' /add" used to create new PC user).

<img width="1920" height="1080" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/b08622b9-35da-4143-b82a-b0ce213ada5c" />

2. Created a New folder and named it "company files" in the main drive. Configured its setting by changing shared permissions to full control and NTFS permissions. Under security properties Bob was granted Modify permission, and TestUser was denied read & execute permissions.

3. When attempted to test user access through command prompt, I experienced errors. After resetting the password again using runas on cmd, I discovered I was entering the incorrect password into the account.

4. Logged into local user Bob, I was able to open the test folder named "company files" and read the test file as well as edit it. I also verified Bob was able to create new files in the shared folder.

5. 
## Comments/ notes
On step 1, I learned the difference between all the users shown on the command line including user accounts, administrator accounts, and built-in Windows system accounts as well as the importance of never tampering with the Windows Administrator, Windows Defender Application Guard Utility Account, and Default Account. 
