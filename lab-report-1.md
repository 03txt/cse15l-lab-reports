# Lab Report 1 - Remote Access and File System 
## cd command
The 'cd' command, short for "Change Directory", is a command used to switch between directories and change the current working directory.
#### No Arugments  
* Working in the '/home' directory, using the 'cd' command with no arguments does not produce an output or change in the current working directory, as shown below:
```
[user@sahara ~]$ cd
```
* The resulting line, rather the lack thereof, is due to a lack of specification of the directory the user wants to use as their new working directory. Since no argument/directory name is provided, the working directory remains the same.  
#### Using a Path to a Directory 
* Using the command with a path to a directory causes a change in the user's working directory. In our example, we begin in the '/home' directory, use the command 'cd' followed by a relative path to the directory 'lecture1'. The working directory is then changed to 'lecture1', and is shown as follows:
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ 
```
* *It is important to note that this does not cause error because 'lecture1' is directly within the home directory.*  
#### Using a Path to a File 
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
#### Using a Path to a Directory 
* Working in the '/home', using the 'ls' command with a relative path to a directory will also print out a list of files and other directories in the directory referenced. For example, if we provide a relative path to lecture1, it will print out the following:
```
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
```
* *Again, it is important to note that this does not cause error because 'lecture1' is directly within the home directory.*  
#### Using a Path to a File 
* Working in the '/home' directory and using a relative path to a file will return the relative path provided as an argument as shown below:
  ```
  [user@sahara ~]$ ls lecture1/messages/zh-cn.txt
  lecture1/messages/zh-cn.txt
  ```
* This behavior occurs regardless of the directory you are in. In the following example, we switch to the 'lecture1' directory and retry the 'ls' command with a relative path to the 'README' file:
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ ls README
README
```
## cat command
The 'cat' command, short for "Concatenate", which is used to print out the contents of one or more files. 
#### No Arugments 
* Working in the '/home/ directory and using the command with no arguments results in error and looks as follows: 
```
[user@sahara ~]$ cat
^C
```
* Although not stated explicitly, there is an error at runtime as the command does not output anything nor does it display an error message.
#### Using a Path to a Directory 
* Using the command with a path to a directory results in a message stating that the relative provided references a directory. In our example, we begin in the '/home' directory, use the command followed by a relative path to the directory 'lecture1'. Terminal prints the following:
```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
```
#### Using a Path to a File
* Working in the '/home' directory and using a relative path to a file will return the contents of the referenced file, for example:
```
[user@sahara ~]$ cat lecture1/README
To use this program:

javac Hello.java
java Hello messages/en-us.txt
```

* This command also works for multiple files as well. For example, when switching to the messages directory and using a relative paths to mutiple files, it will printout the contents of the files:

```
[user@sahara ~]$ cd lecture1/messages
[user@sahara ~/lecture1/messages]$ cat en-us.txt zh-cn.tx
t
Hello World!
你好世界
```

* *The content for both files are combined into one input as seen above.*

