# Programs and Processes
```
$ yum list * // all or ? s t f
$ yum list available
$ yum search tree
$ yum remove tree
$ yum install tree
$ yum upgrade tree
$ init // all programs come from init
$ ps 
$ ps -u
$ top (h help k kill q quits r changepriority s updaterate P displaybycpuusage M sortbymemoryusage)
$ cd var/log
$ tail messages
```

# Test Review
```
ps pre/top
ps -u
```
> Test 2 Review Sheet

1) e (/etc/passwd)
```
// Each line of this file gives us information about all users
$ cat /etc/passwd 

// Know what each of the following means
(i.e) clin:x:1000:1000:colin:/home/colin:/bin/bash
```

3) c (top)
```
// Both work
$ top
$ ps 
```

4) b (init)

5) c (/var/log)
```
// Have to know
$ ls /var/log
...
yum.log
messages.log
boot.log
```

6) c (yy)
```
// Must know how to get around vi/vim
```

7) c (tail)
```
$ tail -5 FileName
```

8) c (%s/Hello/Bye/g)
```
// Have to know how to write these out
// :s only searches on one line, add /g to search all not just first
:s/search/find/g
// %s means search all lines
%s/Hello/Bye/g
```

9) b (dd)

10)
```
vi
nano  // know how to save and exit in nano
gedit
pico
```

11)
```
// Know how to write scripts in bash

#!/bin/bash // Identifies file as a script
```
```
a) Store the next user input provided into a new variable: 

read name // DON'T use $ when assigning variable a value
// read says take user input and store it in that variable
```
```
b) Write a function that will print "hello" to the terminal followed by the first parameter passed to the function

// function keyword is optional, () identifies keyword as a function
// never put anything in the ()
function hello() 
{
    // Using quotes is optional
    // $1 is the first param passed in the function
    // created automatically for us
    // i.e Echo "hello $1 is a $2 $3"
    Echo hello $1 
}
```
```
c) Call the function from step (b) passing it the variable created in step (a)
hello $name lab
// echo $1
```

100) Call script and pass word friday
```
// friday will be stored in $1 as first param
./testScript friday
> hello friday lab
```


101) FULL SCRIPT
```
#!/bin/bash // Identifies file as a script
read name
function hello() 
{
    // i.e Echo "hello $1 is a $2 $3"
    Echo hello $1 
}
hello $name lab
```

102) While loop
```
while [ $cost < 100 ]
    do 
        echo "testing over 100: $cost"
        read $cost
    done
```

103) If statement
```
if [ $abc = $name ]
    then 
        echo "correct! $name"
    else 
        echo "good try! $abc"
fi
```

103) Add user
```
useradd userName 
```

104) where is user's mail directory
```
/var/maik/userName
```

105) Check login status
```
who
```

106) Change user passwd as root
```
passwd userName
```

107) modify user
```
usermod userName
```

108) delete user
```
userdel userName
```

109) check identity
```
whoami
```

110) Assign user for different groups
```
usermod -a -G groupName userName
```

1) manage group
```
groupadd myGrp
groupmod -rwx myGrp
groupdel myGrp
```

2) users home dir
```
/etc/passwd
```

3) group info
```
/etc/group
```

4) log files
```
/var/log
```

5) find passwords
```
/etc/shadow
```

6) view top processes
```
top (P for cpu M for memory)
ps 
```

7) check if file exists
```
if [ -s /tmp/file ]
    then 
        echo "yes"
    else
        echo "no"
fi
```