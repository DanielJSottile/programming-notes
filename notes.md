# ITS A UNIX MACHINE!

- `command + space` brings up spotlight
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

- alt + # will switch between your tabs

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

- `!!` - a substitution containing the previous command

    - `sudo !!` for instance, works for if you need admin priviledges on a command.

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

- for `mkdir/rmdir -p`, it is "idempotent" meaning that when you perform an action, it will always end up at the same state, or if you run it twice, it won't do anything the second time but it will succeed.


---

- `echo` - prints all of its arguments i.e `echo "Hello World"`

- single quotes also work, like in Python.

- you can use \" to write in double quotes into what is printed.

- you can also use ' " to write double quotes into what is printed.

- `echo` -- help will print that, so it doesn't quite work like that.

- `-n` will make it not print a new line afterwards

- `-e` allows it to interpret backslash escapes as different values

- `\t` creates a tab (must have `-e`)

- `\n` create a new line (must have `-e`)


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

- `-r` removes directories and their contents recursively, so you can get rid of specific ones.  for instance, `rm -r a/b/c` will get rid of only 'c'

- `-v`, --verbose explains what is going on

- `-i` interactive mode


---

- `touch` - change file timestamps, or more importantly, creating empty files

---

- `yes` - output a string repeatedly until killed.

- kill it by `^c`.  this works for everything.

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

- `;` - will run both commands no matter what

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

- you can also do something like this `wc -l -w -m -c -L file | awk '{print $2" "$1" "$3" "$4" "$5" "$6}'`  to switch the order of the things.

---

- `sort` - sorts lines of text

- `-d` `--dictionary-order` , considers only blanks and alphanumeric characters

- `-f` `--ignore-case` , fold lower case to upper case characters

- `-n` `--numeric sort` , compare according to string numerical value

- `-R` `--random-sort` , shuffle, but group identical keys.

- `-r` `--reverse` , reverse the result of comparisons

- `shuf` - basically works like sort `-R`

---

- `tee` - read from standard input and write to standard output and files, copy standard input to each file and also to standard output.

- `-a` `--append` , append to the given file(s), do not overwrite

- `echo $'hello\nworld'` for example is one way to add lines to things.  usually `|` it into `tee`

---

- `apt` - this is a high level command line interface for the package management system.

- `apt-get` , it is also the package manager, but it's for scripts.

- `apt update` / `apt-get update` , need to do this before installing packages

- `apt install` / `apt-get install` , installs a package

- `apt remove` / `apt-get remove` , uninstalls a package

- `apt upgrade` / `apt-get upgrade` , will upgrade all packages

- `update-manager` & will do the same thing, but in a nice graphical box.  muy bueno 

- you must add `sudo` before `apt` / `apt-get` in order to update

what is `sudo`?

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

- `^` goes to the beginning of the line

- `$` goes to the end of the line 

- `shift + g` goes to the end of the file

- `[#] shift + g` goes to that specific number line

- `u` will undo.

---

- `git clone [URL]` - makes a clone of a repository on github

- `git status` - shows the current state of the git repository

- `git add [file]` adds a file to staging area for git repository

- `git commit` - commits anything that is staged

- `git commit -m ['commit messages here']` standard practice to add a message

- `git push` - pushes current branch onto git repository

- `git show` - shows the commit that I made and what was done on it

- `git show <commit ID>`

- you can type the first unambiguous prefix, but first 4 digits is easy to remember

- `master` is the default branch name, you can use this too

- `git diff` - shows the differences in the tracked files

- `git add -u` , add any files that have been tracked before

- `git fetch` - retrieves meta data from the remote server

- `git pull` - it pulls in the changes from the remote branch

- `git checkout <source> -b <branchname>` - create a new branch from the source named `<branchname>`

    - `<source>` is almost always origin/master, `<branchname>` can be whatever you want as long as it isn't master.

- `git branch` - it lists the local branches

- 'git checkout <branchname>` will switch branches

