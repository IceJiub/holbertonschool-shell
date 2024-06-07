This directory contains shell scripts.

## 0-current_working_directory
Script that prints the absolute path name of the current working directory.

Example:
```
$ ./0-current_working_directory
/basics
$
```

## 1-listit
Script that displays the contents list of your current directory.

Example:
```
$ ./1-listit
Applications    Documents   Dropbox Movies Pictures
Desktop Downloads   Library Music Public
$
```

## 2-bring_me_home
Script that changes the working directory to the user's home directory.

Example:
```
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ echo $HOME
/home/julien
julien@ubuntu:/tmp$ source ./2-bring_me_home
julien@ubuntu:~$ pwd
/home/julien
julien@ubuntu:~$ 
```

## 3-listfiles
Script that displays current directory contents in a long format.

Example:
```
$ ./3-listfiles
total 40
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:20 README.md
$
```

## 4-listmorefiles
Script that displays current directory contents in long format, including hidden files.

Example:
```
$ ./4-listmorefiles
total 48
drwxr-xr-x@ 6 sylvain staff 204 Jan 25 00:29 .
drwxr-xr-x@ 43 sylvain staff 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:41 4-listmorefiles
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:20 README.md
$
```

## 5-listfilesdigitonly
Script that displays current directory contents and hidden files in long format, with user and group IDs displayed numerically.

Example:
```
$ ./5-listfilesdigitonly
total 56
drwxr-xr-x@ 6 501 20 204 Jan 25 00:29 .
drwxr-xr-x@ 43 501 20 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:23 1-listfiles
-rwxr-xr-x@ 1 501 20 19 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 501 20 20 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:41 4-listmorefiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:43 5-listfilesdigitonly
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:20 README.md
$
```

## 6-firstdirectory
Script that creates a directory named ```my_first_directory``` in the ```/tmp/``` directory.

Example:
```
$ ./6-firstdirectory
$ file /tmp/my_first_directory/
/tmp/my_first_directory/: directory
$
```

## 7-movethatfile
Script that moves the file ```betty``` from ```/tmp/``` to ```/tmp/my_first_directory```.

Example:
```
$ ./7-movethatfile
$ ls /tmp/my_first_directory/
betty
$
```

## 8-firstdelete
Script that deletes the file ```betty``` in ```/tmp/my_first_directory```

Example:
```
$ ./8-firstdelete
$ ls /tmp/my_first_directory/
$
```

## 9-firstdirdeletion
Script that deletes the directory ```my_first_directory``` that is in the ```/tmp``` directory.

Example:
```
$ ./9-firstdirdeletion
$ file /tmp/my_first_directory
/tmp/my_first_directory: cannot open `/tmp/my_first_directory' (No such file or directory)
$
```

## 10-back
Script that changes the working directory to the previous one.

Example:
```
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ cd /var
julien@ubuntu:/var$ pwd
/var
julien@ubuntu:/var$ source ./10-back
/tmp
julien@ubuntu:/tmp$ pwd
/tmp
```

## 11-lists
Script that lists all files and hidden files in long format in the current directory, in the parent of the working directory and the ```/boot``` directory (in this order).

Example:
```
root@34943:~/holbertonschool-shell# basics/11-lists
.:
total 28
drwxr-xr-x 5 root root 4096 Jun  7 10:48 .
drwx------ 1 root root 4096 Jun  7 07:18 ..
drwxr-xr-x 8 root root 4096 Jun  7 11:44 .git
-rw-r--r-- 1 root root    2 Jun  7 07:12 .gitignore
-rw-r--r-- 1 root root   67 Jun  7 07:12 README.md
drwxr-sr-x 2 root root 4096 Jun  7 11:44 basics
drwxr-xr-x 3 root root 4096 Jun  7 10:48 hello

..:
total 44
drwx------ 1 root root 4096 Jun  7 07:18 .
drwxr-xr-x 1 root root 4096 Jun  7 07:11 ..
-rw-r--r-- 1 root root 3106 Oct 15  2021 .bashrc
drwxr-xr-x 3 root root 4096 Feb 12 15:09 .cache
drwx------ 3 root root 4096 Jun  7 08:00 .emacs.d
-rw-r--r-- 1 root root   52 Jun  7 07:18 .gitconfig
drwx------ 4 root root 4096 Jun  7 07:08 .openvscode-server
-rw-r--r-- 1 root root  161 Jul  9  2019 .profile
drwxr-xr-x 2 root root 4096 Feb 12 15:09 empty_directory
drwxr-xr-x 5 root root 4096 Jun  7 10:48 holbertonschool-shell
-rw-r--r-- 1 root root    0 Feb 12 15:09 not_here
-rw-r--r-- 1 root root    0 Feb 12 15:09 old_school
-rw-r--r-- 1 root root    0 Feb 12 15:09 ready_to_be_removed
-rw-r--r-- 1 root root   13 Feb 12 15:09 school

