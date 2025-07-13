# Bandit Level 12 → Level 13

## Login

ssh bandit12@bandit.labs.overthewire.org -p 2220

## Commands Used

bandit12@bandit:~$ cd /tmp  
bandit12@bandit:/tmp$ mktemp -d  
/tmp/tmp.9605a8jyaa  

bandit12@bandit:/tmp$ cd /tmp/tmp.9605a8jyaa  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ cp ~/data.txt .  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ mv data.txt hexdump_data  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ xxd -r hexdump_data compressed_data  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ mv compressed_data compressed_data.gz  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ gzip -d compressed_data.gz  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ mv compressed_data compressed_data.bz2  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ bzip2 -d compressed_data.bz2  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ mv compressed_data compressed_data.gz  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ gzip -d compressed_data.gz  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ mv compressed_data compressed_data.tar  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ tar -xf compressed_data.tar  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ tar -xf data5.bin  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ bzip2 -d data6.bin  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ tar -xf data6.bin.out  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ mv data8.bin data8.gz  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ gzip -d data8.gz  
bandit12@bandit:/tmp/tmp.9605a8jyaa$ cat data8  
The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

## Password for Level 13

FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
