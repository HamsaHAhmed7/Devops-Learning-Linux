# Bandit Level 19 ➡️ Level 20

## 🧠 Goal
Use the **setuid** binary located in the home directory to read the password for user `bandit20` from `/etc/bandit_pass/bandit20`. The binary is designed to run commands as `bandit20`.

## 🖥️ Commands Used
```bash
# Step 1: Login
ssh bandit19@bandit.labs.overthewire.org -p 2220
# Password: IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x

# Step 2: View details of the binary
ls -la

# Output (relevant line):
# -rwsr-x--- 1 bandit20 bandit19 7296 May  7  2020 bandit20-do

# Step 3: Read help message from binary
./bandit20-do

# Step 4: Use binary to list bandit passwords (optional)
./bandit20-do ls /etc/bandit_pass

# Step 5: Use binary to read bandit20's password
./bandit20-do cat /etc/bandit_pass/bandit20

# Output:
# GbKksEFF4yrVs6il55v6gwY5aVje5f0j
