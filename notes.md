# ITS A UNIX MACHINE!

- command + space brings up spotlight
- when exiting terminal, type exit
- `^d` also exits
- `^` = control

---------

- `unix` = grandfather
- `bsd` - became mac os
- `linux` - more popular
- theres many distributions of linux
- ubuntu, arch, debian, fedora

- ubuntu is based on debian, (ubuntu) which is currently the most popular distribution.  I'm installing a specific version which is 18.04 release.  which is the 4th month of 2018.

- why so old?  It's because it's stable.  ubuntu calls these LTS's which is long term supports.

- Every one has a code name, which is some kind of adjective + animal.  This one is bionic beaver.  i.e. Mega Bidoof.

---

- `^alt+t` - command terminal for ubuntu

- `^d` exits

- `^v` is past inside ubuntu, but you can `command + c` to copy

- `^shift+T` - creates a new tab inside the terminal 

- `cmd + t` - the above but for mac terminal

- `^r` - does a reverse search.  start typing what you did above and it will tab it for you.

- i can shut it down like a normal thing

- only short options work on MACOS terminal i.e. `-h`, `-a`, etc. because mac is garb.

- on gnu you can use long options i.e. `--help` or `--force`. muy bueno

---

WHAT IS MEANT BY A TERMINAL?
---------------------------

- terminal is short for "terminal emulator"

- the original idea is that you used to connect to a mainframe machine and used a dialed in connection, that connection was called a terminal.  We no longer have mainframes, so we have a emulator.

- i used "terminal" on macOS.  and i used "gnome terminal" in ubuntu.  

- it will run a "shell", which we're sticking to the most basic shell.  on macOS it's called "bash" which is short for "bourne again shell".  In ubuntu, it's "dash" which is running in "bash emulation mode"

- other common shells are "sh" which is the most basic shell, but it sucks.  Another one is "zsh" and it has a lot of nice features.  Another one is "fish" it has some features, its buggy and kinda weird.

- you can refer to either as "bash" and people will know.

- theres other terminal emulators, but we're going to use the defaults.  the better one on mac is "iterm" 

---

- `~` is short for the home directory

- `~[username]` is also short for the home directory.

- pressing up copies the previous line

- `.` refers to current directory
- `..` refers to the directory above

---

- `$?` -shows the exit code of the previous command

---

- `ls` shows what files and directories exist on a path.  by default, it uses the current path.

- 1st note: FILES ARE CASE SENSITIVE ON LINUX

- `ls Desktop` would be proper.

- `ls -a` : it shows a little more with "hidden files".  by convention, files that start with a . are hidden.

- `ls -l` : it shows the mode, owner, user, and creation time of directories and files.

- `ls -a -l` : combines the two

- (`ls -al` also works) (short opts)

- `ls -h` - shows file sizes as readable sizes i.e. 1K, 100M, 24G

- `ls --help` (only on gnu systems)

- `--help` will work less of the time on MacOS because its shit

---


- `cd` stands for change directory.  if no arguments, it goes to the default directory.

- `cd Desktop` would take you to directory of Desktop

- `cd -` (goes back to previous directory)

- `cd + Tab` (lets you tab to directories)

---

- `pwd` (present working directory) - it prints out what directory you're in.

---

- `rmdir` (removes directories if they are empty)

- `mkdir` (creates directories if they do not already exist)