- `git branch --merged' shows all branches that are merged with master

- `git branch -d <branchname>` deletes that branchname



---

- `less` - is a pager.  Useful for viewing files nicely.

---

- `curl` - it downloads something from a URL.

---

- `dpkg` it does a lot of stuff, but it basically let's you see what is installed

---

- `grep` - print lines matching a pattern

    - `-E` - extended regex mode

    - `-i` - ignore case (makes it not case sensitive)
    - `-v` - inverts the match i.e. find what doesnt match
    - `-l` - print just the file names that match

    - `-L` - print just the file names that don't match

    - `-o` - only prints out the characters that match your pattern

    - `-q` - prints nothing, but makes the exit code match (will return 0)

    - `-r` - recursive matching mode, so it will recursively search through files and attempt to match

- a neat trick: `grep --color=always <pattern> <file> | less -R` will open a less that shows the color coded of the pattern.  neat huh?

- `^` matches the beginning of a string i.e. it finds something only at the beginning of a line.  the `^` is known as an anchor. is always put at the beginning.

- `$` matches the end of a string i.e. it finds something only at the END of a line.  also an anchor. since this is also a special character, we have to put 'single quotes$' around that. must always be at the end.

- `.` matches any character, i.e. it's a single character wildcard

- `*` is a repeat quantifier, meaning 0 or more. it's also a special character and requires `'single quotes*'`

- `\` it makes the character after it treated differently, most commonly used to disable special characters.  So if I wanted to search for a "." I would use `\.`.  this is also special, ironically, so it must be in 'single quotes'

- `+` it's like `*` but only 1 or more.  only available in extended regex mode (`-E`)

- `[...]` it finds ranges of characters i.e. `[A-Z]`.  They are another special character, so put single quotes around them.

- `(...)` it does nothing special on it's own, but can look for groups of works sort of like how `*` works on single characters.  is a special character and needs single quotes around it. it also needs -E.  for example, grep -E '( it)' [file] would find all instances of' it', and any instances that repeat ' it' 

- `|` allows you to pick one or the other, is often inside of parentheses, must use -E. also needs to be in quotes

- `{...}` inside is a number expression as a repeat quantifier; it works like `*` and `+` but you can choose how many repeats you are looking for.  needs -E and 'quotes'.  for example, `grep -E '0{2,}' [file}` will only look for '00', wheras 2,5 would look for a range of those amounts of characters.

- `?` matches 0 or 1 as a repeat quantifier.  needs -E. so basically matches with the character before it or without it.

---

- `which` - locates executables

	- `-a` - prints out all the matching pathnames matching the argument

- `$PATH` - an environment variable that contains where executables can be.  The contents of the variable are paths separated by :

---

- `type` - it shows you what provides it.

-  we made a personal bin directory and we put it on the PATH.  we used the export command, which is a bash built in which sets an environment variable.  

- `#!/usr/bin/env python3` - called a shebang, originally "hash bang", tells the os how to run an executable.  they are either 1 or 2 arguments, cant be more or less.  first has to be a full path.  it finds the path to python3 and runs it.

- `env` - runs a program in a modified environment.  running just env prints all environment variables.  if you run it with more than 1 environment, it takes this form `env VAR=value ... program arg arg`.  

- `chmod +x hello-world` - stands for change mode, it turns the file we made called "hello-world" into an executable file.  

- `export PATH="$HOME/bin:$PATH"` - $HOME and $PATH are environment variables and my shell substituted those variables into the export command.  This lets us move the $HOME/bin path into the begining of our home directory path.  then we put that into our bashrc (bash run commands) which runs whenever you start a shell.

- `source` - it runs the commands in a file as if you wrote them on your shell.  it has an alias `.` not the same as `.` the directory

- `venv/bin/activate` - it set the path with the venv bin to the front of PATH so we can mess around with python and not destory anything.  It also set the PS1 to venv as the shell prompt

- `pip` - is the package manager for python.  
	- `install` , `uninstall`, and `freeze` (which shows you what is installed) only useful option for freeze is `--all`

- `virtualenv` - a tool that makes a virtual python environment, takes -p [python version] and the directory, which you should put in the project you are working on and call it `venv`

- let's say I break my venv...

- `deactivate` - undoes the activate we did before (see above)

- `flake8` - is a linter for python; it finds formatting mistakes in your programming and suggests fixes.  It can find unused variables/assignments, etc.  run as `watch flake8 [file path]` in a different window.

---

- `watch` - execute a program periodically, showing output fullscreen

---

PYTHON!
-------

every script should end with this:

