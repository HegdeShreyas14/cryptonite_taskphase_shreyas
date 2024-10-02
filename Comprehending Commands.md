# Comprehending Commands 
## Challenges 1 to 8:
### Learnings:Learnt use of multiple commands such as cat,grep,touch ,ls and cd.
### Most of the tasks were straight forward and reading the instructions helped solve the problem.

### References:Did not use reference other than the given problem statements

## Challenge 9:An Epic Filesystem Quest
## CODE:
```
 cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
LEAD  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin   challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat LEAD
Yahaha, you found me!
The next clue is in: /usr/share/perl/5.30.0/unicore/lib/GrExt

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/shre/prl/5.30.0/unicore/lib/GrExt
ssh-entrypoint: cd: /usr/shre/prl/5.30.0/unicore/lib/GrExt: No such file or directory
hacker@commands~an-epic-filesystem-quest:/$ cat  /usr/share/perl/5.30.0/unicore/lib/GrExt
cat: /usr/share/perl/5.30.0/unicore/lib/GrExt: Is a directory
hacker@commands~an-epic-filesystem-quest:/$ ls  /usr/share/perl/5.30.0/unicore/lib/GrExt
\INSIGHT-TRAPPED  Y.pl
hacker@commands~an-epic-filesystem-quest:/$ ls /usr/share/perl/5.30.0/unicore/lib/GrExt
INSIGHT-TRAPPED  Y.pl
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/perl/5.30.0/unicore/lib/GrExt/INSIGHT-TRAPPED
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/drivers/staging/rtl8192e
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/drivers/staging/rtl8192e
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/staging/rtl8192e$ ls
Kconfig   dot11d.c      rtl819x_BAProc.c  rtl819x_TS.h         rtllib_crypt_tkip.c  rtllib_rx.c          rtllib_wx.c
MEMO      dot11d.h      rtl819x_HT.h      rtl819x_TSProc.c     rtllib_crypt_wep.c   rtllib_softmac.c
Makefile  rtl8192e      rtl819x_HTProc.c  rtllib.h             rtllib_debug.h       rtllib_softmac_wx.c
TODO      rtl819x_BA.h  rtl819x_Qos.h     rtllib_crypt_ccmp.c  rtllib_module.c      rtllib_tx.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/staging/rtl8192e$ cd MEMO
ssh-entrypoint: cd: MEMO: Not a directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/staging/rtl8192e$ cat MEMO
Tubular find!
The next clue is in: /usr/lib/python3/dist-packages/tornado/test/gettext_translations/fr_FR

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/staging/rtl8192e$ ^C
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/staging/rtl8192e$ cat /usr/lib/python3/dist-packages/tornado/test/gettext_translations/fr_FR
cat: /usr/lib/python3/dist-packages/tornado/test/gettext_translations/fr_FR: Is a directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/staging/rtl8192e$ ls
Kconfig   dot11d.c      rtl819x_BAProc.c  rtl819x_TS.h         rtllib_crypt_tkip.c  rtllib_rx.c          rtllib_wx.c
MEMO      dot11d.h      rtl819x_HT.h      rtl819x_TSProc.c     rtllib_crypt_wep.c   rtllib_softmac.c
Makefile  rtl8192e      rtl819x_HTProc.c  rtllib.h             rtllib_debug.h       rtllib_softmac_wx.c
TODO      rtl819x_BA.h  rtl819x_Qos.h     rtllib_crypt_ccmp.c  rtllib_module.c      rtllib_tx.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/staging/rtl8192e$ ls /usr/lib/python3/dist-package
s/tornado/test/gettext_translations/fr_FR
CLUE-TRAPPED  LC_MESSAGES
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/staging/rtl8192e$ cat /usr/lib/python3/dist-packages/tornado/test/gettext_translations/fr_FR/CLUE-TRAPPED
Tubular find!
The next clue is in: /opt/linux/linux-5.4/drivers/media/usb/s2255
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/staging/rtl8192e$ cd /opt/linux/linux-5.4/drivers/media/usb/s2255
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/media/usb/s2255$ ls
Kconfig  Makefile  SECRET  built-in.a  s2255drv.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/media/usb/s2255$ cat /opt/linux/linux-5.4/drivers/media/usb/s2255/SECRET
Tubular find!
The next clue is in: /opt/linux/linux-5.4/include/config/dcache/word

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/media/usb/s2255$ cd /opt/linux/linux-5.4/include/config/dcache/word
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/dcache/word$ ls
MESSAGE  access.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/dcache/word$ cat /opt/linux/linux-5.4/inclu
de/config/dcache/word/MESSAGE
Yahaha, you found me!
The next clue is in: /usr/share/racket/pkgs/r5rs-doc/r5rs/scribblings

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/dcache/word$ cd /usr/share/racket/pkgs/r5rs-doc/r5rs/scribblings
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/r5rs-doc/r5rs/scribblings$ ls
README  r5rs-std
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/r5rs-doc/r5rs/scribblings$ cat /usr/share/racket/pkgs/r5
rs-doc/r5rs/scribblings/README
Congratulations, you found the clue!
The next clue is in: /usr/lib/python3/dist-packages/twisted/scripts/__pycache__

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/r5rs-doc/r5rs/scribblings$ cd /usr/lib/python3/dist-packages/twisted/scripts/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/twisted/scripts/__pycache__$ ls
__init__.cpython-38.pyc      _twistw.cpython-38.pyc   trial.cpython-38.pyc
_twistd_unix.cpython-38.pyc  htmlizer.cpython-38.pyc  twistd.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/twisted/scripts/__pycache__$ ls -a
.   .BRIEF                   _twistd_unix.cpython-38.pyc  htmlizer.cpython-38.pyc  twistd.cpython-38.pyc
..  __init__.cpython-38.pyc  _twistw.cpython-38.pyc       trial.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/twisted/scripts/__pycache__$ cat /usr/lib/python3/dist-packages/twisted/scripts/__pycache__/.BRIEF
Lucky listing!
The next clue is in: /opt/radare2/shlr/spp

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/twisted/scripts/__pycache__$ cd ^C
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/twisted/scripts/__pycache__$ cd /opt/radare2/shlr/spp
hacker@commands~an-epic-filesystem-quest:/opt/radare2/shlr/spp$ ls
BUGS     Makefile   bin           config.h       configure      meson.build  r_api.c  spp.1  spp.d  spp.o
LICENSE  README.md  config.def.h  config.mk.acr  configure.acr  p            r_api.h  spp.c  spp.h
hacker@commands~an-epic-filesystem-quest:/opt/radare2/shlr/spp$ ls -a
.   .POINTER  LICENSE   README.md  config.def.h  config.mk.acr  configure.acr  p        r_api.h  spp.c  spp.h
..  BUGS      Makefile  bin        config.h      configure      meson.build    r_api.c  spp.1    spp.d  spp.o
hacker@commands~an-epic-filesystem-quest:/opt/radare2/shlr/spp$ cat /opt/radare2/shlr/spp/.POINTER
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{QQu2uG6cp1wKC0_riODIBHU8wS7.dljM4QDL1kTN0czW}
hacker@commands~an-epic-filesystem-quest:/opt/radare2/shlr/spp$
```
### Learnings:Better understanding of cat function and patience 
### References: Discussion with friends.
## Challenge 10:Making Directories
### Learnings:Learnt the use of mkdir command
### References:None 


