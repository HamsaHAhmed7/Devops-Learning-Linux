# Bandit Level 17 ➡️ Level 18

## 🧠 Goal
Compare the two files `passwords.old` and `passwords.new` in the home directory. The password for the next level is the **only line that differs** between the two files — it's a changed line in `passwords.new`.

## 🖥️ Commands Used
```bash
# Step 1: Login with the SSH key from Level 16
ssh -i sshkey17.private bandit17@bandit.labs.overthewire.org -p 2220

# Step 2: Use diff to find the changed line
diff passwords.old passwords.new

# Output:
# 42c42
# < w0Yfolrc5bwjS4qw5mq1nnQi6mF03bii
# ---
# > kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd

# The line that was changed in passwords.new is the new password.
