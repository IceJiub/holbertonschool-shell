This directory contains shell scripts about permissions.

## 0-iam_betty
This script switches the current user to the user ```betty```.

Example:
```
root@18072:/tmp# ./0-iam_betty 
$ whoami
betty
$
```

## 1-who_am_i
This script prints the effective username of the current user.

Example:
```
root@18072:/tmp# ./1-who_am_i
root
```

## 2-groups
This script prints all the groups the current user is part of.

Example:
```
julien@ubuntu:/tmp/h$ ./2-groups
julien adm cdrom sudo dip plugdev lpadmin sambashare
julien@ubuntu:/tmp/h$ 
```

## 3-new_owner
This script changes the owner of the file hello to the user betty.

Example:
```
julien@ubuntu:/tmp$ ls -l
total 4
-rwxrw-r-- 1 julien julien 30 Sep 20 14:23 3-new_owner
-rw-rw-r-- 1 julien julien  0 Sep 20 14:18 hello
julien@ubuntu:/tmp$ sudo ./3-new_owner 
julien@ubuntu:/tmp$ ls -l
total 4
-rwxrw-r-- 1 julien julien 30 Sep 20 14:23 3-new_owner
-rw-rw-r-- 1 betty  julien  0 Sep 20 14:18 hello
julien@ubuntu:/tmp$
```

## 4-empty
This script creates an empty file called ```hello```.

Example:
```
root@211b-2377118072:/tmp# ls -l
total 4
-rwxr-xr-x 1 root root 24 Jun 10 13:59 4-empty
root@211b-2377118072:/tmp# ./4-empty 
root@211b-2377118072:/tmp# ls -l
total 4
-rwxr-xr-x 1 root root 24 Jun 10 13:59 4-empty
-rw-r--r-- 1 root root  0 Jun 10 13:59 hello
root@211b-2377118072:/tmp#
```

## 5-execute
This script adds execute permission to the owner of the file ```hello```.

Example:
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:26 5-execute
-rw-rw-r-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./hello
bash: ./hello: Permission denied
julien@ubuntu:/tmp/h$ ./5-execute 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:26 5-execute
-rwxrw-r-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```

## 6-multiple_permissions
This script adds execute permission to the owner and the group owner, and read permission to other users, to the file ```hello```.

Example:
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 36 Sep 20 14:31 6-multiple_permissions
-rw-r----- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./6-multiple_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 36 Sep 20 14:31 6-multiple_permissions
-rwxr-xr-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$
```

## 7-everybody
This script adds execution permission to the owner, the group owner and the other users, to the file ```hello``` without using commas.

Example:
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:35 7-everybody
-rw-r----- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./7-everybody 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:35 7-everybody
-rwxr-x--x 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```

## 8-James_Bond
This script sets the permission to the file hello as follows (without using commas) : No permission at all for owner and group, all permissions for other users.

Example:
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:40 8-James_Bond
-rwxr-x--x 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./8-James_Bond 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:40 8-James_Bond
-------rwx 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```

## 9-John_Doe
This script sets the mode of the file ```hello``` as follows : ```-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello```

Example:
```
