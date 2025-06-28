# Bandit Level 5 → Level 6

## Login

ssh bandit5@bandit.labs.overthewire.org -p 2220

## Commands & Output

bandit5@bandit:~$ ls  
inhere

bandit5@bandit:~$ cd inhere/

bandit5@bandit:~/inhere$ ls  
maybehere00 maybehere01 maybehere02 maybehere03 maybehere04  
maybehere05 maybehere06 maybehere07 maybehere08 maybehere09  
maybehere10 maybehere11 maybehere12 maybehere13 maybehere14  
maybehere15 maybehere16 maybehere17 maybehere18 maybehere19

bandit5@bandit:~/inhere$ find . -size 1033c  
./maybehere07/.file2

bandit5@bandit:~/inhere$ cat ./maybehere07/.file2  
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG                                                                                                                                
## Password for Level 5                                                                                                     HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
