# Bandit Level 15 ➡️ Level 16

## 🧠 Goal
The password for the next level can be retrieved by submitting the current level's password to port `30001` on `localhost`, using **SSL encryption**.

## 🖥️ Commands Used
```bash
# Step 1: Login to Bandit 15
ssh bandit15@bandit.labs.overthewire.org -p 2220
# Password: BfMYroe26WYalil77FoDi9qh59eK5xNr

# Step 2: Connect to the SSL-enabled port using OpenSSL
openssl s_client -connect localhost:30001

# Step 3: Paste the current password when prompted or after connection
BfMYroe26WYalil77FoDi9qh59eK5xNr

# Output: cluFn7wTiGryunymYOu4RcffSxQluehd
