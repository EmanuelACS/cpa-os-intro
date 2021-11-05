```
$ cat /etc/group    // displays all dif groups 
$ groupadd grpName  // creates gorups
$ cat /etc/passwd   // displays all dif users' information
// grpName:x:0000:groupAssociation   // check the group association
$ usermod -G groupName userName // allows to change group user belongs to      // overwrites      
$ usermod // allows you to change user 
$ usermod -aG groupName userName // appends (-a) to group
```