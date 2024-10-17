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
###
```

```

## Using Sudo
###
```


```
