# Chaining Commands 

## Chaining with semi colons

```
 /challenge/pwn;/challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{Ac_GDuQs9av17DTROTRLKLGi_T-.dVTN4QDL1kTN0czW}
```

## Your First Shell Script 
### Reference: Had to ask my friends for help as I did not know how to begin.
```
hacker@chaining~your-first-shell-script:~$ touch x.sh
hacker@chaining~your-first-shell-script:~$ echo /challenge/pwn >> x.sh
hacker@chaining~your-first-shell-script:~$ echo /challenge/college >> x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{YnUfdsTb1rzSqbYTogfSfQdeUM3.dFzN4QDL1kTN0czW}
```

## Redirecting Script Output
### Learnings: Learnt how to pipe the script output
```
touch script.sh
hacker@chaining~redirecting-script-output:~$ echo /challenge/pwn >> script.sh
hacker@chaining~redirecting-script-output:~$ echo /challenge/college >> script.sh
hacker@chaining~redirecting-script-output:~$ bash script  | /challenge/solve
Please name your script with an '.sh' extension. This isn't strictly necessary
eventually, but we'll keep things explicit for the next few levels.
The data piped from /challenge/pwn did not match what I expected. I
re-randomize the data every time you input a new line to the shell, so you must
get it right in one shot! Make sure to pipe the output from your script to
/challenge/solve.
hacker@chaining~redirecting-script-output:~$ bash script.sh  | /challenge/solve
Correct! Here is your flag:
pwn.college{ogVUczG-kZ9I6vwVAVNitegcr1V.dhTM5QDL1kTN0czW}
```

## Executable Shell Scripts 
 Took some time to solve the question as I was doing silly errors.
```
touch script.sh
hacker@chaining~executable-shell-scripts:~$ echo /challenge/solve >> script.sh
hacker@chaining~executable-shell-scripts:~$ chmod a+x /challenge/solve
chmod: changing permissions of '/challenge/solve': Operation not permitted
hacker@chaining~executable-shell-scripts:~$ chmod a+x script.sh
hacker@chaining~executable-shell-scripts:~$ /challenge/solve
You must make a shellscript in your home directory that will launch
/challenge/solve, make it executable, and invoke it without explicitly
specifying 'bash'!
hacker@chaining~executable-shell-scripts:~$ ./script.sh
./script.sh: line 1: /challenge/pwn: No such file or directory
./script.sh: line 2: /challenge/college: No such file or directory
Congratulations on your shell script execution! Your flag:
pwn.college{cVSomfFe8cJ2UZX2wRVp2KIfugb.dRzNyUDL1kTN0czW}
```
