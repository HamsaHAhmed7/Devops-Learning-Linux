# Bandit Level 3 → Level 4

## Login

ssh bandit3@bandit.labs.overthewire.org -p 2220

## Commands Used

bandit3@bandit:~$ ls  
inhere

bandit3@bandit:~$ cd inhere/

bandit3@bandit:~/inhere$ ls

bandit3@bandit:~/inhere$ ls -a  
.  ..  ...Hiding-From-You

bandit3@bandit:~/inhere$ cat ...Hiding-From-You  
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

## Password for Level 4

2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
 # Bandit Level 2 → Level 3

## Login

ssh bandit2@bandit.labs.overthewire.org -p 2220

## Commands Used

bandit2@bandit:~$ ls  
spaces in this filename

bandit2@bandit:~$ ls -l  
total 4  
-rw-r----- 1 bandit3 bandit2 33 Apr 10 14:23 spaces in this filename

bandit2@bandit:~$ cat spa[TAB]  
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

## Password for Level 3

MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
