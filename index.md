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
Determines a files type
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
### Curcly braces in variables
### echo with unset variable?

# Wildcards

### *, ?, and the many ways to use []
### Be able to tell what a specific wildcar will match given the files/directories in the current working directory

# Basic Bash Scripting

### Command line arguments
### Descripe what script does
### Write a simple script
### How while-loops are structured

# I/O Manipulation/Redirection

### Using the echo command
### <, >, >>, 2>, 2>>, and |

# Misc

### Exit Status, $?
### Control Signals (Ctrl-C, Ctrl-D)
