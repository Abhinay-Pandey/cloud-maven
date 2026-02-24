🐧 Linux Lab Manual

This repository contains basic Linux administration practice labs covering user management, file permissions, process control, and text editing using Vim.

📌 Lab 1 – User Management
🔹 1. Create a User

Create a new user account:

sudo useradd alice
sudo passwd alice

Set the password when prompted.

🔹 2. Switch User

Switch to the newly created user:

su - alice

Verify current user:

whoami
🔹 3. Verify Home Directory

Check the home directory of the user:

pwd

Expected output:

/home/alice
📌 Lab 2 – File Permissions
🔹 1. Create a File
touch myfile.txt
🔹 2. Modify Permissions
chmod 640 myfile.txt

Verify permissions:

ls -l myfile.txt

Permission meaning:

Owner → Read & Write

Group → Read only

Others → No access

🔹 3. Change Ownership
sudo chown bob myfile.txt
🔹 4. Test Access

Switch to another user:

su - bob
cat myfile.txt

You may see:

Permission denied
📌 Lab 3 – Process Control
🔹 1. Run Background Process
sleep 300 &
🔹 2. Identify Process ID (PID)
ps aux | grep sleep

Note the PID number.

🔹 3. Kill Process
kill <PID>

Example:

kill 12345
📌 Lab 4 – Editing with Vim
🔹 1. Create File Using Vim
vim notes.txt
🔹 2. Insert Content

Press:

i

Add content:

Meeting Notes
* Discuss project timeline
* Review task assignments

