# Unix Commands

The commands below are Unix commands. They will all run from the Mac Terminal, and in most cases, Windows Powershell or Git Bash.

Many, but not all, of these commands will run inside the IPython shell. For example, `touch` is not a valid command in IPython. Of the below, valid commands in the IPython shell include `pwd`, `cd`, `ls`, `rm`, `cp`, and `mv`.

## Navigation

* `pwd` - Stands for `print working directory`; this will write the full
  pathname of the current working directory to the terminal
* `cd` - Stands for `change directory`; this will allow you to navigate between
  different folders/directories in your directory structure
* `ls` - Stands for `list`; this will list the files in the current working
  directory

```bash
cd galvanize/DSI-evening-prep # To use the cd command in this way,
                              # /Users/sallamander must be my current
                              # directory.
cd /Users/sallamander/galvanize/DSI-evening-prep # This will work from
                                                 # any current directory.
```

```bash
cd ~ # Change directories to your home directory.
cd  # Another way to change directories to your home directory. 
cd .. # Change directory to the directory right above the current directory.
```

```bash
ls # List all of the files and directories in galvanize/DSI-evening-prep
ls Introduction # List all of the files and directories in
                # galvanize/DSI-evening-prep/Introduction
ls /Users/sallamander/galvanize/DSI-evening-prep/Introduction # Same thing as
                                                              # ls Introduction
                                                              # above
```

## Creating and Removing files

* `touch` - create a file/change the timestamp on an already existent file
* `rm` - remove/delete a file

```bash
touch already_existent.txt # Assuming already_existent.txt is an existing
                           # file, then this changes the timestamp on it.
touch new_file1.txt # Assuming new_file1.txt doesn't exist, this creates a
                    # file named new_file1.txt in the current directory.
touch new_file2.txt new_file3.txt # Assuming that both new_file2.txt and
                                  # new_file3.txt don't exist, this creates
                                  # them in the current working directory.
```

```bash
rm file1.txt # Delete file1.txt
rm file2.txt file3.txt # Delete both file2.txt and file3.txt
```

## Creating and Removing Directories

* `mkdir` - create a directory
* `rmdir` - remove a Directory

```bash
mkdir new_dir1 # Create new directory called new_dir1 in the current directory
mkdir new_dir2 new_dir3 # Create new directories called new_dir2 and new_dir3
                        # in the current directory.
```

```bash
rmdir empty_dir # Delete the empty directory called empty_dir
```

If the directory we want to delete is not empty, and **we are sure**
that we want to delete it, then we can add a **recursive** option to the
`rm` command from above:

```bash
rm -r nonempty_dir # Recursively deletes all files in the nonempty_dir,
                   # and then deletes the nonempty_dir itself.
```

## Moving files and Directories

* `cp` - copy files and directories
* `mv` - move and rename files and directories

```bash
cp file1.txt file2.txt # Copy file1.txt to a new file called file2.txt
cp file1.txt directory1 # Copy file1.txt to directory1, keeping it named
                        # as file1.txt within directory1.
cp file1.txt directory1/file11.txt # Copy file1.txt to directory1, but
                                   # name the copy file11.txt.
cp -r dir1 dir2 # Copy dir1 and all its concents into dir2.  
```

```bash
mv file1.txt file2.txt # Move the contents of file1.txt to file2.txt. This
                       # effectively just renames file1.txt to file2.txt.
mv dir1 dir2 # Renames dir1 to dir2 if dir2 doesn't exit, and otherwise
             # moves dir1 into dir2.
```

`mv` will overwrite files if they already exist. If `file2.txt` had already existed in the above, then it would have been overwritten with the contents of `file1.txt`.

[**Back to Index**](README.md)