```python
def main():
   ...


if __name__ == '__main__':
    exit(main())
```

- it is akin to the int main in C++

---

STRINGS
-------

- there are 4 syntaxes for strings:

	- `'string'`
	- `"string"`
	- `'''string'''`
	- `"""string"""`

- the first two are normal, single line string literals.  You can put double quotes inside of a single quote string and vise versa.
- the triple quoted strings are multi line strings.  They preserve spacing and new lines like this:

```python
x = """
hello
world
"""

y = """
    hello
    world
"""

z = """\
hello
world
"""

print(x == '\nhello\nworld\n')
print(y == '\n    hello\n    world\n')
print(z == 'hello\nworld\n')
```
- notice how the `\` in the third example escapes the newline, making it not appear inside the string.

- as long as there isnt a triple quote inside of the triple string, you can use either `'` or `"` inside.

- conventionally, `"""` should be used for docstrings, which the various examplees are below: 

```python
"""
This is a docstring for the module
"""

class C:
    """this is a docstring for the class"""

    def meth(self):
        """this is a docstring for the method"""


def func():
    """this is a docstring for the method"""


print(__doc__)
print(C.__doc__)
print(C.meth.__doc__)
print(func.__doc__)
```
- those ways below are how to call the docstrings above.
- the `__foo__` is called a magic attribute, or a "dunder" attribute.  They must be leading and trailing.  They are hooks for the interpreter.

- Docstrings
	- they basically work as a summary for the programmer so they can see how a function works.  They can be 1 line or multiline.  Multiline should have a blank space between the first line summary and the rest of the docstring
	- a multiline docstring should end with triple quotes on its own line.

- PEP 257: https://www.python.org/dev/peps/pep-0257/

- `u'unicode string'`
	- this prefix is there only for backwards compatability because it is default in python3.0
	- it means it is a text string

- `r'raw string'`
	- it preserves literal escape sequences in the string
	- something like \n which normally create a new line will be treated as regular characters.
	
- these can be used for any of the strings we saw above.

- `b'foo'`
	- a bytes literal, a binary string, a bytestring
	- it makes a stringlike thing that is really a sequence of integers
	- br and rb are valid

- `f'foo'` - (new in python3.6)
	- they are called format strings, will look at later.
	- rf and fr are valid

- illegal combinations so far are: ur, ru, uf, fu, ub, bu, fb, bf.  These will all fail.

- the typename of strings in python is `str`

- operators that can be used with strings

	- multiplication 'hi' * 3 >>> 'hihihi'
	- `<`, `<=`, `>`, `>=`, `==`, `!=` checks values of string to sort them.
		- 'abc' < 'abb' False
		- 'abc' < 'ABC' False
		- 'abc' < 'bbc' True
	- plus '+' or the concatenation operator
		- 'foo' + 'bar' >>> 'foobar'
	- `in` checks if the string is in another string
		- 'f' in 'foobar' True, for instance
	- `len(foo)` shows how long the string is.  it looks for this function: `.__len__()`

STRING METHODS
--------------

- how you call any method
```python
foo = 'hello world'
print(foo.upper())
```

- how you should apply these to strings
- `'string'.capitalize()` - can also have a variable containing a string instead of the string

- `.upper()` - makes everything upper case
- `.title()` - makes it be capitalized on start of every word
- `.lower()` - makes everything lower case
- `.swapcase()` - swaps the casetype
- `.casefold()` - its like .lower() on steroids, since it will convert things like 'ß' to 'ss'
- `.capitalize()` - returns a copy of the string with the first character capitalized and the rest lowercase 
- `str.startswith(s, [, start [, end]])` - the last part allows you to bound your search
- `str.endswith(s, [, start [, end]])`

- `.isalnum()` - alphanumeric, `.isalpha()`, `.isascii()`, `.isdecimal()` - 1-10, `.isdigit()` - all the characters are 0-9 , `.isidentifier()` - whether that string could be a python identifier, is it a variable name.
- `.islower()` - are they lower case `.isnumeric()`, `.isprintable()` - can everything go to the screen?
- `.isspace()`, `.istitle()` - are they capitalized by front of each word `.isupper()`

