Every file has an owner, a group, and a list of permissions for others.
root users have superadmin, which overrules all permissions. 
Owner of a file can also change the permissions of that file
Write allows write to dir, create, delete or rename 
Execute (x) is needed to run files
Symbolic links should always have 777 perms

## Permissions
File type code | owner permissions | group permissions | World Permissions 
       -            r w x                 r - x                 r - -
r = read (4)
w = write (2)
x = excecute (1)
- = does not have that permission (no value)

if total = 7, Owner rwx
if total = 5, Group r-x
if total = 4, Other r--

File Type Codes:
- = Normal data file
d = Directory
l = Symbolic Link
p = Named pipe
s = Socket
b = Block device
c = Character device

Adding perms
u = owner
g = group
o = other
a = all categories
- = remove perm
+ = add perm

Settings
"umask"
    - Used to set default perms to new file
    - umask command without args displays the current default 
    - current default shows what perms have been removed
        i.e 0022 means 0 perms removed from owner, 2(w) removed from g, 2(w) removed from other
    - umask perms // will change the default perms 

```
// Check users
$ cat /etc/passwd
// Change owner of file
$ chown user filename
// check perms
$ ls -l filename
-rw-r--r--. 1 root root     0 Sep 28 08:46 file1  // would be represented as 644
// change group                                                      // ^
$ chgrp grpname filename                                             // |             
// Change file perms                                                 // |
$ chmod perms file                                                   // | for perms
// Perms can also be like:
$ chmod u+w file (add write to owner)
$ chmod u-w,g-w,o-w file (remove write for all)
$ chmod g+rwx file (add rwx to group)



```