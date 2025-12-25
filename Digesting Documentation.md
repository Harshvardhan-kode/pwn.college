# Linux Luminarium

## Module 4: Digesting Documentation 

### Challenge: reading manually

**Commands Used:**
```bash
man challenge

/challenge/challenge --gwsifn 055
```
**Output:**
```bash
Correct usage! Your flag: pwn.college{gwOWsiZ0fnpcdbppPUwn55BU9He.QX0EDO0wCM3UzNzEzW}
```

# Linux Luminarium

## Module 4: Digesting Documentation 

### Challenge: searching manuals

**Commands Used:**
```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --ictx
```
**Output:**
```bash
Initializing...
Correct usage! Your flag: pwn.college{YWEPk5pZjg-HiQsXhFe7ulOLXxn.QX1EDO0wCM3UzNzEzW}
```

# Linux Luminarium

## Module 4: Digesting Documentation 

### Challenge: searching for manuals

**Commands Used:**
```bash
hacker@man~searching-for-manuals:~$ /challenge/challenge --wtgcqd 902
hacker@man~searching-for-manuals:~$ man -k challenge
wtgcqdatbm (1)       - print the flag!
```
**Output:**
```bash
Correct usage! Your flag: pwn.college{wWGtD9gQcALqMBRdXatbTRM0Wmf.QX2EDO0wCM3UzNzEzW}
```

# Linux Luminarium

## Module 4: Digesting Documentation 

### Challenge: helping programs

**Commands Used:**
```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge --print-value
The secret value is: 776
hacker@man~helpful-programs:~$ /challenge/challenge -g 776
```
**Output:**
```bash
Correct usage! Your flag: pwn.college{Er7Z7SvraPV6VBUZNE95oRySVfL.QX3IDO0wCM3UzNzEzW}
```

# Linux Luminarium

## Module 4: Digesting Documentation 

### Challenge: help for builtins

**Commands Used:**
```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "QF30RtIi".
hacker@man~help-for-builtins:~$ challenge --secret QF30RtIi
```
**Output:**
```bash
Correct! Here is your flag!
pwn.college{QF30RtIijGAVIDYAdBerzMb4GTo.QX0ETO0wCM3UzNzEzW}
```






