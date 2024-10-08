# Practicing Piping
## Redirecting output
Fairly straight forward, followed the intructions to reach the flag.
```
echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{A32JVNawm1jz49X0BGtx7Dv5oCY.dRjN1QDL1kTN0czW}
```
### Learnings: Learnt the functioning of ">"


## Redirecting More Output
Followed the instructions to the flag
```
/challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{cfm6ry2zwNVE7ReF0gz6ywIko7E.dVjN1QDL1kTN0czW}
```


## Appending Output
### Learnings: Learnt use of the append operator  ">>"

```

hacker@piping~appending-output:~$ /challenge/run >> ~/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat ~/the-flag
 |
\|/ This is the first half:
 v
pwn.college{8R7vGYkwHXjcy9sgTiKtIiZs89j.ddDM5QDL1kTN0czW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
```

## Redirecting Errors
### Learnings : Learnt how to redirect errors 
```
 /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{83diP0zsQTJ5bNgFhTwCyA0FAN_.ddjN1QDL1kTN0czW}
```
References: None taken
## Redirecting Input
```
 echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{I-VABkGkgTNyJ4pTJxlMJRKZgGv.dBzN1QDL1kTN0czW}
```
### Learnings: Revisited usage of echo command

## Grepping stored results
```
 /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn /tmp/data.txt
pwn
pwning
pwns
pwn.college{wUW8cbxFE6Y2WcVMHm_y_TrRv8S.dhTM4QDL1kTN0czW}
pwned
```

## Grepping Live Output
```
/challenge/run | grep pwn
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwns
pwn.college{ILM5tiefDCuvCYbaxnKsCZUtIPU.dlTM4QDL1kTN0czW}
pwned
pwn
pwning
```
### Learnings: Understood the use and working of the pipe command 

## Grepping Errors 
### Learnings: This challenge was a bit tricky as I did not completely understand the command.
```

hacker@piping~grepping-errors:~$ /challenge/run
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...

[FAIL] You did not satisfy all the execution requirements.
[FAIL] Specifically, you must fix the following issue:
[FAIL]   stderr of this process does not appear to be a pipe!
hacker@piping~grepping-errors:~$ /challenge/run grep pwn
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...

[FAIL] You did not satisfy all the execution requirements.
[FAIL] Specifically, you must fix the following issue:
[FAIL]   stderr of this process does not appear to be a pipe!
hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwning
pwn.college{YGqeA2QsEzVjWMD0IweOIPv-yyn.dVDM5QDL1kTN0czW}
pwns
pwn
pwned
```
Took me multiple tries to get to the flag
### References: Asked a friend on how to use the command.


## Piped Data with Tee
### 
```
/challenge/pwn | tee com | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee pwn | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat pwn
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "E7BsDP52"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee --secret E7BsDP52 | /challenge/college
Processing...
/bin/tee: unrecognized option '--secret'
Try '/bin/tee --help' for more information.
You must pipe the output of /challenge/pwn into /challenge/college (or 'tee'
for debugging).
/challenge/secret needs to the on the receiving end of the output of
'/challenge/pwn' (or 'tee' for debugging).
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret E7BsDP52
Processing...
You must pipe the output of /challenge/pwn into /challenge/college (or 'tee'
for debugging).
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret E7BsDP52 | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{E7BsDP522h1VehirrianUYRPv7m.dFjM5QDL1kTN0czW}
```
This challenge was a bit tricky as I did not understand the use of tee fully, had to run it multiple times to get to the flag, I got the flag without using tee though.

References: Took help from a friend.


## Writing to Multiple Programs 
### Learnings : Learnt on how to pass output as input to multiple files 
```
/challenge/hack | tee >/challenge/the >/challenge/planet
ssh-entrypoint: /challenge/the: Permission denied
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the ) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
17622206732120627559
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{csjxey0vER14bRnswRbaSSDGp6z.dBDO0UDL1kTN0czW}
```
This challenge was a bit tricky and I did not completely understand the code.
### References: Asked my friend for help. 

## Split piping stderr and stdout 
### Learnings: Learnt combined use of the commands.
```
/challenge/hack > >(/challenge/planet) 2>(/challenge/the)
You must redirect my standard error into '/challenge/the'!
Are you sure you're properly redirecting /challenge/hack's standard error into
'/challenge/the'?
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{0aApqHoJ_RkPZOCCPy_d8JZXoC9.dFDNwYDL1kTN0czW}
```
The challenge was a bit tricky as I was repeatedly getting the syntax wrong 





