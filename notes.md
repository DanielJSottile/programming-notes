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

- `!$' - similar to above, but only does the last part of the command

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

- `:q!` exit and discard changes

- press `:w` to write the file

- press `:wq` to write the file AND quit

- `dd` will delete a line

- `^` goes to the beginning of the line

- `$` goes to the end of the line 

- `shift + g` goes to the end of the file

- `[#] shift + g` goes to that specific number line

- `u` will undo.

- `:sort` sorts the file by character value 

---

.bashrc
-------

-`.bashrc` is located in the ~ directory (home).  So far we have added:


```
[ -d "$HOME/bin" ] && export PATH="${HOME}/bin:${PATH}"
```
- in conjunction with virtualenv


```
export EDITOR=vim VISUAL=vim
```
- in order to set our default interpreter as vim


```
function title() {
    PS1="$(sed 's/\\\[\\e]0;.*\\a\\]//g' <<< "$PS1")"
    PS1="${PS1}\[\e]0;$*\a\]"
}
```
- Anthony made this.  If you type `title` followed by any characters, you can make titles for the current tab you are on.  neato.

---

GIT
---

- `git clone [URL]` - makes a clone of a repository on github

- `git status` - shows the current state of the git repository

- `git add [file]` adds a file to staging area for git repository

- `git commit` - commits anything that is staged

- `git commit -m ['commit messages here']` standard practice to add a message

- `git push` - pushes current branch onto git repository
	- `git push origin HEAD` - HEAD is a shortcut for the current thing you have checked out, and origin is the remote that you are pushing to.  Do this whenever you are doing a pull request, or on anything really.

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

- `git checkout <branchname>` will switch branches

- `git branch --merged` shows all branches that are merged with master

- `git branch -d <branchname>` deletes that branchname

- to convert a directory into a git repo:
    - first, create a new repository on Github

    - cd to the repository you want to add

    - type `git init` - it initializes an empty repository

    - `git commit --allow-empty -m 'initial empty commit'` - adds an empty commit - its a commit with no contents.

    - you'll have to add a .gitignore to this directory and add the things you should ignore.

    - `git add .` - adds all the files

    - `git commit -m 'message'` - as normal

    - `git remote add origin <url>` - this sets the remote that you push it to.

    - `git push -u origin master` - this pushes to there.

- to update multiple files again, you can run `git add .` or `git add -u` and push it like normal

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

- `sed` - stream editor, performs basic text transformations
- `-i` transforms files in place
- `-r` uses extended regex


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

	- multiplication `'hi' * 3 >>> 'hihihi'`
	- `<`, `<=`, `>`, `>=`, `==`, `!=` checks values of string to sort them.
		- 'abc' < 'abb' False
		- 'abc' < 'ABC' False
		- 'abc' < 'bbc' True
	- plus `+` or the concatenation operator
		- `'foo' + 'bar' >>> 'foobar'`
	- `in` checks if the string is in another string
		- `'f' in 'foobar' True`, for instance
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

LISTS
-----

- lists only have 1 syntax, which looks like this: [..., ...,]
	- `['hello', 'world']`

- list('hello')
	- ['h', 'e', 'l', 'l', 'o']

- lists can be multi-line like this:

```python
x = [
    1,
    2,
    3,
]
```
- the comma at the end is optional, but it's good practice for multi line lists.

LIST OPERATORS
--------------

- `+` you can add lists together, but only lists to lists.
- `*` it repeats the list 
- `<`, `>`, `<=`, `>=`, `==`, `!=`, they work the same as the strings, but they start by comparing the 1st element, 2nd, etc.
- `in` - checks if any of the elements are equal to the right hand side.

```pycon
>>> 3 in [1, 2, 3]
True
```

- `del` deletes that array position
```pycon
>>> x = [1, 2, 3]
>>> del x[1]
>>> x
[1, 3]
```

---

INDEXING AND SLICING
--------------------

- works the same as strings!  one small difference is that you can assign to a slice (in essence replace it)

```pycon
>>> x = [1, 2, 3, 4, 5]
>>> x[1:3]
[2, 3]
>>> x[1:3] = [6, 7, 8]
>>> x
[1, 6, 7, 8, 4, 5]
```

- lists are 'mutable' which means parts inside them can be changed.  so for instance, individual indexes can be changed.

---

LIST METHODS
------------

- `list.append(element)` - adds to the end of a list
- `list.pop([i])` - i is index, or the last index if not i, removes that element.
- `list.insert(i, element)` - inserts into list at index i
- `list.extend(itterable)` - appends all the elements in the itterable

```pycon
>>> x = [1, 2, 3]
>>> x.extend([4, 5, 6])
>>> x
[1, 2, 3, 4, 5, 6]
```
- `list.count(x)` - counts the number of times x appears in the list
- `list.index(x[, start[, end]])` - this find the index if the first element that matches, and raises ValueError if it doesnt exist.
- `list.remove(x)` - this removes the first element matching x, and raises ValueError if it doesnt exist.
- `list.clear()` - empties the entire list
- `list.sort(key=None, reverse=False)` - this sorts the list in place, and the key is a function that takes the element and returns the sort key.

```pycon
>>> def uppercase(s):
...     return s.upper()
... 
>>> x = ['fOo', 'Foo', 'bar']
>>> x.sort()
>>> x
['Foo', 'bar', 'fOo']
>>> x.sort(key=uppercase)
>>> x
['bar', 'Foo', 'fOo']
``` 
	- there is also `sorted(x)` and `sorted(iterable)`
- `list.reverse()` - it reverses the list in place.
	- there is also `reversed(x)` would reverse a list of x, it returns a reversed iterator of the list, does not actually modify.  there's also `reverse(reversible)`

- `list.copy()` - copies a new shallow copy of the list.

```pycon
>>> x = [[1, 2, 3], [4, 5, 6]]
>>> x[0].append(5)
>>> x
[[1, 2, 3, 5], [4, 5, 6]]
>>> y = x.copy()
>>> y.append([])
>>> x
[[1, 2, 3, 5], [4, 5, 6]]
>>> y
[[1, 2, 3, 5], [4, 5, 6], []]
>>> x[0].append(7)
>>> y
[[1, 2, 3, 5, 7], [4, 5, 6], []]
```

---

TUPLES
------

- syntax (x, y), though technically you can have something like y = 1, 2
- `()`, `(1,)`, `(1, 2)`
- just like lists, you can construct one like this `tuple(iterable)` => ('h', 'e', 'l', 'l', 'o')
- they can be multi line like this:
```
x = (
    1,
    2,
    3,
)
```

- what is a tuple?  it is a sequence type, sort of like a list, but you cannot modify it.


TUPLE OPERATORS
---------------

- they support the same as the LIST OPERATORS!  EASY!

INDEXING AND SLICING
--------------------

- indexing and slicing is similar, but you cannot assign to a slice or index because a tuple is immutable

METHODS
-------

- there are 2:
- tuple.count(x) - counts the amount of things in the tuple.
- tuple.index(x[, start[, end]]) - this find the index if the first element that matches, and raises ValueError if it doesnt exist.

NAMED TUPLES
------------

- `collections.namedtuple(typename, field_names, *, rename=False, defaults=None, module=None)`

- here is an example:

```pycon
>>> import collections
>>> Car = collections.namedtuple('Car', ('make', 'model', 'color'))
>>> car = Car('chevy', 'corvette', 'red')
>>> car
Car(make='chevy', model='corvette', color='red')
>>> car.count('chevy')
1
>>> car.make
'chevy'
>>> car.model
'corvette'
```

- they are their own data type, but still inherit from tuple.  They are basically tuples.

---

- for loop
	- is good for when you have an interval or a fix sized bound, i.e. from 1 - 100, or from 2 to something.  Another is when you are iterating over an iterable object.

- written as `for <unpacking> in <iterable>:`
	- the unpacking is basically an assignment, and the iterable is what we are iterating over.
	- the most basic iterable is a function called `range`

- while loop
	- is useful running a chunk of code while a condition is true.
        - is often found in this pattern;
```python
# INITIALIZE
while CONDITION:
    # BODY
    # UPDATE (often the same as initialize)
```

- `elif` will run if the `if` statement before it fails

	- you can have 1-inf `if` statements, 0-inf `elif` statements, and 0 or 1 `else` statements in that order.

---

DICTIONARIES
------------

- syntax: `{'key': value, 'key2': value, 'key3': value}`
or
- `dict(key='value', key2='value'`)
or
- `dict([('key1', 'value1'), ('key2', 'value2')])`
- what it lets you do is map keys to values, allows you to do lookups
- keys must be immutable!
- operators that can be used:
    - `in` checks if the key exists inside the dictionary
    - `del` will delete an entry
        ```pycon
        >>> x = {'k': 1, 'k2': 2}
        >>> del x['k']
        >>> x
        {'k2': 2}
        ```
    - `==` and `!=` checks if keys and values are the same
    - `len(dct)` will tell you how many entries there are
    - looping in dictionaries changes the keys and values:
    ```pycon
    >>> for k in {'k': 1, 'k2': 2}:
    ...     print(k)
    ... 
    k
    k2
    ```

