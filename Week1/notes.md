## Commands
```
// shows path to current directory
$ pwd

// show help for command
$ man <command>

// show files
$ ls  // use -a to show hidden files too

// check command
$ whatis <command>

// chmod, passwd 
// enter q to quit from man pages
$ man 5 passwd

// relative path vs absolute path
// pwd gives absolute path
<<<<<<< HEAD
// ~ is root
// ./ is current dir

// echo used to write to files fast
$ echo "info to write" > fileName

// cp make a copy for fileA named fileB at path
// -i to ask before overwriting file if exists
// -p preserve ownership
// -R recursive copy
$ cp fileA path/fileB

// mv can be used to move or rename a file/dir
// path is optional, to move, otherwise it will be renamed
$ mv fileName path/fileRenamed

// links
// hard link vs symbolic link
// hard link is a dupe entry (copy of a file basically)
// soft link points to file name which points to address in memory // i.e shortcut
// ln creates a link
$ ln fileA hardLink

// rm removes file
// -r recursive
// -f force delete 
$ rm path/fileToRemove

// wildcards
// ? stands for single character
// * stands for any set of characters (including no chars)
// [a-z] or [abc...xyz] stands for any character of the ones specified 
$ ls f??t
$ ls f*t
$ ls b[ao][lo]?s
$ ls b[A-Z]ok

// mkdir makes directory 
// -p create parent directory first then child
$ mkdir dirName
$ mkdir path/dirName
$ mkdir -p parentName/childName
