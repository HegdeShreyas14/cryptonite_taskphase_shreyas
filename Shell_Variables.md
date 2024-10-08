# Shell Variables
## Printing Variables 
### Fairly straightforward challenge,followed the instructions to reach the flag.
```
 echo $FLAG
pwn.college{83j_ueXQd44CtC76mQd6QtiO7z0.ddTN1QDL1kTN0czW}
```

## Setting Variables
###   Simple challenge, was able to do by following the instructions 
```
 PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{I4ejrWLyKyD4ZuGTVt3fQIDQSxv.dlTN1QDL1kTN0czW}
```

## Multi-word variables 
### Really simple challenge, was able to do easily. 
```
 PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{wqoQgiJOUSfMMYWO4Gp9T93NC4N.dBjN1QDL1kTN0czW}
```

## Exporting Variables 
###  Fairly simple program, followed instructions to reach the flag.
```
 export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{Yjg_wT-ylBUqOJipsfpLdGbj8GX.dJjN1QDL1kTN0czW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```