-indexing

- you can look up the keys (but cannot change them)
```pycon
>>> x = {'k': 1, 'k2': 2}
>>> x['k2']
2
```
- gives a KeyError: if accessed out of bounds
- you can modify the values as well:
```pycon
>>> x
{'k': 1, 'k2': 2}
>>> x['k2'] = 3
>>> x
{'k': 1, 'k2': 3}
```

- methods

- `dct.clear()`
- `dct.copy()`
- `dct.get(key, default=None)` - this retrieves the value for the key or defaults if not present
    - usaully bad because it means you're guessing your data
- `dct.pop(key[, default])` - it will remove the entry returning the value of that entry, and if default is not present and key is not present, raise a `KeyError`.
    - if default is present it will return that value instead
- `dct.setdefault(key, default=None)` - it will set the key to the default value if the key isnt present, and returns the value.
```pycon
>>> x
{'k': 1, 'k2': 2}
>>> x.setdefault('k', 999)
1
>>> x
{'k': 1, 'k2': 2}
>>> x.setdefault('k3', 999)
999
>>> x
{'k': 1, 'k2': 2, 'k3': 999}
```
- `dct.popitem()` - returns a key value pair from the dictionary and delete it from the dictionary.
    - it will return the last pair that was set in the dictionary, its a new behavior in 3.6
