# Admin File Sharing
## Description
I learned How to share files with multiple users including how to deny and allow access.
## Objectives
- Configure shared folders
- Manage access to shared folders using Windows share and NTFS permissions
## Skills Learned
- File paths (C:\)
- File sharing
- Share & NTFS permissions
- Permission inheritance
- Explicit Allow vs Deny
- Effective permissions
- Password resets
- User context testing
- Basic access troubleshooting
## Steps
1. Created two test users on Windows 11 Home using Command Prompt. (command "net user 'name' 'password' /add" used to create new PC user).

<img width="1920" height="1080" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/b08622b9-35da-4143-b82a-b0ce213ada5c" />

2. Created a New folder and named it "company files" in the main drive. Configured its setting by changing shared permissions to full control and NTFS permissions. Under security properties Bob was granted Modify permission, and TestUser was denied read & execute permissions.

<img width="1920" height="1080" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/e07efac0-151a-4b7c-8f15-867fed2583d1" />

4. When attempted to test user access through command prompt, I experienced errors. I tried various Runas attempts in cmd and had multiple fails. After resetting the password again using runas on cmd, I discovered I was entering the incorrect password into the account.

5. I logged into local user Bob, I was able to open the test folder created named "company files" and read the test file as well as edit it. I also verified Bob was able to create new files in the shared folder.

<img width="1920" height="1080" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/b7141187-5160-4c04-b823-1b222cf5b69d" />

6. I then logged in as Testuser and attempted to also open the folder and verified permissions was denied.

<img width="1920" height="1080" alt="Screenshot (24)" src="https://github.com/user-attachments/assets/4c9b4579-34b7-4f1d-a724-1b2c0aa0d978" />

## Comments/ notes
  On step 1, I learned the difference between all the users shown on the command line including user accounts, administrator accounts, and built-in Windows system accounts as well as the importance of never tampering with the Windows Administrator, Windows Defender Application Guard Utility Account, and Default Account. 
  
  I learned the permissions rule of: The most restrictive permissions wins between Windows Share and NTFS stating that the most restrictive setting between the two will rule over the other one that allows more access. Typically, Shared is set to full control and the files are managed through NTFS because NTFS is more specific making management of files simpler. 
