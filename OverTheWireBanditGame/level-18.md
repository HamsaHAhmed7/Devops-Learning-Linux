# Bandit Level 18 ➡️ Level 19

## 🧠 Goal
The password for the next level is stored in a file named `readme` in the home directory. However, you are **immediately logged out upon login via SSH**, due to a modified `.bashrc` file.

## 🖥️ Commands Used
```bash
# Instead of logging in normally, use SSH to execute a command remotely

# Step 1: List files in the home directory
ssh bandit18@bandit.labs.overthewire.org -p 2220 ls

# Step 2: Read the file directly
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme

# Output:
# IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
