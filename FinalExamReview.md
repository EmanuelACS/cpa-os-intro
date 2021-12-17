# Review

## CHECKS
- MVS: Multiple Virtual Storage
- TSO: Time Sharing Option
- ISPF: Interactive System Productivity Facility
- Mainframes first programming languages: COBOL ASSEMBLY FORTRAN LISP
- ISPF navigation: https://www.ibm.com/docs/en/zos/2.4.0?topic=ismf-navigating-through-functional-panels
- ISPF editor commands: https://sites.google.com/site/indusitfactory/tso-commands
- JCL: Job Control Language
- Common JCL statements and their column locations: https://www.ibm.com/docs/en/zos/2.3.0?topic=statements-jcl-statement-fields
- Submitting a job and viewing the output of jobs that have been submitted
    - Submit: Command===> SUB + enter + letter
    - View: Command===> =sd.h + S to view job

## Know
- Scroll (PAGE HALF 1 2 3 X)

- Delete
a.	D on its own will delete the line cursor is at
b.	DD will create a delete block and then place DD to end block
c.	Dx will delete x amount of lines

- Copy
a.	C / CX Copy x lines
b.	CC will create a copy block and then place DD to end block
c.	Cx will delete x amount of lines
d.  use A / B for after / before paste

- Insert
a. I / Ix Insert x lines

- Move
a.	M / MX Move x lines
b.	MM will create a move block and then place MM to end block
c.	Mx will delete x amount of lines
d.  use A / B for after / before move

KC03A0D.COMP1081.CNTL(HAPPY)
_User_ . _DataSet_ . _Type_ . _Member Name_

- Enter the command(s) to copy a member called “QUIZ” at the bottom of the member being edited. “QUIZ” which exists in the same PDS as the member being edited
> Because member is not empty, put an A or B in the prefix area
Command => COPY'KC02132.COMP1081.CNTL(QUIZ)'

- F8 to scroll down x amount (specified)
- Exec statement is refferred to as a job step

>Example
```
000006 //COPY     EXEC PGM=IEBGENER                                           
000007 //NEWFILE  DD DSN=KC02132.COMP1081.COLIN.HAPPY,                        
000008 //             DISP=(NEW,KEEP,DELETE),                                 
000009 //             DCB=(LRECL=256,BLKSIZE=512,RECFM=FB),                   
000010 //             SPACE=(512,10)                                          
```
-> Execute job step using the dd statement
    Job Step Name -> COPY (can use as a reference variable later on)
    EXEC -> IEBGENER (Program that will be ran)
    DD -> Creating this new dataset called happy

## Datasets
> Files is z/os are known as datasets
- SDS and PDS appear the same to the z/OS, users can't tell either
    - by just looking at the name
    - member always in () after the type qualifier 
    - must be 8 chars long and start with a letter

### Sequential Datasets
- Bunch or records one after another
- Have to read preceding records before getting to the one you want

### Partitioned DataSets
- Like having a directory with files inside of it
- A dir + one or more members
- PDS - referred to as a library
- No subdirectories
- Each member acts as a Sequential DS, having to read each line of a member to get to a specific one you are looking for

### General info
- Min allocation of a DS: one track on a disk
- Small files waste a lot of space if stored in a SDS

### Naming conventions
- High level qualifier (ur user ID)
- User Determined Qualifier 
    - (Designates the type of data or application that is served by the DS)
- Type of Data (i.e ASM CNTL COBOL DATA EXEC LOAD OBJ PLI TEXT CLIST LOAD) i.e extensions
> Separated by a . 
> i.e COMP1081.FALL2013.DATA
> i.e KC03A0D.COMP1081.DATA

### Management of the PDS
- Created and organized by OS
- Used to access individual members
    - Only name of the member is required
- Types will be separated (but same high level qualifiers)
    - Since programmers like using the same name
- The ISPF Editor can default to a convenient screen when editing JCL script or COBOL source code

### ISPF
- View member: 1
- Edit member: 2

### View Entry Panel
- High level qualifier (ur userID)
- User determined qualifier
- Type 
- Member name

### PDS Members
- After you select member to display, browse panel displays the first 22 lines of data
    - F8: move forward thru file
    - F7: moves you back (upwards) thru file
    - Not permitted to edit the member






## Extra Review 
- Max num of characters for each qualifier in a dataset name: 8
    - (Qualifier = things bettween the dots (i.e KC02132.COMP1081.CNTL are all qualifiers))
- JCL must end with a NULL statement // 
- Operation field (eg JOB EXEC DD) beings in column: 12
- Only system can tell if data set is partitioned, cannot tell from dataset name
- Identified a job and supplies accounting information: JOB (i.e where we're gonna run it)
- ISPF: Interactive System Productivity Facility
- JCL TSO ISPF (memorize)