- `dct.update(other)`
    - `dct.update(k=1, k2=2)`
    - `dct.update({'k': 1, 'k2': 2})`
    - `dct.update([('k', 1), ('k2', 2)])`
- this adds multiple values and keys to the dictionary and overwrites them if they are already there.

- `dct.keys()` returns a keyview, iterating over it iterates over the keys
- `dct.values()` returns a valuesview, iterating over it iteraves the values
- `dct.items()` returns a view of both, iterating gives both.
```pycon
>>> x = {'k': 1, 'k2': 2}
>>> for k, v in x.items():
...     print(f'{k} = {v}')
... 
k = 1
k2 = 2
```
- dict.fromkeys(iterable, value=none) - it creates a dictionary that takes from the iterable and sets them all to the value.
```pycon
>>> dict.fromkeys([1, 2, 3], 'ohai')
{1: 'ohai', 2: 'ohai', 3: 'ohai'}
```

---

LAMBDA
------

-a lambda is a one line function with no name
-if you had a function that looked like this:
```
def func(a, b, c):
    return a + b // c
```
- then the equivalent lambda would look like this:
- `func = lambda a, b, c: a + b // c`
- they allow you to cut corners when things need a function
- they have the name '<lambda>'

---

I/O
---

- opening files:
- syntax: `open(filename, mode='r', ...)`
- ran as:
```python
with open(filename) as file_obj:
    ...
```

- `r` - reading a file
- if file does not exist, it will come up with an error.
- `w` - writing a file
- w opens the file for writing, truncate to zero bytes, and then start writing.  It will empty files with that name beforehand.
- `a` - append mode, adds to the end of a file.
- if you put a `b` next to any of these, it will do it in binary mode, which just gives the raw bytes.
- occasionally will need the `+` which is used for read and write mode.

- writing files:
- syntax: `file_obj.write('foo\n')`
- you can also do this: `print('foo', file=file_obj)`
- another writing function: `file.obj.writelines(<iterable of lines>)`
- but you could also do:
```python
for line in lines:
    file_obj.write(line)
```
- sometimes when writing and reading to disk, parts of the file are in memory before they are on disk.  use `file_obj.flush()` that flushes the buffer.  if you use it, put it after write calls.

- reading from a file:
- if you are reading line by line:
```python
with open('foo.txt') as f:
    for line in f:
        print(line, end='')
```

