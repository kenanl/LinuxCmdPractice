[Original video](https://www.youtube.com/watch?v=bF7c8Owp_3Y)

### Executing python script
Without parameter : `python3 my_echo.py`
With paramter: `python3 my_echo.py hello world!`

Another way:
1. add `#!/usr/bin/env python3` at the top of the script
2. check permission status of the script: `ls -la`, now the script is read/write, but not executable.
3. in the shell terminal, use `chmod +x my_echo.py`. Now the script is executable
4. run `./my_echo.py hello wolrd!`.
5. In addition: Linux does not care about the suffix of file name. We rename the file name by removing file type suffix, by using `mv my_echo.pymy_echo`.  Now we can use `./my_echo hello world!` to execute it. 

Note: Add up this does not impact the initial way of runningthis script.

If we want to call this executable outside current folder, we can
1. Add the current path to our environment variables, `PATH=$PATH:$PWD`. We can check it is added or not by `echo $PATH`
2. Now we can step to the parent folder in terminal, and directly use`my_echo  hello world!`

`which python` or `which python3` can help us find where python is installed in our machine. Similarly, `which my_echo` returns the path of our ownversion  of echo executable.

### #!
read as 'shebang', could be sourced from SharpBang or HashBang

### chmod
change mode
- `chmod +x foo` add executable permission. `+w +r` are for write and read
- `chmod -x foo`
- `chmod 740 foo` (chmod a+rwx,g-wx,o-rwx) sets permissions so that, (U)ser / owner can read, can write and can execute. (G)roup can read, can't write and can't execute. (O)thers can't read, can't write and can't execute. [chmodcommand.com/chmod-740/](https://chmodcommand.com/chmod-740/)
- 644 is the default mode

### mv
- `mv a.txt b.txt` rename
- `mv folder newFolder/` move folder

### cp
- `cp a.txt a_copy.txt` copy file
- `cp -r dir1 dir2` copy folder. `-r` means recursive

### rm
delete, but will not found in trashbin
- `rm a.txt`
- `rm a.txt b.txt` or `rm *.txt`
- `rm -r dir1` delete all under dir1




