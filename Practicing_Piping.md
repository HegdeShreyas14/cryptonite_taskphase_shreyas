# Practicing Piping
## Redirecting output
Fairly straight forward, followed the intructions to reach the flag.
```
echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{A32JVNawm1jz49X0BGtx7Dv5oCY.dRjN1QDL1kTN0czW}
```
## Learnings: Learnt the functioning of ">"


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
