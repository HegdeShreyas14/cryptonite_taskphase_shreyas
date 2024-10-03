# Digesting Documentation
##  Learning from documentation
### The task was pretty straightforward, I followed the question statement to get to the flag

## Using complex anaylsis 
### 
```
/challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{AhNbv6NGHwrQ9rX3-hJO8bAuBQY.dVjM5QDL1kTN0czW}
```
### Followed the given instructions to get to the flag


## Reading and Searching Manuals
### Followed the instructions to reach the flag in both the tasks
## Searching for manuals
```
man man
MAN(1)                           Manual pager utils                          MAN(1)

NAME
       man - an interface to the system reference manuals

SYNOPSIS
       man [man options] [[section] page ...] ...
       man -k [apropos options] regexp ...
       man -K [man options] [section] term ...
       man -f [whatis options] page ...
       man -l [man options] file ...
       man -w|-W [man options] page ...

DESCRIPTION
       man  is  the system's manual pager.  Each page argument given to man is nor‐
       mally the name of a program, utility or function.  The manual  page  associ‐
       ated  with  each of these arguments is then found and displayed.  A section,
       if provided, will direct man to look only in that  section  of  the  manual.
       The default action is to search in all of the available sections following a
       pre-defined order (see DEFAULTS), and to show only  the  first  page  found,
       even if page exists in several sections.

       The  table  below  shows  the  section numbers of the manual followed by the
       types of pages they contain.

       1   Executable programs or shell commands
       2   System calls (functions provided by the kernel)
       3   Library calls (functions within program libraries)
       4   Special files (usually found in /dev)
       5   File formats and conventions, e.g. /etc/passwd
       6   Games
       7   Miscellaneous (including macro packages and conventions),  e.g.  man(7),
           groff(7)
       8   System administration commands (usually only for root)
       9   Kernel routines [Non standard]

       A manual page consists of several sections.

       Conventional  section  names include NAME, SYNOPSIS, CONFIGURATION, DESCRIP‐
       TION, OPTIONS, EXIT STATUS, RETURN VALUE, ERRORS, ENVIRONMENT,  FILES,  VER‐
       SIONS, CONFORMING TO, NOTES, BUGS, EXAMPLE, AUTHORS, and SEE ALSO.

       The following conventions apply to the SYNOPSIS section and can be used as a
       guide in other sections.

       bold text          type exactly as shown.
       italic text        replace with appropriate argument.
       [-abc]             any or all arguments within [ ] are optional.
       -a|-b              options delimited by | cannot be used together.
       argument ...       argument is repeatable.
       [expression] ...   entire expression within [ ] is repeatable.

       Exact rendering may vary depending on the output device.  For instance,  man
       will  usually  not be able to render italics when running in a terminal, and
       will typically use underlined or coloured text instead.

       The command or function illustration is a pattern that should match all pos‐
       sible  invocations.  In some cases it is advisable to illustrate several ex‐
       clusive invocations as is shown in the SYNOPSIS section of this manual page.

EXAMPLES
       man ls
           Display the manual page for the item (program) ls.

       man man.7
           Display the manual page for macro package man from section 7.  (This  is
           an alternative spelling of "man 7 man".)

       man 'man(7)'
           Display  the manual page for macro package man from section 7.  (This is
           another alternative spelling of "man 7 man".  It may be more  convenient
           when  copying  and  pasting cross-references to manual pages.  Note that
           the parentheses must normally be quoted to protect them from the shell.)

       man -a intro
           Display, in succession, all of the available  intro  manual  pages  con‐
           tained  within  the  manual.   It is possible to quit between successive
           displays or skip any of them.

       man -t bash | lpr -Pps
           Format the manual page for bash into the default troff or  groff  format
           and  pipe  it  to the printer named ps.  The default output for groff is
           usually PostScript.  man --help should advise as to which  processor  is
           bound to the -t option.

       man -l -Tdvi ./foo.1x.gz > ./foo.1x.dvi
           This  command  will  decompress  and format the nroff source manual page
           ./foo.1x.gz into a device independent (dvi) file.   The  redirection  is
           necessary  as the -T flag causes output to be directed to stdout with no
           pager.  The output could be viewed with a program such as xdvi  or  fur‐
           ther processed into PostScript using a program such as dvips.

       man -k printf
           Search  the  short  descriptions  and  manual page names for the keyword
           printf as regular expression.  Print out  any  matches.   Equivalent  to
           apropos printf.

       man -f smail
           Lookup  the manual pages referenced by smail and print out the short de‐
hacker@man~searching-for-manuals:~$
hacker@man~searching-for-manuals:~$ man -k[apropos flag]
man: invalid option -- '['
Try 'man --help' or 'man --usage' for more information.
hacker@man~searching-for-manuals:~$ man -k
apropos what?
hacker@man~searching-for-manuals:~$ man -k flag
dpkg-buildflags (1)  - returns build flags to use during package build
Dpkg::BuildFlags (3perl) - query build flags
fegetexceptflag (3)  - floating-point rounding and exception handling
fesetexceptflag (3)  - floating-point rounding and exception handling
gqoeouqdkh (1)       - print the flag!
i386 (8)             - change reported architecture in new program environment and/...
ioctl_iflags (2)     - ioctl() operations for inode flags
linux32 (1)          - change reported architecture in new program environment and/...
linux64 (1)          - change reported architecture in new program environment and/...
pcap-config (1)      - write libpcap compiler and linker flags to standard output
security_compute_av_flags (3) - query the SELinux policy database in the kernel
security_compute_av_flags_raw (3) - query the SELinux policy database in the kernel
set_matchpathcon_flags (3) - set flags controlling the operation of matchpathcon or...
set_matchpathcon_invalidcon (3) - set flags controlling the operation of matchpathc...
set_matchpathcon_printf (3) - set flags controlling the operation of matchpathcon o...
setarch (1)          - change reported architecture in new program environment and/...
setarch (8)          - change reported architecture in new program environment and/...
x86_64 (8)           - change reported architecture in new program environment and/...
hacker@man~searching-for-manuals:~$ man gqoeouqdkh

CHALLENGE(1)                     Challenge Commands                    CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --gqoeou NUM
              print the flag if NUM is 674

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The  repository for this dojo: <https://github.com/pwncollege/linux-luminar‐
       ium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                           May 2024                         CHALLENGE(1)
hacker@man~searching-for-manuals:~$ /challenge/challenge --gpoeou 674
Incorrect usage! Please read the challenge man page!
hacker@man~searching-for-manuals:~$ /challenge/challenge --gpoeou 674\
>
Incorrect usage! Please read the challenge man page!
hacker@man~searching-for-manuals:~$ /challenge/challenge --gpoeou 674
Incorrect usage! Please read the challenge man page!
hacker@man~searching-for-manuals:~$ /challenge/challenge -gpoeou 674
Incorrect usage! Please read the challenge man page!
hacker@man~searching-for-manuals:~$ /challenge/challenge --gpoeou 674
Incorrect usage! Please read the challenge man page!
hacker@man~searching-for-manuals:~$ /challenge/challenge
Incorrect usage! Please read the challenge man page!
hacker@man~searching-for-manuals:~$ /challenge/challenge --gqoeou 674
Correct usage! Your flag: pwn.college{gq__MoePoCCCuqICd67kT-Mhxrc.dZTM4QDL1kTN0czW}
```
### Learnings:Similar to the previous question but had to scout for the command

