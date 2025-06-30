# Bandit Level 4 → Level 5

## Login

ssh bandit4@bandit.labs.overthewire.org -p 2220

## Commands Used

bandit4@bandit:~$ cd inhere/

bandit4@bandit:~/inhere$ ls  
-file00  -file02  -file04  -file06  -file08  
-file01  -file03  -file05  -file07  -file09

bandit4@bandit:~/inhere$ file ./*  
./-file00: PGP Secret Sub-key -  
./-file01: data  
./-file02: data  
./-file03: data  
./-file04: data  
./-file05: data  
./-file06: data  
./-file07: ASCII text  
./-file08: data  
./-file09: data

bandit4@bandit:~/inhere$ cat ./-file07  
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

## Password for Level 5

4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
