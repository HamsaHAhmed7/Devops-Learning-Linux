# Bandit Level 10 → Level 11

## Login

ssh bandit10@bandit.labs.overthewire.org -p 2220

## Commands Used

bandit10@bandit:~$ ls  
data.txt

bandit10@bandit:~$ ls -la  
total 24  
drwxr-xr-x  2 root     root     4096 Apr 10 14:22 .  
drwxr-xr-x 70 root     root     4096 Apr 10 14:24 ..  
-rw-r--r--  1 root     root      220 Mar 31  2024 .bash_logout  
-rw-r--r--  1 root     root     3771 Mar 31  2024 .bashrc  
-rw-r-----  1 bandit11 bandit10   69 Apr 10 14:22 data.txt  
-rw-r--r--  1 root     root      807 Mar 31  2024 .profile

bandit10@bandit:~$ cat data.txt  
VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==

bandit10@bandit:~$ base64 -d data.txt  
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

## Password for Level 11

dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
