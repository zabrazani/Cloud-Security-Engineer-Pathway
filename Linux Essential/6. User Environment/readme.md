1. User Management
   I successfully created and later attempted to remove a user account.

User Creation:

Created a new user named kceefrank with a full name of "Kcee Franklin," a home directory (-m), and the /bin/bash shell.

Set the password for the new user kceefrank.

Verified the user's existence in the /etc/passwd and /etc/group files.

User Deletion:

Attempted to delete the user kceefrank and their home directory (userdel -r kceefrank).

Confirmed the successful deletion of the user account by observing the blank output from grep kceefrank /etc/passwd.

Confirmed the successful deletion of the user's home directory by receiving the output: ls: cannot access '/home/kceefrank': No such file or directory.

2. SSH Server Management
   I successfully started, used, and then securely disabled the SSH service.

Service Startup:

Checked the status of the ssh.service and found it was inactive (dead).

Started the SSH service (sudo systemctl start ssh).

Confirmed the service was running by checking the status again, which showed Active: active (running).

SSH Connection:

Successfully connected to the local machine as the new user (ssh kceefrank@localhost) after starting the service.

Accepted the host key and logged in to the new user's account.

Closed the connection (Connection to localhost closed.).

Service Shutdown (Security Best Practice):

Stopped the SSH service (sudo systemctl stop ssh).

Disabled the SSH service (sudo systemctl disable ssh), preventing it from starting automatically on the next system boot.

3. File and Directory Exploration
    I used basic file system commands to check the state of the system and user files.

Explored Directories:

Ran ls -l /etc/skel to check the contents of the skeleton directory used for new user home directories.

Used ls and ls -ld /home/kceefrank (after user deletion) to confirm the user's home directory was gone.
Finally Some of Beau Screenshots
Thanks....
