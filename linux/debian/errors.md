## Fix the apt-get install error: “Media change: please insert the disc labeled ...”

Modify the file /etc/apt/sources.list
```
vim /etc/apt/sources.list
```

The file looks like:
```
# deb cdrom:[Debian GNU/Linux 11.2.0 _Bullseye_ - Official amd64 DVD Binary-1 20211218-11:13]/ bullseye contrib main

deb cdrom:[Debian GNU/Linux 11.2.0 _Bullseye_ - Official amd64 DVD Binary-1 20211218-11:13]/ bullseye contrib main

deb http://security.debian.org/debian-security bullseye-security main contrib non-free
deb-src http://security.debian.org/debian-security bullseye-security main contrib non-free

# bullseye-updates, to get updates before a point release is made;
# see https://www.debian.org/doc/manuals/debian-reference/ch02.en.html#_updates_and_backports
# A network mirror was not selected during install.  The following entries
# are provided as examples, but you should amend them as appropriate
# for your mirror of choice.
#
# deb http://deb.debian.org/debian/ bullseye-updates main contrib
# deb-src http://deb.debian.org/debian/ bullseye-updates main contrib
deb http://deb.debian.org/debian/ bullseye main contrib non-free
deb http://deb.debian.org/debian/ bullseye-updates contrib main non-free
```
This file contains all package sources. Comment the line ```deb cdrom:[Debian GNU/Linux 11.2.0 _Bullseye_ - Official amd64 DVD Binary-1 20211218-11:13]/ bullseye contrib main``` by placing a ```#``` symbol at the beginning of the line and save. 
