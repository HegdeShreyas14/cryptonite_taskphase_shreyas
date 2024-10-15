# Process and Jobs 

## Listing Processes
### Followed the intructions to reach the flag. 
```
 ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 11:26 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /ru
root           7       1  0 11:26 ?        00:00:00 /run/dojo/bin/sleep 6h
root          68       1  0 11:26 ?        00:00:00 /challenge/2758-run-20797
root          72      68  0 11:26 ?        00:00:00 sleep 6h
hacker        73       0  0 11:26 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint
hacker        91      73  0 11:26 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/2758-run-20797
Yahaha, you found me! Here is your flag:
pwn.college{IVAry2KUSJ-ux0ecJ1k0pAiZqCL.dhzM4QDL1kTN0czW}
Now I will sleep for a while (so that you could find me with 'ps').
```
## Killing Processes 
### Learnings: Learnt use of kill command
```
 ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 11:35 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /ru
root           7       1  0 11:35 ?        00:00:00 /run/dojo/bin/sleep 6h
root          71       1  0 11:35 ?        00:00:00 su -c /challenge/.launcher hacker
hacker        73      71  0 11:35 ?        00:00:00 /challenge/dont_run
hacker        74      73  0 11:35 ?        00:00:00 sleep 6h
hacker        75       0  0 11:35 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint
hacker        92       0  0 11:35 pts/1    00:00:00 /run/dojo/bin/ssh-entrypoint
hacker       109      92  0 11:38 pts/1    00:00:00 ps -ef
hacker@processes~killing-processes:~$ kill 73
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{IWha9v7KZrXvTY-BBBwVvopolaN.dJDN4QDL1kTN0czW}
```

## Interrupting Processes
###
```


```


## Suspending Processes
###
```

```
## Resuming Processes
###
```

```




###