/boot:
total 8
drwxr-xr-x 2 root root 4096 Apr 18  2022 .
drwxr-xr-x 1 root root 4096 Jun  7 07:11 ..
```

## 12-file_type
Script that prints the type of the file named ```iamafile``` in the ```/tmp``` directory.

Example:
```
ubuntu@ip-172-31-63-244:~$ ./12-file_type
/tmp/iamafile: ELF 64-bit LSB  executable, x86-64, version 1 (SYSV), dynamically linked (uses shared libs), for GNU/Linux 2.6.24, BuildID[sha1]=bd39c07194a778ccc066fc963ca152bdfaa3f971, stripped
```

## 13-symbolic_link
Script that creates a symbolic link to ```/bin/ls```, named ```__ls__``` in the current working directory.

Example:
```
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Sep 20 03:24 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:24 ..
ubuntu@ip-172-31-63-244:/tmp/sym$./13-symbolic_link
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Sep 20 03:24 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:24 ..
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls
```

## 14-copy_html
Script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.

Example:
```
root@34943:~/html# ls -l
total 4
-rwxr--r-- 1 root root 28 Jun  7 12:02 14-copy_html
-rwxr--r-- 1 root root  0 Jun  7 12:03 index.html
-rwxr--r-- 1 root root  0 Jun  7 12:03 index2.html
root@34943:~/html# ls -l ..
total 20
-rwxr--r-- 1 root root   28 Jun  7 11:59 14-copy_html
drwxr-xr-x 2 root root 4096 Feb 12 15:09 empty_directory
drwxr-xr-x 5 root root 4096 Jun  7 11:58 holbertonschool-shell
drwxr-xr-x 2 root root 4096 Jun  7 12:03 html
-rw-r--r-- 1 root root    0 Feb 12 15:09 not_here
-rw-r--r-- 1 root root    0 Feb 12 15:09 old_school
-rw-r--r-- 1 root root    0 Feb 12 15:09 ready_to_be_removed
-rw-r--r-- 1 root root   13 Feb 12 15:09 school
root@34943:~/html# ./14-copy_html 
root@34943:~/html# ls -l ..
total 20
-rwxr--r-- 1 root root   28 Jun  7 11:59 14-copy_html
drwxr-xr-x 2 root root 4096 Feb 12 15:09 empty_directory
drwxr-xr-x 5 root root 4096 Jun  7 11:58 holbertonschool-shell
drwxr-xr-x 2 root root 4096 Jun  7 12:03 html
-rwxr--r-- 1 root root    0 Jun  7 12:06 index.html
-rwxr--r-- 1 root root    0 Jun  7 12:06 index2.html
-rw-r--r-- 1 root root    0 Feb 12 15:09 not_here
-rw-r--r-- 1 root root    0 Feb 12 15:09 old_school
-rw-r--r-- 1 root root    0 Feb 12 15:09 ready_to_be_removed
-rw-r--r-- 1 root root   13 Feb 12 15:09 school
```

## 15-lets_move
Script that moves all files beginning with an uppercase letter to the directory ```/tmp/u```.

Example:
```
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 148
drwxrwxr-x  3 ubuntu ubuntu   4096 Sep 20 03:33 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:26 ..
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 My_file
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 Elif_ym
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 random_file
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la /tmp/u
total 8
drwxrwxr-x 2 ubuntu ubuntu 4096 Sep 20 03:33 .
drwxrwxr-x 3 ubuntu ubuntu 4096 Sep 20 03:33 ..
ubuntu@ip-172-31-63-244:/tmp/sym$ ./15-lets_move
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 148
drwxrwxr-x  3 ubuntu ubuntu   4096 Sep 20 03:33 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:26 ..
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 random_file
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la /tmp/u
total 8
drwxrwxr-x 2 ubuntu ubuntu 4096 Sep 20 03:33 .
drwxrwxr-x 3 ubuntu ubuntu 4096 Sep 20 03:33 ..
-rw-rw-r-- 1 ubuntu ubuntu    0 Sep 20 03:32 My_file
-rw-rw-r-- 1 ubuntu ubuntu    0 Sep 20 03:32 Elif_ym
```

## 16-clean_emacs
Script that deletes all files in the current working directory that end with the character ```~```.

Example:
```
ubuntu@ip-172-31-63-244:/tmp/sym$ ls
main.c  main.c~  Makefile~
ubuntu@ip-172-31-63-244:/tmp/sym$ ./16-clean_emacs
ubuntu@ip-172-31-63-244:/tmp/emacs$ ls
main.c
ubuntu@ip-172-31-63-244:/tmp/emacs$
```

## 17-tree
Script that creates the directories ```welcome/```, ```welcome/to/``` and ```welcome/to/school``` in the current directory.

Example:
```
julien@ubuntu:/tmp/h$ ls -l
total 4
-rwxrw-r-- 1 julien julien 44 Sep 20 12:09 17-tree
julien@ubuntu:/tmp/h$ wc -l 17-tree 
2 17-tree
julien@ubuntu:/tmp/h$ head -1 17-tree 
#!/bin/bash
julien@ubuntu:/tmp/h$ tr -cd ' ' < 17-tree | wc -c # you do not have to understand this yet, but the result should be 2, 1 or 0
2
julien@ubuntu:/tmp/h$ ./17-tree 
julien@ubuntu:/tmp/h$ ls
17-tree  welcome
julien@ubuntu:/tmp/h$ ls welcome/
to
julien@ubuntu:/tmp/h$ ls -l welcome/to
total 4
drwxrwxr-x 2 julien julien 4096 Sep 20 12:11 school
julien@ubuntu:/tmp/h$ 
```