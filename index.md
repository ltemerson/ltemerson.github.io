# Welcome to 274 Notes

Here is a summary of all commands neederd to for the [274 midterm](https://kellyn-larson.github.io/midterm-review.txt).

# Text Editors (Vim)

### exit without saving
 ```markdown
1. If you are currently in insert or append mode, press Esc.
2. Press : (colon).
3. Enter q!
```
### save without exiting
 ```markdown
1. If you are currently in insert or append mode, press Esc.
2. Press : (colon).
3. Enter w
```
### save and exit
 ```markdown
1. If you are currently in insert or append mode, press Esc.
2. Press : (colon).
3. Enter wq
```
### copy(yank), delete, and paste

#### copy and paste
 ```markdown
1. Place the cursor on the line you want to begin cutting.
2. Press V to select the entire line, or v to select from where your cursor is.
3.  Move the cursor to the end of what you want to cut, using h,j,k, or l
4.  Press y to copy it, or d to cut it.
5.  Place the cursor where you would like to paste your copied stuff.
6.  Press P to paste it before your cursor, or p to paste it after the cursor.
```

#### delete
 ```markdown
```

# Terminal Basics

### Understand info displayed on bash prompt
 ```markdown
Example:    jmcnabb@isengard:~/Desktop$
                 ^      ^           ^
             username  hostname   Working Directory
```
### File Navigation
```markdown
cd: Change directory
    ex: cd /Desktop/274
pwd: Print Working Directory
    ex: pwd     
        output: ..../jmcnabb/Desktop
ls: list segments
    ex. ls
    output: All files and folders within the current working directory
```
### Meaning of ~, ., and ..
```markdown
~  : Known as the metacharacter and represents the home directory.
         It is the equivalent of /home
.  : It has several meanings listed below.
         1. In a pathname it means the current "working directory (./filename)
         2. As a prefix to a filename, it causes them to be hidden (.filename)
         3. It is a synonym for the source command (. execfile) :: Note the space
..  : Represents the parent directory of the current "working directory"
```
### Importance of Capitilization
```markdown
Capitilization is really important! 
Unlike windows, you can have the exact same file name with different cases.
```
# Commands

### ls and its -a and -l options
```markdown
ls: list segments
    Shows all segments in the current directory
    segments include things such as files and folders
```
###### -a
```markdown
list all files including hidden file starting with '.'
ex: ls -a
```
###### -l
```markdown
list files with long format

shows file or directory, size, modified date and time, 
file or folder name and owner of file and its permission.

ex: ls -l
```
### cp and its -r option
```markdown
cp
  makes copies of files and directories.
```
###### -r
```markdown
-r
  makes copy recursively
```
### wc and its -c, -w, and -l options'
```markdown
Prints newline, word, and byte counts for each file
```
###### -c
```markdown
-c
  prints byte count
```
###### -w
```markdown
-w
  prints word count
```
###### -l
```markdown
-l
  prints the newline count
```
### rm and ```its -r option
```markdown
Removes the file, not directories
```
###### -r
```markdown
-r
  Removes directories and their contents recursively
```
### bash and its -e and -x options
```markdown
Executes commands read from a file or standard input
```
###### -e
```markdown
-e
  Exits immediately with a non-zero status
```
###### -x
```markdown
-x
  Prints all executed commands to the terminal
```
### mkdir and its -p option
```markdown
Makes a new directory
EXAMPLES
~/myfiles
  Creates directory myfile in home directory
mkdir -p /home/hope/Documents/pdf
   Creates the directory /home/hope/Documents/pdf. If any of the parent 
   directories /home, /home/hope, or /home/hope/Documents do not already 
   exist, they will automatically be created.
 ```
###### -p
```markdown
-p
  Creates nested directory if they don't exist
```
### tar and how to extract (-xvf) archived files and create (-cvf) archived files
```markdown
tar is used to create, maintain, modify, and extract files that are in tar format
```
###### -xvf
```markdown
-xvf: use 'tar -xvf file_name.tar'
```
###### -cvf
```markdown
-cvf: use 'tar -cvf  file_name.tar
```
### rmdir
```markdown
Removes empty directories from the file system
```
### pwd 
```markdown
Prints directory you are in
```
### mv
```markdown
moves or renames files
EXAMPLES
mv myfile.txt myfiles ////// moves myfile.txt to myfiles
mv myfiles myfiles2 ////// mpves myfiles into myfiles2
```
### cat 
```markdown
Reads data from files
EXAMPLES
cat mytext.txt ////// Reads the content of mytext.txt
cat mytext.txt > newfile.txt ////// Will put contents of mytext.txt into newfile.txt
cat mytext.txt >> another-text-file.txt ////// Appends instead of overwriting
```
### echo 
```markdown
Displays text
```
### touch
```markdown
Creates an empty file
EXAMPLE
touch file.txt ////// Creates file.txt
```
### file
```markdown
file *

    Below is an example of what may appear when running file with a wildcard for all files:

    shutdown.htm: HTML document text
    si.htm: HTML document text
    side0.gif: GIF image data, version 89a, 107 x 18
    robots.txt: ASCII text, with CRLF line terminators
    routehlp.htm: HTML document text
    rss: setgid directory

file *.txt

        running the file command listing     any file ending with .txt:
```
### find e
```markdown
Searches for files 
```
# Variables
```markdown
Can only contain letters,numbers, or the underscore character
EXAMPLE
NAME="Lucas Emerson"
echo$NAME
```
### Different ways to set and see contents of shell variables
### '' vs ""
```markdown
Single quotes will literally echo what you have between them
double quotes will evaluate variables between them and output the value of the variable
```
### Curcly braces in variables
```markdown
Braces are used to unambiguously identify variables
```
### echo with unset variable?
```markdown
unset var
echo $var
```
# Wildcards

### *, ?, and the many ways to use []
and ?:
```markdown
Wldcard allows you to specify more than one file at the same time. 
The '*' matches any number of characters. For example, if   you want to execute 
a command on all files in the current directory, you would specify '*' as the filename. 
If you want to be more selective and match only files which end in "ing", you 
would use "*ing". Note that the '*' can even match zero characters, so "*ing" would match 
"ing" as well as "sing".

The other wildcard, '?', is not used very often, but it can be useful. It matches exactly 
one character. For example, if you want to match "sport", but not "spat", you would use 
"sp??t". The first '?' matches the 'a' in "spat", but the second '?' can't match anything, 
so "spat" fails.
```
[] :

Square Brackets Wildcard
```markdown
The third type of wildcard in shell commands is a pair of square brackets, which can represent 
any of the characters enclosed in the brackets. Thus, for example, the following would provide 
information about all objects in the current directory that have an x, y and/or z in them:

    file *[xyz]*

And the following would list all files that had an extension that begins with x, y or z:

    ls *.[xyz]*

The same results can be achieved by merely using the star and question mark wildcards. However,
it is clearly more efficient to use the bracket wildcard.

When a hyphen is used between two characters in the square brackets wildcard, it indicates a 
range inclusive of those two characters. For example, the following would provide information 
about all of the objects in the current directory that begin with any letter from a through f:

    file [a-f]*

And the following would provide information about every object in the current directory whose 
name includes at least one numeral:

    file *[0-9]*

The use of the square brackets to indicate a range can be combined with its use to indicate a 
list. Thus, for example, the following would provide information about all filesystem objects
whose names begin with any letter from a through c or begin with s or t:

    file [a-cst]*

Likewise, multiple sets of ranges can be specified. Thus, for instance, the following would
return information about all objects whose names begin with the first three or the final three 
lower case letters of the alphabet:

    file [a-cx-z]*

Sometimes it can be useful to have a succession of square bracket wildcards. For example, 
the following would display all filenames in the current directory that consist of jones
followed by a three-digit number:

    ls jones[0-9][0-9][0-9]
```

### Be able to tell what a specific wildcar will match given the files/directories in the current working directory

# Basic Bash Scripting

### Command line arguments
```markdown
$0
 The command or script
$1 to $9
 Arguments 1-9
$#
 Total number of arguments
$*
 Represents all arguments
$$
 PID of a running script
```
### Descripe what script does
```markdown
A command script is simply a file, which contains a set of normal linux commands that the command shell will perform automatically in the given order
```
### Write a simple script
```markdown
#! /bin/bash
echo "Hey what's Your First Name?"
read a
echo "welcome Mr./Mrs. $a, would you like to tell us, Your Last Name"
read b
echo "Thanks Mr./Mrs. $a $b for telling us your name"
echo "*******************"
echo "Mr./Mrs. $b, it's time to say you good bye"
```
### How while-loops are structured
```markdown
INPUT_STRING=hello
while [ "$INPUT_STRING" != "bye" ]
do
  echo "Please type something in (bye to quit)"
  read INPUT_STRING
  echo "You typed: $INPUT_STRING"
done
```

# I/O Manipulation/Redirection

### Using the echo command
### <, >, >>, 2>, 2>>, and |
```markdown
>
 Standard output, overwrite
<
 Standard input, overwrite
>>
 Standard output, append
2>
 Standard error, overwrite
2>>
 Standard error, append
1|2
 Feeds output from left program to the program on the right

```

# Misc

### Exit Status, $?
```markdown
To view the exit status use"
echo $?

To change exit code, as the end of the if or else statement put:
exit#
```
### Control Signals (Ctrl-C, Ctrl-D)
```markdown
Ctrl-C
 Interrupt/stop what you are doing. Terminates application
Ctrl-D
 Exits terminal 
```