- `mkdir -p` (doesn't error if it already exists) (it creates parent directories so it lets you add (or destroy) multiple at once)

- for mkdir/rmdir -p, it is "idempotent" meaning that when you perform an action, it will always end up at the same state, or if you run it twice, it won't do anything the second time but it will succeed.


---

- `echo` - prints all of its arguments i.e echo "Hello World"

- single quotes also work, like in Python.

- you can use \" to write in double quotes into what is printed.

- you can also use ' " to write double quotes into what is printed.

- `echo' -- help will print that, so it doesn't quite work like that.

- `-n` will make it not print a new line afterwards

- `-e` allows it to interpret backslash escapes as different values

- `\t` creates a tab (must have -e)

- `\n` create a new line (must have -e)


---

- `man` opens a "pager" which displays the manual page, so if you put it in front of a command, it will give detail about that command.

- quit pagers by typing `q`

- `/` and a string, it searches inside.  n goes to the next thing.  `shift + n` goes to the previous thing.

---

- redirection allows you to send the outputs of commands and put them into files or other commands.

- `cat` - prints the contents of the files that are passed to it.  if there is no file, it will attempt to pass whatever is a standard input.

- `>` the left hand side gets written to the file on the right handed side

- `<` this takes what is on the right hand side and feeds it as input to the left hand side.

- `|` (a pipe) takes the output of left and feeds it as the input to right side.

- `>>` this appends to a file (it works kinda like the > before)

- `<<<` if the left is a command and the right is a string, the string now becomes the input of the command

- `^d` sends end of file

---

- `rm` - deletes things

- `-f`, `--force` ignores nonexistent files and arguments, never prompt

- `-r` removes directories and their contents recursively, so you can get rid of specific ones.  for instance, rm -r a/b/c will get rid of only 'c'

- `-v`, --verbose explains what is going on

- `-i` interactive mode


---

- `touch` - change file timestamps, or more importantly, creating empty files

---

- `yes` - output a string repeatedly until killed.

- kill it by ^c.  this works for everything.

---

- `cp` - copy files and directories

- `-R` `-r` `--recursive`  copies directories recursively, works like rm -r

---

- `mv` - move (rename) files 

- uses left to right

---

- `true` - do nothing successfully (returns 0 with $?)

- `false` - do nothing unsuccessfully (returns either 1 or 2 with $?)

---

- `&&` - takes a command on the left side and on the right side, and only runs on the right side if the left is successful

- `||` - takes a command on the left and right side, and only runs the right if the left is unsuccessful

- ';' - will run both commands no matter what

---

- in the highest directory `ls /` is a directory called `tmp`.  you can write files in here and they will be deleted upon restart

---

- `sleep` - delay or pause for a specified amount of time.  Suffix may be s (seconds), m (minutes), h (hours) or d (days), this will not work on mac

---

- `head` - outputs the first part of files, which is the first 10 lines to standard output.

- `tail` - outputs the last part of files, which is the last 10 lines to standard output.

- `-n # file` , shows however many lines you want

---

- `wc` -  prints new line, word, and byte counts for each file (in the order below).

- `-l`  `--lines` , print the newline counts

- `-w` `--words` , print the word counts

- `-m` `--chars` , print the character counts

- `-c` `--bytes` , print the byte counts

- `-L` `--max-line-length` , print the maximum display width

- you can also do something like this wc -l -w -m -c -L file | awk '{print $2" "$1" "$3" "$4" "$5" "$6}'
 to switch the order of the things.

---

- `sort` - sorts lines of text

- `-d` `--dictionary-order` , considers only blanks and alphanumeric characters

- `-f` `--ignore-case` , fold lower case to upper case characters

- `-n` `--numeric sort` , compare according to string numerical value

- `-R` `--random-sort` , shuffle, but group identical keys.

- `-r` `--reverse` , reverse the result of comparisons

- `shuf` - basically works like sort -R

---

- `tee` - read from standard input and write to standard output and files, copy standard input to each file and also to standard output.

- `-a` `--append` , append to the given file(s), do not overwrite

- echo $'hello\nworld' for example is one way to add lines to things.  usually | it into tee

---

- `apt` - this is a high level command line interface for the package management system.

- `apt-get` , it is also the package manager, but it's for scripts.

- `apt update` / `apt-get update` , need to do this before installing packages

- `apt install` / `apt-get install` , installs a package

- `apt remove` / `apt-get remove` , uninstalls a package

- `apt upgrade` / `apt-get upgrade` , will upgrade all packages*

- `update-manager` & will do the same thing, but in a nice graphical box.  muy bueno 

- you must add `sudo` before apt / apt-get in order to update

what is sudo?

- it basically works like "run as administrator" or in this case, a "superuser" but inside your terminal.  It lets you change basically anything.  BEWARE.

- `apt list [package]` lets you see if you have that package installed.


---

- `vim` - it takes a file name as an argument.  It's essentially a text editor.

- press `i` to enter insert mode

- press `esc` to exit insert mode

- press `:` to enter command-line mode

- press `:q` to exit

- press `:w` to write the file

- press `:wq` to write the file AND quit

- `dd` will delete a line

---

- `git clone [URL]` - makes a clone of a repository on github

- `git status` - shows the current state of the git repository

- `git add [file]` adds a file to staging area for git repository

- `git commit` - commits anything that is staged

- `git commit -m ['commit messages here']' standard practice to add a message

- `git push` - pushes current branch onto git repository

- `git show` - shows the commit that I made and what was done on it

- `git show <commit ID>`

- you can type the first unambiguous prefix, but first 4 digits is easy to remember

- master is the default branch name, you can use this too

- `git diff` - shows the differences in the tracked files

- `git add -u` , add any files that have been tracked before

- `git fetch` - retrieves meta data from the remote server

- `git pull` - it pulls in the changes from the remote branch

---




