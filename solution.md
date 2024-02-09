create new user
# sudo su
# root@ubuntu-focal:/home# adduser altschool

loging in user altschool
# root@ubuntu-focal:/home# su -l altschool

creating directories inside home/altschool
# altschool@ubuntu-focal:~$ mkdir test
# altschool@ubuntu-focal:~$ mkdir code
# altschool@ubuntu-focal:~$ mkdir personal
# altschool@ubuntu-focal:~$ mkdir misc

Changing text directory absolute path
# altschool@ubuntu-focal:~$ cd /home/altschool/test

Changing text directory relative path
# altschool@ubuntu-focal:~$ cd test

Creating a file name Hello A using echo command
# altschool@ubuntu-focal:~$ cd misc
# altschool@ubuntu-focal:~/misc$ echo Hello A > fileA
# altschool@ubuntu-focal:~/misc$ ls
# fileA

Creating an empty file name fileB and populating it with dummy text
# altschool@ubuntu-focal:~/misc$ cat > fileB
# dummmmmmyyyyyyyyy 
ends dummy content with Ctrl + D
# altschool@ubuntu-focal:~/misc$ ls
# fileA fileB

Copy fileA into fileC
# altschool@ubuntu-focal:~/misc$ cp fileA fileC
# altschool@ubuntu-focal:~/misc$ ls
# fileA fileB fileC

move fileB into fileD
# altschool@ubuntu-focal:~/misc$ mv fileB fileD
# altschool@ubuntu-focal:~/misc$ ls
# fileA fileC fileD

ceate archive calles misc.tar
# altschool@ubuntu-focal:~$ tar -cvf misc.tar
# altschool@ubuntu-focal:~$ ls
# code misc misc.tar personal test

ceate archive calles misc.tar.gz
# altschool@ubuntu-focal:~$ tar -czvf misc.tar.gz
# altschool@ubuntu-focal:~$ ls
# code misc misc.tar misc.tar.gz personal test

create user
# altschool@ubuntu-focal:~$ sudo adduser mmasinachi

force user to chnage password upon login
# altschool@ubuntu-focal:~$ sudo passwd -e mmasinachi
# passwd: password expiry information changed.

new user login with adminstrative anforcement to change password
# altschool@ubuntu-focal:~$ sudo su -l mmasinachi
# You are required to change your password immediately
# (administrator enforced)
# Changing password for mmasinachi.
# Current password:
# New password:
# Retype new password:

lock user passwprd
# altschool@ubuntu-focal:~$sudo passwd -l mmasinachi

create user with no shell login
# altschool@ubuntu-focal:~$sudo useradd Bilbo

disable password based auth for ssh
# altschool@ubuntu-focal:~$ vi /etc/ssh/sshd-config
 then chnage
# PasswordAuthentication no
to exit vim and save file
# :wq!

Disable SSH root login
# altschool@ubuntu-focal:~$ vim /etc/ssh/sshd-config
then chnage
# PaermitRootLogin no
to exit vim and save file
# :wq!