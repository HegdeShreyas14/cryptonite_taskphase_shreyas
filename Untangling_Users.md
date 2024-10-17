# Untangling Users
## Becoming root with su
### Learnings: Learnt use of switch user command
```
 su root
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{MWNMTkkQeah2x9XEIwVzavrCUEi.dVTN0UDL1kTN0czW}
```

## Other Users with su 
Straightforward question but ended up using the wrong command twice (cat flag)
```
 su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ cat flag
zardus@users~other-users-with-su:/home/hacker$ cat /flag
cat: /flag: Permission denied
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{YEjO3B3kHmFbCDbTBpMXylr_lxO.dZTN0UDL1kTN0czW}
```

## Cracking Password
### Learnings: Learnt how to 
```
 john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
0g 0:00:00:14 0% 2/3 0g/s 281.6p/s 281.6c/s 281.6C/s serena..88888888
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04856g/s 282.8p/s 282.8c/s 282.8C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ --show
ssh-entrypoint: --show: command not found
hacker@users~cracking-passwords:~$ su zardus
Password:
su: Authentication failure
hacker@users~cracking-passwords:~$ su zardus
Password:
su: Authentication failure
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{cyb6nrtUAXkG41-Gsi-htx_tNOq.ddTN0UDL1kTN0czW}
```

## Using Sudo
###
```


```
