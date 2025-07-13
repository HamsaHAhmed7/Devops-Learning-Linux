# Bandit Level 20 ➡️ Level 21

## 🧠 Goal
Use the setuid binary `suconnect` to retrieve the password for the next level. This binary connects to `localhost` on a specified port, waits for a password input, and if it matches the current level's password (`bandit20`), it sends back the next level’s password.

## 🖥️ Commands Used
```bash
# Step 1: Login to Bandit 20
ssh bandit20@bandit.labs.overthewire.org -p 2220
# Password: GbKksEFF4yrVs6il55v6gwY5aVje5f0j

# Step 2: Create a netcat server that sends the current password when contacted
echo -n 'GbKksEFF4yrVs6il55v6gwY5aVje5f0j' | nc -l -p 1234 &

# Step 3: Run the setuid binary and point it to the port we're listening on
./suconnect 1234

# Output:
# Read: GbKksEFF4yrVs6il55v6gwY5aVje5f0j
# Password matches, sending next password
# gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
