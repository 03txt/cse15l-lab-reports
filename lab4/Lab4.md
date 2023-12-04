# Lab Report 4: Vim 

### Step 1: Setup: Delete any existing forks of the repository you have on your account
### Step 2: Setup: Fork the repository
### Step 3: The real deal Start the timer!
### Step 4: Log into ieng6: 
- Keys Pressed: ```<CTRL> 'R' 'ssh cse' <TAB> <ENTER>```
- I searched for the  command using my bash terminal hisotry by typing the beginning of the command.
![image](sshlogin)
### Step 5: Clone your fork of the repository from your Github account 
- Keys Pressed ```'ssh' <CTRL> 'v'```
- I had previously copied the SSH URL from github so I just copy and pasted into the terminal.
- ![image](sshclone)

### Step 6: Run the tests, demonstating they fail 
- Keys Pressed: ```bash test.sh```
- I merely typed out the command to run the script. 
![image](testfailreal)

### Step 7: Editing the File: vim ListExamples.java 
- Keys pressed: ```'50'<down> <up><up><up><up>'e' 'x' 'i' in insert mode: 2 <ESC> ':wq'```
- I jumped down 50 lines to the end of the file and went back up 4 lines. I pressed 'e' to reach the end of the first word which was '1' of 'index1'. Then I deleted '1', by using 'x' and then entered insert mode by clicking 'i'. I inserted '2' at the end of 'index'.
![image](vimedit)

### Step 8: Run the tests, demonstrating that they now succeed
- Keys Pressed: ```<up><up>```
- I had used the command two steps prior so I just used the up arrow twice to access it.
![image](testsuccess)

### Step 9: Commit and push the resulting change to your Github account (you can pick any commit message!)
- Keys Pressed: ```<CTRL> 'R' 'git ad' <TAB> <ENTER>``` & ```<CTRL> 'R' 'git com' <TAB> <backspace><backspace><backspace><backspace> 'fixed bugs' <ENTER>``` & ```<CTRL> 'R' 'git pu' <TAB> <ENTER>```
- I searched for all these commands using the bash terminal history. For the commit command, I changed the messages to "fixed bugs".

![image](gitcommitpush)
