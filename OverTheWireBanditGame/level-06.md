# Bandit Level 6 → Level 7

## Login

ssh bandit6@bandit.labs.overthewire.org -p 2220

## Commands Used

bandit6@bandit:~$ ls  
bandit6@bandit:~$ ls -la  
total 20  
drwxr-xr-x  2 root root 4096 Apr 10 14:22 .  
drwxr-xr-x 70 root root 4096 Apr 10 14:24 ..  
-rw-r--r--  1 root root  220 Mar 31  2024 .bash_logout  
-rw-r--r--  1 root root 3771 Mar 31  2024 .bashrc  
-rw-r--r--  1 root root  807 Mar 31  2024 .profile

bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c -type f 2>/dev/null  
/var/lib/dpkg/info/bandit7.password

bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password  
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

## Password for Level 7

morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

