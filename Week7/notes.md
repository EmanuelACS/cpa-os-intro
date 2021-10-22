### VI 
```
$ vi filename
$ chmod a+x filename
```

### Bash scripts
```
#!/bin/bash
echo "Script, output to console"
esc + :wq (quit and save)
```

### Lab Script
```
#!/bin/bash
echo "Script test"
rm *$1*  // first input
week=$2 // when assigning values you omit $ for vars
if [ $week = "break" ] // when accessing vars, add $
then 
    echo "Breaking out."
fi