# Linux Luminarium

## Module 4: File Globbing

### Challenge: matching with *

**Commands Used:**
```bash
hacker@globbing~matching-with-:~$ cd /c*e
hacker@globbing~matching-with-:/challenge$ /challenge/run
```
**Output:**
```bash
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{w-ZZQY-CqrvoHjew3xbS8D0mgwt.QXxIDO0wCM3UzNzEzW}
```

## Module 4: File Globbing

### Challenge: matching with ?

**Commands Used:**
```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
```
**Output:**
```bash
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{096cuCHfRXChJoXHCHhcpIZDrCL.QXyIDO0wCM3UzNzEzW}
```

## Module 4: File Globbing

### Challenge: matching with []

**Commands Used:**
```bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[abhs]
```
**Output:**
```bash
You got it! Here is your flag!
pwn.college{sIbpnL41ASxtNT4BOMW_N7yD_vv.QXzIDO0wCM3UzNzEzW}
```

## Module 4: File Globbing

### Challenge: matching psths with []

**Commands Used:**
```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
```
**Output:**
```bash
You got it! Here is your flag!
pwn.college{0urSwt2OUxL751innRc506QTfHF.QX0IDO0wCM3UzNzEzW}
```

## Module 4: File Globbing

### Challenge: multiple globs

**Commands Used:**
```bash
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
```
**Output:**
```bash
You got it! Here is your flag!
pwn.college{8SBbOFqFzDGQ-3b-XwZWPpOh8ZG.0lM3kjNxwCM3UzNzEzW}
```

## Module 4: File Globbing

### Challenge: mixing globs

**Commands Used:**
```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
```
**Output:**
```bash
You got it! Here is your flag!
pwn.college{0DQBH4jg_Q80nRClwz-jUEdUl4n.QX1IDO0wCM3UzNzEzW}
```

## Module 4: File Globbing

### Challenge: exclusionary globbing

**Commands Used:**
```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
```
**Output:**
```bash
You got it! Here is your flag!
pwn.college{gO1JfsRlmTzMk538vAavYUQhrsn.QX2IDO0wCM3UzNzEzW}
```

## Module 4: File Globbing

### Challenge: tab completion

**Commands Used:**
```bash
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​ 
```
**Output:**
```bash
pwn.college{A-9eEnEGA_5R23-R1IBdo0hwBaQ.0FN0EzNxwCM3UzNzEzW}
```

## Module 4: File Globbing

### Challenge: multiple options for tab completion

**Commands Used:**
```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cd /challenge/files
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ /challenge/files/pwn
pwn                    pwn-the-planet         pwncollege-flamingo    pwncollege-hacking     
pwn-college            pwncollege-family      pwncollege-flyswatter  
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-fla
pwncollege-flag      pwncollege-flamingo  
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-flag
```
**Output:**
```bash
pwn.college{AlP1gFDpNIblGfobE_aMOn8XTyy.0lN0EzNxwCM3UzNzEzW}
```

## Module 4: File Globbing

### Challenge: tab completion on commands

**Commands Used:**
```bash
hacker@globbing~tab-completion-on-commands:~$ pwncollege-2317 
```
**Output:**
```bash
Correct! Here is your flag:
pwn.college{cqNwEm4szTuBR_MPWTQ0hiCybu4.0VN0EzNxwCM3UzNzEzW}
```
