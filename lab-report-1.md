# Lab Report 1 - Remote Access and File System 
## cd command
The 'cd' command, short for "Change Directory", is a command used to switch between directories and change the current working directory.
#### No Arugments  
* Working in the '/home' directory, using the 'cd' command with no arguments does not produce an output or change in the current working directory, as shown below:
```
[user@sahara ~]$ cd
```
* The resulting line, rather the lack thereof, is due to a lack of specification of the directory the user wants to use as their new working directory. Since no argument/directory name is provided, the working directory remains the same.  
####  Using a Path to a Directory 
* Using the command with a path to a directory causes a change in the user's working directory. In our example, we begin in the '/home' directory, use the command 'cd' followed by a relative path to the directory 'lecture1'. The working directory is then changed to 'lecture1', and is shown as follows:
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ 
```
* *It is important to note that this does not cause error because 'lecture1' is directly within the home directory.*  
####  Using a Path to a File 
* Now working in the directory 'lecture1' and using the command with a realtive path to a file, the terminal prints an error given that the command is only used for directories. The message looks as follows: 
```
[user@sahara ~/lecture1]$ cd README
bash: cd: README: Not a directory
```
## ls command
The 'ls' command, short for "List", is a command used to print out the list of files and directories within a given path.
#### No Arugments 
* Working in the '/home' directory, using the 'ls' command with no arguments returns the list of files amd directories, as shown below:
```
[user@sahara ~]$ ls 
lecture1
```
* This can be intepretted as the '/home' directory only containing one directory named 'lecture1'.
####  Using a Path to a Directory 
