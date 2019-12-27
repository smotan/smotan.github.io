---
layout: default
---
## In general
The course was about using command-line environment for useful linguistic tasks. The course is given at the University 
of Helsinki.

Week | Commands I've learned
--- | ---
 1 | `ls`, `cd`, `wget`, `less`, `cp`, `mv`
 2 | `rm -r`, `chmod`, `kill`
 3 | `head`, `tail`, `dos2unix`, `unix2dos`, `tr`, `tr -d`, `cat`, `wc`, `wc -l`, `egrep`
 4 | `uniq -c`, `sort`, `sed`
 5 | `export`
 6 | `make`, `su`, `sudo`, `pip install`, `apt-get install` 
 7 | `git add`, `git commit -m`, `git push`, `git pull`, `git merge`

## Week 1
The commands included in this week are `ls` for listing the content of the current directory, 
`cd` for changing directory, `wget` for getting the content from the internet, `less` for displaying
a text file, `cp` for copying files and `mv` to move or rename files.<br>
I learned to fluently use the command line for basic tasks.

## Week 2
This week contained three parts:
- the first part was about copying, moving and removing the directories. It was also mentioned
what standard system directories are present in UNIX systems.
- the second part was about processes and process management using the command line
- the third part was about working on a remote server using ssh

For example command
```
chmod a+r filename
```
adds read permissions for the file filename without changing write and execute permissions.<br>
Command
```
kill pid
```
kills the process with the given PID.<br>
I learned how to find the PID of a process and kill the process, change permissions and work on directories. I can run commands in the background and move a process to the background.

## Week 3
This week contained two parts:
- first part was about different encodings, converting between them and commands for text processing
- the second part was about formatted text files, i.e. CSV (comma seperated values) or TSV (tab seperated values) files.

Command
```
head file.txt
```
shows first 10 lines of file.txt.<br>
Command
```
tail file.txt
```
shows 10 last lines of the file.<br>
Command `cat book.txt | tr -d '\r'` is equivalent to the command `dos2unix book.txt`. The commands translate a file
from Windows to Unix format. This is because lines in Windows text files are ended with `\r\n` and in Unix text files
just with `\n`.<br>
I learned also to use pipeline to redirect the output of one command to another and the greater-than sign to redirect the output to a file. I learned also commands `tr`, `wc`, `wc -l` and `egrep`.

## Week 4
This week was about more advanced processing of text files, using pipelines to combine commands. The command `sed` was introduced.<br>
For example the command
```
cat file.txt | tr -s '\n\t\r ' '\n' | tr -dc "A-Za-z0-9'\n" | sort | uniq -c | sort -nr
```
forms a frequency list from the file file.txt.<br>
The command
```
tr 'A-Z' 'a-z
```
translates all uppercase letters into lowercase letters.

I learned to generate a frequency list and sentence per line format from a text file. I also learned more about regular expressions. I learned also how to generate a list of n-grams from a text file. 


## Week 5
This week was about scripts and environment variables. Scripts are files ended by convension with `.sh`. We can use them to write a series of commands to perform some more complex tasks. Then we can execute them by typing the path to the script and the name of the script. This allows us to perform more complex tasks easily, without having to type a lot of commands every time.<br>
For example we can run a script myscript.sh located in our current directory with the command
```
./myscript.sh
```
I learned how to write a simple script. I also created my own .bashrc file to customize my command prompt.

## Week 6
This week was about installing programs and package managing programs. Package managing programs track all the dependencies that are needed to install a program. With them we can easily install a program, without having to look that all the dependencies are also installed. One of the package managing tools is apt-get.<br>
The second part was about becoming a root user, `su` command for changing the user and `sudo` command to run a command as a root user.
It was also told about creating a python virtual environment.
For example the command
```
sudo apt-get install programname
```
installs the program programname and all the required dependencies.

I learned to install programs using apt-get and python packages using pip. I can run commands as a root user and I set password for root.

## Week 7
This week was about version control using Git and Github. Git is a tool that allows us making changes to the files with a possibility to come back to a previous version. It is commonly used in projects developed by more than one person.

![git commit](https://imgs.xkcd.com/comics/git_commit.png)

I learned to create a repository on Github and clone it to my own computer. I learned to create new branches, switch between branches, merge a branch with the master branch and delete a branch. I also learned to revert a previous commit.
