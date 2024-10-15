# Perceiving Permissions 
## Changing File Ownership
### Learnings: Learnt how to change owner using chown command
```
 ls -l
total 48
-rw-r--r-- 1 hacker hacker    4 Oct  6 10:16 COLLEGE
drwxr-xr-x 2 hacker hacker 4096 Oct  1 11:05 Desktop
-rw-r--r-- 1 hacker hacker   19 Oct 15 06:07 PWN
drwxr-xr-x 2 hacker hacker 4096 Oct  1 14:36 asd
-rw-r--r-- 1 root   hacker   77 Oct  8 04:09 com
-rw-r--r-- 1 hacker hacker    0 Oct  2 06:34 flag
lrwxrwxrwx 1 hacker hacker   18 Oct  2 10:32 fuck -> /challenge/catflag
-rw-r--r-- 1 root   hacker   58 Oct 12 16:05 h
-rw-r--r-- 1 hacker hacker  829 Oct  7 13:16 instructions
drwxr-xr-x 2 hacker hacker 4096 Oct  2 04:34 leap
-rw-r--r-- 1 hacker hacker   93 Oct  7 13:16 myflag
lrwxrwxrwx 1 hacker hacker    5 Oct  2 10:34 newfuck -> /flag
lrwxrwxrwx 1 hacker hacker    5 Oct  2 09:10 not-the-flag -> /flag
-rw-r--r-- 1 root   hacker   77 Oct  7 14:42 out
-rw-r--r-- 1 root   hacker   77 Oct  8 04:10 pwn
-rw-r--r-- 1 hacker hacker  435 Oct  6 10:27 the-flag
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{wPZlXQnAkITWK0PcdTskfBUOBBZ.dFTM2QDL1kTN0czW}
```

##
###
```

```


##
###
```

```

##
###
```

```

##
###
```

```