## Challenge 11: Finding Files 
```
 cd /
hacker@commands~finding-files:/$ find -name flag
find: ‘./root’: Permission denied
find: ‘./etc/ssl/private’: Permission denied
find: ‘./tmp/tmp.G9qthVCks5’: Permission denied
./usr/local/share/radare2/5.9.5/flag
./usr/local/lib/python3.8/dist-packages/pwnlib/flag
./usr/share/emacs/26.3/lisp/international/flag
./home/hacker/flag
find: ‘./var/cache/apt/archives/partial’: Permission denied
find: ‘./var/cache/ldconfig’: Permission denied
find: ‘./var/cache/private’: Permission denied
find: ‘./var/log/private’: Permission denied
find: ‘./var/log/apache2’: Permission denied
find: ‘./var/log/mysql’: Permission denied
find: ‘./var/lib/apt/lists/partial’: Permission denied
find: ‘./var/lib/mysql-keyring’: Permission denied
find: ‘./var/lib/php/sessions’: Permission denied
find: ‘./var/lib/private’: Permission denied
find: ‘./var/lib/mysql-files’: Permission denied
find: ‘./var/lib/mysql’: Permission denied
find: ‘./run/mysqld’: Permission denied
find: ‘./run/sudo’: Permission denied
find: ‘./proc/tty/driver’: Permission denied
find: ‘./proc/1/task/1/fd’: Permission denied
find: ‘./proc/1/task/1/fdinfo’: Permission denied
find: ‘./proc/1/task/1/ns’: Permission denied
find: ‘./proc/1/fd’: Permission denied
find: ‘./proc/1/map_files’: Permission denied
find: ‘./proc/1/fdinfo’: Permission denied
find: ‘./proc/1/ns’: Permission denied
find: ‘./proc/7/task/7/fd’: Permission denied
find: ‘./proc/7/task/7/fdinfo’: Permission denied
find: ‘./proc/7/task/7/ns’: Permission denied
find: ‘./proc/7/fd’: Permission denied
find: ‘./proc/7/map_files’: Permission denied
find: ‘./proc/7/fdinfo’: Permission denied
find: ‘./proc/7/ns’: Permission denied
./opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
./opt/radare2/libr/flag
./nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
./nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
hacker@commands~finding-files:/$ cat /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
cat: /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:/$ cat /nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
cat: /nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:/$ cat /nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
cat: /nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag: Is a directory
hacker@commands~finding-files:/$ cat /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
cat: /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:/$ cat /usr/share/emacs/26.3/lisp/international/flag
pwn.college{U_JZISgr9oDyfWHaGm2ws3PELlv.dJzM4QDL1kTN0czW}
```
## Learnings:Learnt about command find and its working
Changed directory to / then tried finding flag by searching the directories to which I had access.
### References:Discussion with friends
