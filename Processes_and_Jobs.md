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
### Learnings: Learnt how to interrupt processes.
```
 /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{clFe75Ouq0UaoUv4hvzzK7Nn9nC.dNDN4QDL1kTN0czW}

```


## Suspending Processes
### Learning : Learnt using Ctrl-Z command 
```
 ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 11:46 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /ru
root           7       1  0 11:46 ?        00:00:00 /run/dojo/bin/sleep 6h
hacker        65       0  0 11:46 pts/1    00:00:00 /run/dojo/bin/ssh-entrypoint
hacker        71       0  0 11:46 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint
hacker       100      71  0 11:47 pts/0    00:00:00 ps -ef
hacker@processes~suspending-processes:~$ run
ssh-entrypoint: run: command not found
hacker@processes~suspending-processes:~$ /run
ssh-entrypoint: /run: Is a directory
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         103      71  0 11:48 pts/0    00:00:00 bash /challenge/run
root         105     103  0 11:48 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         103      71  0 11:48 pts/0    00:00:00 bash /challenge/run
root         110      71  0 11:48 pts/0    00:00:00 bash /challenge/run
root         112     110  0 11:48 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{Y_mXSAujooFmA1RnXxJesBD9DhC.dVDN4QDL1kTN0czW}
```
## Resuming Processes
###
```

```




###