- theres a less good way to read all the lines in a file:
- `file_obj.readlines()` which returns a list of lines.
- `file_obj.readline()` reads a single line, if you run it once, it reads the first line, then if you run it again it reads the second line.
- `file_obj.read(size=-1)` - it would read the entire file as one string.
- but AHA! you can change the size of that to 1 and read the file one character at a time!

- there are some things that act like file objects but are not actually file objects, such as:
- urlopen (opens urls) and returns a binary file, also you have to import urlopen
- StringIO - is an in memory file and comes from the io module. for example: `sio = io.StringIO('hello world')`
```pycon
>>> sio.read(1)
'h'
```
---

BUTLT IN ITERABLE FUNCTIONS
---------------------------

- `enumerate` - allows you to run through an interable but allows you to keep a number next to it.  it's formated as:

- `enumerate(iterable, start=0)`

- you can make the iterable a slice, and of course, change the start number.

- `all(iterable)` it iterates over all the elements and returns true if the elements are truthy, or if its empty.

- `any(iterable)` the same thing, but if any are true.  empty in this case is actually False.

- `filter(function or None, iterable)` - it calls a function on each part of the iterable and returns a new version of the iterable if it is true.

- `map(fn, iterable[, iterable, ...])` - it applies a function to each element of an iterable

- `iter(obj)` - returns an iterator from a thing

- theres also `iter(fn, sentinel)` - this makes an iterator where calling next will call that function and return the value, and it will do that until the object returns the sentinel.

- `sentinel` - its a place holder value.

- `next(iterator obj)` - gives the next object in the itorator or raises a StopIteration if it finds nothing next.

```
>>> x = [1, 2, 3]
>>> iter(x)
<list_iterator object at 0x7ff327dbff98>
>>> x_iter = iter(x)
>>> next(x_iter)
1
>>> next(x_iter)
2
>>> next(x_iter)
3
>>> next(x_iter)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
StopIteration
```
- `reversed(iterable)` - it reverses the object inside, unordered objects are not reversible, and unsized objects are not reversible.

- `sorted(iterable, *, key=None, reverse=False)` - it sorts the iterble inside.

- `sum(iterable[, start])` - it adds each of the elements of the iterable, error if wrong type.

- `zip(*iterables)` - yield tuples from each iterator:

```
>>> for a, b in zip('abc', (1, 2, 3)):
...     print(f'a: {a}, b: {b}')
... 
a: a, b: 1
a: b, b: 2
a: c, b: 3
```
```
>>> list(zip('abcdefg', 'hi'))
[('a', 'h'), ('b', 'i')]
```

- theres also itertools, which you must import
https://docs.python.org/3/library/itertools.html

---

COLLECTIONS
-----------

- it is a module to import

- `collections.defaultdict(factory_fn, <<normal args to dict(...) here>>)`

- works the same as a dictionary, except instead of key erroring, it will call the factory function and return/set that value.  Basically allows you to bypass whether a key exists or not.

- `collections.Counter(iterable)` - makes a mapping from element to count i.e. it counts the amount of unique elements inside.  It acts a little bit like a dictionary.  The most popular is .most_common(n=None)

```
>>> collections.Counter('the quick brown fox')
Counter({' ': 3, 'o': 2, 't': 1, 'h': 1, 'e': 1, 'q': 1, 'u': 1, 'i': 1, 'c': 1, 'k': 1, 'b': 1, 'r': 1, 'w': 1, 'n': 1, 'f': 1, 'x': 1})
```

```
>>> ctr = collections.Counter((1, 1, 1, 1, 4, 4, 5, 6, 7, 8, 9, 9))
>>> ctr.most_common(3)
[(1, 4), (4, 2), (9, 2)]
```

---

SETS
----

- a `set` is a mutable, unordered collection of unique items.
- a `set` must only contain immutable things, same requirement for keys in a dictionary.
- syntax of sets: `{item1, item2 ... }` it looks a bit like a list.  They can be multi-line just like lists can.
- the only way to make an empty set is `a = set()`
- the set class takes an iterable, like a string or a list
- 
```
>>> a = set('abracadabra')
{'a', 'r', 'b', 'c', 'd'} # unique letters in a
```
- methods: 

