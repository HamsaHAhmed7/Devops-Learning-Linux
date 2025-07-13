# Bandit Level 11 → Level 12

## Login

ssh bandit11@bandit.labs.overthewire.org -p 2220

## Commands Used

bandit11@bandit:~$ ls  
data.txt

bandit11@bandit:~$ cat data.txt  
Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4

bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'  
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

## Password for Level 12

7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
