# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

* show current working directory path ---> `pwd`
* creating a directory ---> `mkdir <directory name>`
* deleting a directory ---> `rm -r <directory>`
* creating a file using `touch` command ---> `touch <file name>`
* deleting a file ---> `rm <file name>`
* renaming a file ---> `mv <old name> <new name>`
* listing hidden files ---> `ls -a`
* copying a file from one directory to another ---> `cp <file source> <destination>`  
* **Print to terminal** ---> `echo <text>`
* **Search for something** ---> `grep <expression>`
---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls` ---> list files in current directory  
`ls -a` ---> list all files in current directory including hidden  
`ls -l` ---> list detailed info of all files  
`ls -lh` ---> list detailed info of all files with sizes as 'human readable' sizes  
`ls -lah`---> list all files with detailed information and human readable sizes including hidden  
`ls -t`  ---> list all files sorted by time modified  
`ls -Glp` ---> list all files with color coding and details and '/' at the end  


---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

`-u` ---> list in order of last access
`-r` ---> reverses the ordering

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

`xargs` is a bit like using a loop. You can pass in multiple arguments and execute the same command for each one.

Example:

If I want to delete files with certain extensions, this would let me do it all at once. (Obviously being sure to double check what directory I'm in first):

`find . -name '*.py' | xargs rm`

 