![](https://i.fluffy.cc/KCbbn6vWKjl7MDqZz8kTWmF9lrbgGJC4.png)

- `set.add(element)` - adds an element to a set.  if there, does nothing. (idempotent)
- `set.remove(element)` - removes an element or KeyError if it does not exist.
- `set.discard(element)` - an idempotent remove
- `set.pop()` - this removes an arbritrary element and returns it. raises KeyError otherwise
- `set.clear()` - removes all from set.
- `set.update(*iterables)` - updates the set with the elements from the iterable.
- `set.intersection_update(*iterables)` - modifies the set to contain only the items that are in all the iterables and itself.
- `set.difference_update(*iteralbes)` - removes the elements that are in any of the iterables.
```
>>> x = {1, 2, 3, 4, 5}
>>> x.difference_update((1, 2), (2, 3), (5,))
>>> x
{4}
```
- `set.symmetric_difference_update(other)` - modifies itself to only contain the elements that are not in both.
```
>>> x = {1, 2, 3, 4, 5}
>>> x.symmetric_difference_update((3, 4, 5, 6, 7))
>>> x
{1, 2, 6, 7}
```
- `set.union(*iterables)` - this one is like update, but it returns a new set (does not modify itself)
- `set.intersection(*iterables)` - like int-update, but it returns a new set 
- `set.difference(*iterables)` - " " ", but it returns a new set
- `set.symmetric_difference(other)` - " " ", but it returns a new set

- `set.isdisjoint(other)` - sets are disjoint if they have no overlap, returns a bool
- `set.issubset(other)` - true if every element is inside the other set
- `set.issuperset(other)` - true if every element in other is inside the set (so basically the opposite of above)
- `set.copy()` - it returns a copy of the set.

- operators

- sets are not indexable!
- `len(set)` - gives the length of the set
- `in` and `not in` - tells you whether the element is in the set.
- `|` - returns the union of sets on both sides. (this is binary 'or')
- `&` - returns the intersection of sets on both sides (this is binary 'and')
- `-` - returns the difference of sets on both sides
- `^` - returns the symmetric difference of sets on both sides (binary 'exclusive or', or 'xor')
```
Truth table for AND

  || T | F |
============
T || T | F |
--||---|----
F || F | F |

Truth table for OR

  || T | F |
============
T || T | T |
--||---|----
F || T | F |

Truth table for XOR

  || T | F |
============
T || F | T |
--||---|----
F || T | F |
```

- `|=` the same as union update
- `&=` the same as `intersection_update`
- `-=` " " " `difference_update`
- `^=` " " " `symmetric_difference_update`
- `<=` `>=` - they are issubset and issuperset
- `<` `>` - they are strict subset and strict superset (cannot be equal) 
- they must have sets on both sides, or else they will TypeError

- Frozen Set

- an immutable set (can only make it from frozenset(iterable)
- works the same as a set but without any update methods

---

COMPREHENSIONS
--------------

- `START-BRACE EXPRESSION FOR-PART (IF-PART | FOR-PART)* END-BRACE`
- `ret = [x ** 2 for x in range(10) if x % 2 == 0]`
- roughly the same as:
```
ret = []
for x in range(10):
    if x % 2 == 0:
        ret.append(x ** 2)
```
- there are 4 types of comprehensions:
- list comprehension: `[x for x in ...]`
- set comprehensions: `{x for x in ...}`
- dict comprehensions: `{k: v for ... }`
- generator expressions `(x for x in ...)` (is lazy)

- what is lazy?  in programming there are two approaches to computation, eager or lazy.  Eager will compute the value immediately, while lazy will only compute the value when it's necessary.

- an example of gen expressions:

```
>>> gen = (x for x in range(5))
>>> gen
<generator object <genexpr> at 0x7f90a9f07af0>
>>> next(gen)
0
>>> list(gen)
[1, 2, 3, 4]
>>> list(gen)
[]
```

- you can have double for loops...or MORE!:
```
>>> ret = []
>>> for x in range(5):
...     for y in range(5):
...         ret.append((x, y))
... 
```
```
ret = [(x, y) for x in range(5) for y in range(5)]
```

- double if statements are treated as `And`
` ret = [x for x in range(100) if x % 5 == 0 if x < 20]`

---

TERNARY
-------

- means composed of three parts, in this part, the truth value, the condition, and the false value.

```
foo = 'hi'
bar = 'hello' if foo == 'hi' else 'baibai'
```

---

JSON
----

- JSON is a data format, "JavaScript Object Notation" and it's primary benefit is that it's extremely simple and readable.  There was XML before JSON.
- JSON has a few types it can represent.  The first type is strings.  They are always double quoted, otherwise mostly act like python strings.
- next type is numbers.  Just like normal, numbers.  integers and floats alike map to the JS number type.
- boolean types, which are true and false, and a null type
- arrays, which are with []'s and unlike python they cannot have trailing commas
- obj type, it looks like python syntax but keys must be strings.  and no trailing commas ;(
- no comments in JSON

- in python theres a module called JSON
- there are 4 API's:
- `json.loads(s)` => (python object)
```
>>> json.loads('{"foo": ["bar", "baz", "womp"]}')
{'foo': ['bar', 'baz', 'womp']}
```
- `json.dumps(obj)` => (json string)
- `json.load(file_obj)` => (python object)
- `json.dump(obj, file_obj)` => writes the obj to the file obj

---

REST API
--------

- HTTP: hyper text transport protocol, it's a convention built on TCP (transmission control protocol).  Basically, http is the standard convention that you use when you talk to websites.  

- Typically split into 2 portions, request and response.
- first tells what the protocol is, the verb, and the path, itll pass headers and an optional body.
- request example:

```
GET /foo HTTP/2
Host: example.com
User-Agent: curl/7.58.0
Accept: */*
```
- the response looks like the protocol, then the status code, then headers, then a body (same format as request)

```
HTTP/2 200
cache-control: max-age=604800
content-type: text/html; charset=UTF-8
date: Wed, 15 May 2019 00:22:20 GMT
etag: "1541025663+ident"
expires: Wed, 22 May 2019 00:22:20 GMT
last-modified: Fri, 09 Aug 2013 23:54:35 GMT
server: ECS (sjc/4E8B)
vary: Accept-Encoding
x-cache: HIT
content-length: 1270
<!doctype html>
<html>
<head>
    <title>Example Domain</title>

    <meta charset="utf-8" />
    <meta http-equiv="Content-type" content="text/html; charset=utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
```

- `HTTP/1.1 404 Not Found`
- theres several verbs that get used.  The most common one is `GET`. it is used to read things and conventionally does not perform side effects.  i.e. usually is not used to write stuff, only to retrieve.  You can do it but....DONT DO IT.
- `POST` - usually used for creation, or things that have a side effect.  For instance, signing up for a website, which creates some user data, etc.- generally the web only sticks to GET and POST, but not necessarily anymore.  Old browsers were limited by GET and POST in the past.  womp womp IE.  so sad.
- `PUT` - update/replace, this also makes modifications and is idempotent.- `PATCH` - update/modify, not idempotent.
- `DELETE` - deletes stuff.  is idempotent.

- the first is the parameters in the url, one is via path variables `/foo/1` the second is via the query string, it is a ? followed by some parameters and separated by an &, such as `?foo=1&bar=2` special characters get encoded.  for instance, space is either %20 or +.  `urllib.parse` lets you encode url.  that format is called URL encoding.  in GET requests it's the thing after the ?.  in post requests, you can send it as the body of the request data.

- the other convention in POST requests is the send json as the body. it's the same for PUT and PATCH.

- someone will ask in an interview "can a GET request have a body?" technically it can, but no one does that.

---

CLASSES
-------

- classes give a way to create your own data types.  declare them with class Name:  conventionaly the name should be PascalCase, i.e. each word is capitalized and not separated by an _.

- classes can also have an extra parameter that sepcifies it's base class i.e. inheritance. `class C(base1, base2, base3): pass`

- if you see this `class C(base1, metaclass=M): pass`, this is a metaclass.

- 

```
class C:
    # class variables
    x = 1

   # methods
    def __init__(self, y):
        self.y = y # instance variable

    def f(self):
        print('hello world')

    @staticmethod
    def static_method(arg1, arg2):
        print(arg1, arg2)

    @classmethod
    def class_method(cls, arg1, arg2):
        print(arg1, arg2)
```

- self.y is an instance variable.  it exists only on the object. it kinda looks like this in memory: `"object instance": {"__class__": C, "y": ...}`

- the @ is a decorator.  if you have:

```
@foo
def bar(): pass
``` 
it is equal to:
```
def bar(): pass
bar = foo(bar)

i.e. bottom goes into top.

- 
```

- @staticmethod and @classmethod make it so that you don't need (self) as arguments.

- @property means you dont need to use parentheses anymore when calling the property. It allows you to have computed attributes.

- conventions in classes:

- def normal_method(...): # public (anyone can call it)
- def _private_method(...): # private (should only be called by the class itself)
- def __name_mangled(...): # name mangled (it changes the name when the class gets built so it's even more private), actually ends up being _C__name_mangled (when defined in 'class C')  only used to avoid collisions in inheritance.
- def __magic__(...): # magic methods do not get name mangles, usually represent special hooks such as operators or lifecycle (__init__)

- INHERITANCE

- if you inherit from a class, you can override it's behaviors.

```
class C:
    def bar(self):
        print("I do the bars!")
    def foo(self):
        print('I do the foos!')

class D(C):
    def foo(self):
        print('no foos here!')
```
but also...

```
class E(C):
    def foo(self):
        super().foo()
        print('but also E foos!')
```
- so in the old days, you could use C.foo() to reference C, but then they added super, which automatically finds the reference for you.

- you can nest classes.  if you want.

---

TRY/EXCEPT
----------

- syntax:
```
try:
    # any number of statements
# (optional, and as many as needed)
except Type:  # or `except (Type, Type2)`  # or `except Type as val:`  # or `except (Type, Type, Type) as val:`
   # any number of statements)
# (optional)
else:
    # code which is only run if the body of the `try` is successful
# (optional)
finally:
   # code which is run whether or not there is an exception
```

- dont use except: .  It will catch everything including stuff you do not want to catch.  instead, use except BaseException.

- inside an except block, if you use `raise` without any arguments, that's the same as "re-raise this exception as if I didn't do anything".


- 
```
except BaseException:
    # maybe do some logging or whatever
    raise  # reraise the exception
```

- when using try/except, it's better to ask for forgiveness than permission.  The idea is that it's more performant to assume it will succeed and catch the error rather than writting it to always check it.  Use it only when you have to.

---

PYTEST
------

- first, place a venv inside the project you are working on.
- install pytest with pip install pytest
- then inside the project folder create a directory called `tests` and inside that directory create `__init__.py` and `[name of file]_test.py`

- inside the test.py file, import the name of the file i.e. `import project_3`

- the basic test you can run is structured like this:

```
def test_equals_digit():
    assert project_3.equals_digit(4697, 5) is False  # (or == something)
```

- however, this only allows you to do one test per function, and you have to rename it.

- if you import pytest, you can put this as your overall test example:

```
@pytest.mark.parametrize(
    ('param1', 'param2'),
    (
        (1, 2),
        (3, 4),
    ),
)
def test_foo(param1, param2):
    assert file.foo(param1) == param2 
```

- param2 is usually 'expected'

- for prints, you have to do a little something different:

- you'll need to do something like this

``` 
def test_func(capsys):
    file.func(param1, param2)  # make it the actual values you are testing
    captured = capsys.readouterr()
    assert captured.out == "however it's suppossed to be printed"
```

- you can do clever things to make your tests more compact such as:
ret = function() # call things inside that function
expected = __ # your expected value
assert ret == expected

---

COVERAGE
--------

- coverage is a tool that shows which lines get executed.
- we ran these commands to use it.
- `coverage erase` - erased all the previous info about coverage
- `coverage run -m pytest tests` runs the module pytest with argument tests while coverage is instrumented
- `coverage report --show-missing --omit=venv*` - gave us a report about the coverage
- `coverage html --omit=venv*` - this makes an html report of the coverage
    - `firefox htmlcov &` - opened it in firefox in the background
- you can use this with pytests to show which lines have been tested.

---

FLAKE8
------

- if you use `# noqa` will ignore all errors
- if you use this form `# noqa: E702` it will ignore that specific error
- `# flake8: noqa` ignores all flake8 errors

---

DEBUGGER
--------

- in python3.6 or lower: `import pdb; pdb.set_trace()` (at the top of the file)
- in python3.7 or newer: `breakpoint()` (wherever you want to start debugging code)
- `list` shows where you are about to run a line of code
- `n` goes to the next line
- `s` step into, which lets you follow into a function call and see how it executes
- `p [variable name]` prints the variable
- `pp [var name]` pretty prints the variable
- `w` shows the full call stack i.e. the calls that led to where you are now
- `q` quits the debugger
- https://docs.python.org/3/library/pdb.html#debugger-commands

    