- `.find(s, [, start[, end]])` - it will find the first position in the string which matches s, and if not, it returns -1 (which is true), gives the position
- `.index(...)` - same thing, but raises a `ValueError` if it doesnt find anything
- `.rfind(...)` - same thing, but look from the end
- `.rindex(...)` - same thing, but look from the end

- `.strip([chars])` - will remove those characters from the edges of strings, and by default is blank.  it will strip any regardless of order.
- `.lstrip([chars])` - only from the left
- `.rstrip([chars])` - only from the right

- `.replace(old, new[, count]`

- `.partition(sep)` - returns 3 things, if it finds it, it will split along thereand the rest will be on the right.  if not, everything is on the left.

```pycon
>>> 'foo bar baz'.partition(' ')
('foo', ' ', 'bar baz')
>>> 'foo bar baz'.partition('!')
('foo bar baz', '', '')
```

- `.rpartition(sep)` - the same, but it starts it from the right side

```pycon
>>> 'foo bar baz'.rpartition(' ')
('foo bar', ' ', 'baz')
>>> 'foo bar baz'.rpartition('!')
('', '', 'foo bar baz')
```

- `.split(sep=None, maxsplit=-1)` - first is what is being split (and removed), last is how many times it does it.
- `.rsplit(...)` - does it from the right side
- `.splitlines([keepends])` - see below
- `\n`, `\r\n`, `\r` - all different types of newline.

```pycon
>>> 'split\nsplit\r\nsplit\r'.splitlines()
['split', 'split', 'split']
>>> 'split\nsplit\r\nsplit\r'.splitlines(True)
['split\n', 'split\r\n', 'split\r']
```

- `.join(iterable)` - it takes the iterable and inserts the string in between each thing.  works the opposite of split

```pycon
>>> ', '.join(('a', 'b', 'c'))
'a, b, c'
```

- `.format(*args, **kwargs)` 

---

String Formatting
-----------------

- `%-formatting`
	- 'hello %s' % 'world' >>> 'hello world'
	- 'hello %s %s' % (1, 2) >>> 'hello 1 2'
	- 'hello %(hi)s %(ohai)s' % {'hi': 'one', 'ohai': 'two'} >>> 'hello one two'

- `new string formatting` (uses .format())
	- 'foo {bar} {baz}'.format(bar='hello', baz='ohai') >>> 'foo hello ohai'
	- 'foo {} {}'.format('bar', 'baz') >>> 'foo bar baz'
	- 'foo {1} {0}'.format('bar', 'baz') >>> 'foo baz bar'
	- 'foo {0} {0}'.format('bar', 'baz') >>> 'foo bar bar'
	- https://pyformat.info/
	- 'hello {!r}'.format('world') >>> "hello 'world'"
	- that is a "repr" which is a built in function it shows a programer representation of an object (repr(x))

```pycon
>>> print('foo')
foo
>>> print(repr('foo'))
'foo'
```

- `f strings`

```pycon
>>> thing = 'world'
>>> f'hello {thing}'
'hello world'
```

---

SLICING, INDEXING, ITERATING
----------------------------

-Iterating - basically, just think of this as how you would use it in a for loop

```pycon
>>> for c in 'hello':
...     print(repr(c))
... 
'h'
'e'
'l'
'l'
'o'
```

- iterating over a string produces one character string per iteration

- Indexing - they will also give one character strings.
	- foo[0]
	- foo[-1] will do the first index from the back
	- will raise an IndexError if out of bounds

- Slicing - syntax looks like this: s[<START>:<END>:<STEP>], but the most basic is s[:] which returns a copy of the string
	- 'hello'[1:]
	'ello'
	- 'abcdefgh'[::2] (is a step)
	'aceg'
	- it's kinda like list(range(0, 7, 2))
	[0, 2, 4, 6]



---

- for loop
	- is good for when you have an interval or a fix sized bound, i.e. from 1 - 100, or from 2 to something.  Another is when you are iterating over an iterable object.

- written as `for <unpacking> in <iterable>:`
	- the unpacking is basically an assignment, and the iterable is what we are iterating over.
	- the most basic iterable is a function called `range`

- while loop
	- is useful running a chunk of code while a condition is true.

- `elif` will run if the `if` statement before it fails

	- you can have 1-inf `if` statements, 0-inf `elif` statements, and 0 or 1 `else` statements in that order.


