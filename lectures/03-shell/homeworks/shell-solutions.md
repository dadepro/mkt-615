### Part I: write the commands needed to...

- make a directory called first `mkdir first`
- change directory to the first folder `cd first`
- create a file called person.txt `touch person.txt`
- change the name of the file to another.txt `mv person.txt another.txt`
- make a copy of the another.txt file and call it copy.txt `cp another.txt copy.txt`
- remove the copy.txt file `rm copy.txt`
- make a copy of the first folder and call it second `cp -r first second`
- delete the second folder `rm -rf second`

### Part II: answer the following questions


- What does the man command do? Type in man rm. How do you scroll and get out? **The man command lists the manual for a command**
    **- D or Control ⌃-D to advance half a page**
    **- B or Control ⌃-B to go back one page**
    **- U or Control ⌃-U to go back half a page**
- Look at the man page for ls. What does the -l flag do? What does the 
`-a` flag -do? **The `-l` flag lists files in a list format with more detail and the `-a` lists all files and folders including hidden ones**
- Type the following command: `curl https://www.google.com` > google.html What does the command do? **Download and save the contents of google.com**
- Use less (a command line utility that displays the contents of a file or a command output,) to look at the contents of google.html. Look at the man page for less. Read the section on /pattern. What is the command to search for the text hplogo in the google.html file? `less -p hplogo google.html`
- How do you jump between words in the terminal? `option left/right`
- How do you get to the end of a line in terminal? `control + e`
- How do you move your cursor to the beginning in terminal?  `control + a`
- How do you delete a word (without pressing backspace multiple times) in -terminal? `option + delete`
- What is an absolute path? **An absolute path is a path that starts from the root route and gives the complete location for a file or folder**
- What is an relative path? **A relative path is a path that starts at the current location and not the root route**
- What is a flag? Give three examples of flags you have used. **A flag adds additional functionality to an existing command, we have seen `-a` and `-l` for the `ls` command and `-r` for the `cp` and `rm` commands**
- What do the r and f flags do with the rm command? **`r` will remove folders and recursively go through each folder and file and `f` will force removal**
- How do you list all processes running on your machine? `ps -ax`
-  What is a PID? **A unique identifier for for a process which is necessary when stopping a process**
-  How do you terminate a process? **You can use `kill` or `kill -9`**
-  What is the difference between `kill` and `kill -9`? **9 is a specific signal ensures that the command can not be ignored, whereas without the -9 there may be processes that are not killed by using `kill` alone.**
-  What `grep` flag allows for case insensitive search? `-i`
- What `grep` flag allows for full word search? `-w`
- What `grep` flag shows you the line number of a match? `-n`

### Part III: Find and Grep

Write the following terminal commands to do the following (assume that `instructors.txt` is an imaginary file):

- Find all files inside the `Desktop` folder that have a name of "learn." `find ~/Desktop -name "learn"`
- Find all files inside the `Desktop` folder that start with a "P." `find ~/Desktop -name "P.*" `
- Find all files inside the `Desktop` folder that end with `.txt`. `find ~/Desktop -name "*.txt" `
- Find all files inside the `Desktop/views` folder that have the name `data` somewhere in their filename. `find ~/Desktop/views -name "*data*" `
- Inside of the `instructors.txt` file, output the number of times the word "Elie" appears. `grep -c "Elie" instructors.txt`
- Inside of the `instructors.txt` file, list all matches for any full word that starts with a capital "P." `grep -w "P.*" instructors.txt`
- Inside of the `instructors.txt` file, list all the line numbers for any full word that starts with a "z" (it should match regardless of upper or lower case). `grep -ni "z.*" instructors.txt`
