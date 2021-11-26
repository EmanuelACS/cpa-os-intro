## JCL FILES
All JCL files start with //
Arguments must be separated by a coma
Comments: //*
- JOB (what job to do), JobName must be ur userID 
- EXEC (program to execute), ExecName made up, allows you to identify them
- DD (What datasets do we need to run this program)

### Memo: 
First Forward slash always begins at line 1 (/)
Name field always starts at column 3 (ur id)
Job always starts at column 12 (same as exec and dd)
Params always start at column 16, except for first param which is speartated by one space
Must end script with null statement (//) only last line 
Run script: Command==> SUB - sbumits job field to get executed, type in A (identifier)
Command==> =SD.H (allows u to see all jobs submitted) 
Put an S underneath the one you want to view 
