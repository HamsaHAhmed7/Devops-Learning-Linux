# Bandit Level 16 ➡️ Level 17

## 🧠 Goal
The credentials for the next level can be retrieved by submitting the password of the current level to **a port between 31000 and 32000 on localhost**. You must first identify which ports are open, which ones use SSL, and which one returns the next level's credentials.

## 🖥️ Commands Used
```bash
# Step 1: Login to Bandit 16
ssh bandit16@bandit.labs.overthewire.org -p 2220
# Password: cluFn7wTiGryunymYOu4RcffSxQluehd

# Step 2: Scan ports between 31000 and 32000 using nmap
nmap -sV localhost -p 31000-32000

# Output (truncated):
# PORT      STATE SERVICE     VERSION
# 31046/tcp open  echo
# 31518/tcp open  ssl/echo
# 31691/tcp open  echo
# 31790/tcp open  ssl/unknown
# 31960/tcp open  echo

# Step 3: Connect to the promising SSL port (31790) using OpenSSL
openssl s_client -connect localhost:31790

# Step 4: Submit current password when connected
cluFn7wTiGryunymYOu4RcffSxQluehd

# Output: Private SSH key for Bandit 17
