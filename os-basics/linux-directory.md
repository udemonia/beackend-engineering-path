# linux directory

like a tree

root /

look in slash - that file is in slash - talking about root

/bin - binary - machine readable binaries

/etc - etsy - configuration files - control how the applications behave (boot into text or graphical)

/home - users home directory - separate your data from another users data

/opt - optional or third party applications (google earth)

/tmp - temporary some distros clear at boot

/usr - user, user related programs... can have sub directories. /usr/bin - binaries for a particular usr

/usr/sbin - users system admin binaries 

/var - variable data - log files - data that changes often /var/logs

/boot - files needed to boot the system

/cdrom - mount point for cdrom

/dev - device files - controlled by the OS and the sys admins

/srv - contains data that is served - e.g. srv/www - web files

/srv/ftp - served filed for ftp

/sys - display and sometimes configure

## Application Directory Structure

option 1

- /usr/local/{{ app name }}/bin
- /usr/local/{{ app name }}/etc
- /usr/local/{{ app name }}/lib
- /usr/local/{{ app name }}/log

option 2
  
- /opt/{{ app name }}/bin
- /opt/{{ app name }}/etc
- /opt/{{ app name }}/lib
- /opt/{{ app name }}/log

option 3

- /etc/opt/myApp - installed binaries here
- /opt/myApp/bin - 
- /opt/myApp/lib - 
- /var/opt/myApp - logs stored here

## mount points

files get mounted to a directory for access

## File Permissions


 Brandon: ~/dev/backend-engineering-roadmap/os-basics [git:os]
🪐 $la
total 16
drwxr-xr-x  4 brandonlambert  staff   128B May  8 22:03 ./
drwxr-xr-x  9 brandonlambert  staff   288B May  8 21:01 ../
-rw-r--r--  1 brandonlambert  staff   1.4K May  9 06:54 linux-directory.md
-rw-r--r--  1 brandonlambert  staff   756B May  8 21:53 os-memory-linux.md

the first character

- regular file

d directory

i symbolic link

the next come i

rwx - -wx r-x

User Group Other All

Permissions

drwxr-xr-x

d = file type

rwx = user

r-x = group

-xr = all

Permissions are also called modes which is why we use chmod to update them

Summary _ls tells us the permissions associated with a directory/file_

## chmod

There are two ways to update permissions

chmod [u: user, g: group, o: other, a: all] [+/-/=] [rwx] {{ file name }}

chmod u+w test.js

We have provided write access to the user for the test.js file

-rw-rw-r--  1 blambert blambert    0 May  9 13:55 example.txt

blambert@s-md-pd-scrp-03:~/permissons-test$ chmod u+x example.txt

blambert@s-md-pd-scrp-03:~/permissons-test$ ls -alhF

> > **-rwxrw-r--  1 blambert blambert    0 May  9 13:55 example.txt**

In the above example, we've added execute permissions at the user level for the example.txt file

we can use a comma to separate multiple changes

> > **-rwxrw-r-- 1 blambert blambert 0 May  9 13:55 example.txt**

blambert@s-md-pd-scrp-03:~/permissons-test$ chmod g+x,a+w example.txt

blambert@s-md-pd-scrp-03:~/permissons-test$ ls -l

> > **-rwxrwxrw- 1 blambert blambert 0 May  9 13:55 example.txt**
