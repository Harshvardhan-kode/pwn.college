# Linux Luminarium

## Module 3:comprehending commands  

### Challenge: linking files

**Commands Used:**
```bash
hacker@commands~linking-files:~$ ls
 COLLEGE   Desktop   PWN   catflag   not-the-flag   tmp  '~'
hacker@commands~linking-files:~$ ln -s /flag /challenge/catflag
ln: failed to create symbolic link '/challenge/catflag': File exists
hacker@commands~linking-files:~$ rm /home/hacker/not-the-flag
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /flag
bash: /flag: Permission denied
hacker@commands~linking-files:~$ cat /flag
cat: /flag: Permission denied
hacker@commands~linking-files:~$ file /home/hacker/not-the-flag
/home/hacker/not-the-flag: symbolic link to /flag
hacker@commands~linking-files:~$ /challenge/catflag
```
**Output:**
```bash
About to read out the /home/hacker/not-the-flag file!
pwn.college{AxItR7hMqYMY6H1nNeD7w57jQ8g.QX5ETN1wCM3UzNzEzW}
```
