# Bandit Level 13 ➡️ Level 14

## 🧠 Goal
The password for the next level is stored in `/etc/bandit_pass/bandit14` and can only be read by user `bandit14`. You are not given the password directly but instead a private SSH key to access the next level.

## 🖥️ Commands Used
```bash
# Step 1: Login to Bandit 13
ssh bandit13@bandit.labs.overthewire.org -p 2220
# Password: 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

# Step 2: Check home directory
ls
# Output: sshkey.private

# Step 3: Exit and use SCP to download the private key
exit
scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .

# Step 4: Fix file permissions
chmod 700 sshkey.private

# Step 5: Login to Bandit 14 using the private key
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
