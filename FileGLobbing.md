# File Globbing 

## Matching with *
### Learnings: Learnt about matching with *
```
cd /c*
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{opgJNQpZST-ZshnzklSX5FlS0Nb.dFjM4QDL1kTN0czW}
```
References:None used.






## Matching with ?
### Learnings:Learnt about ? and its character matching
```
 cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{Q067K0bEG3RpG6DBPw335qbXXcy.dJjM4QDL1kTN0czW}
```
Used the problem statement to reach the flag.
References:None used.
## Matching with []
### Learnings: Learnt about selective matching of [] command
```
 cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run /challenge/files/file_[bash]
Your expansion did not expand to the requested files (file_a, file_b, file_h,
and file_s). Instead, it expanded to:
/challenge/files/file_a /challenge/files/file_b /challenge/files/file_h /challenge/files/file_s
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{Qvp0QVMdlBn2FZkaF86LpeweeVS.dNjM4QDL1kTN0czW}
```
References:None used.

## Matching paths with []


```
 cd /challenge/files
hacker@globbing~matching-paths-with-:/challenge/files$ /challenge/run files_[bash]
Error: please run with a working directory of /home/hacker!
hacker@globbing~matching-paths-with-:/challenge/files$ /challenge/run/file_[bash]
ssh-entrypoint: /challenge/run/file_[bash]: Not a directory
hacker@globbing~matching-paths-with-:/challenge/files$ cd ~
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{Qkvq1yfQsoJCUhXt2iw2E9HwDx7.dRjM4QDL1kTN0czW}
```
### References: Discussed with my friends

## Mixing Globs
```
 cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run -[cep]*
Error: your argument is too long! It must be 6 characters or less.
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{kzDaFyJ6fd7SPOGU6XhzwW2WWkK.dVjM4QDL1kTN0czW}
```
### Learnings: 




