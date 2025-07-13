# Bandit Level 14 ➡️ Level 15

## 🧠 Goal
The password for the next level can be retrieved by submitting the password of the current level to port `30000` on `localhost`.

## 🖥️ Commands Used
```bash
# Step 1: Login using the private SSH key obtained from Level 13
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220

# Step 2: Get the current password (stored in the usual location)
cat /etc/bandit_pass/bandit14
# Output: 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

# Step 3: Submit the password to port 30000 on localhost using netcat (nc)
nc localhost 30000
# Paste the password: 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

# Output: BfMYroe26WYalil77FoDi9qh59eK5xNr
