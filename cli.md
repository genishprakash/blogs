# A Guide to Essential CLI Commands

**The Command Line Interface (CLI) is a tool for interacting with your operating system.This is a guide to some of the most commonly used CLI commands.**

## Navigating File System

1. `pwd` - **Print the working directory**
   - **Usage**:

     ```bash
     $ pwd
     home/user
     ```

2. `ls` - **List all files in the current directory**
   - **Usage**:

     ```bash
     $ ls # ls command used in home directory.

     Desktop Documents  Downloads     
     ```

   - **Flags**:
     - `-a` - **List all files including hidden files**
     - `-S` - **Sort files in size order**
     - `-d` - **List all directories**
     - `-l` - **List all files with detailed information**<br>

     These are some important flags which used with the ls command. You also learn in detail by visiting this [documentation](https://www.geeksforgeeks.org/ls-command-in-linux/).

     
       
3. `cd` - **Change directory**
   - **Usage**:

     ```bash
     $ cd directory_name 
     ```
     `cd`   ->   used to move forward to the child directory.

     ```bash
     $ cd ..
     ```
     `cd ..` _->_ used to move backward to the parent directory.

     ```bash
     $ cd ~
     ```
      `cd ~` -> used to move to the home directory.
     
   - **Relative paths**

     ```bash
     $ cd ./directory_name/subdirectory_name
     ```
     You can also use [relative paths](https://www.codingrooms.com/blog/file-paths) to move to a certain folder.
    
   - **Absolute paths**

     ```bash
     $ cd ~/directory_name/subdirectory_name
     ```
     A sample command using [absolute path](https://www.educative.io/answers/what-is-absolute-path).

## Managing Files and Directories

1. `touch` - **Create a new file**
   - **Usage**: 

     ```bash
     $ touch file_name
     ```
     This is the syntax to create a file.

2. `mkdir` - **Create a new directory**
   - **Usage**:

     ```bash
     $ mkdir directory_name
     ```
     This is the syntax to create a directory.
   
   - **Flags**:
      - `-p` - **Create parent directories if they do not exist**

        ```bash
        $ mkdir -p directory_name/subdirectory_name
        ```
        This is the most commonly used flag . You can learn more about it [here](https://www.geeksforgeeks.org/mkdir-command-in-linux-with-examples/).
3. `rmdir` - **Remove a directory**
   - **Usage**:

     ```bash
     $ rmdir directory_name
     ```
     This is the syntax to remove a directory.

     If you want to ***remove a directory which contains files***, you can use this command.

     ```bash
     $ rm -r directory_name
     ```
4. `rm` - **Remove a file** 
   - **Usage**:

     ```bash
     $ rm file_name
     ```
     This is the syntax to remove a file. You can learn more about it [here](https://www.ibm.com/docs/en/power6?topic=commands-rm-command).

5. `cp` - **Copy a file**
   - **Usage**:

     ```bash
     $ cp file_name destination
     ```
     This is the syntax to copy a file.

6. `mv` - **Move a file**
   - **Usage**: 

     ```bash
     $ mv file_name destination
     ```
     This is the syntax to move a file.To rename a file you can also use this command.

## Viewing and Editing files

1. `cat` - **View a file**
   - **Usage**:

     ```bash
     $ cat file_name
     ```
     This is the syntax to view a file.

     ```bash
     $ cat > file_name
     #Create a new file

     $ cat file_name1 >> file_name2
     #Append the contents of file_name1 to file_name2

     $ cat -n file_name
     #View a file with line numbers
     ```

     These are some stuffs used with cat commands. You can learn more about it [here](https://www.geeksforgeeks.org/cat-command-in-linux-with-examples/).

2. `vi` , `nano` - **Edit a file**
   - **Usage**:

     ```bash
     $ vi file_name

     $ nano file_name
     ```

      There are lot more commands for editing files. You can learn more about it [here](https://www.geeksforgeeks.org/how-to-edit-text-files-in-linux/).

3. `head` - **View the first 10 lines of a file**
   - **Usage**: 

     ```bash
     $ head file_name
     #View the first 10 lines of a file

     $ head -n 10 file_name
     #You can also specify the number of lines you want to view.
     ```
4. `tail` - **View the last 10 lines of a file**
   - **Usage**:

     ```bash
     $ tail file_name
     #View the last 10 lines of a file
     $ tail -n 10 file_name
     #You can also specify the number of lines you want to view.
     ```
5. `less` , `more` - **View a file in a detailed manner**
   - **Usage**:

     ```bash
     $ less file_name
     
     $ more file_name
     
     ```
    - **Differences**
      - `more`: forward navigation and limited backward navigation.<br>
      - `less`: both forward and backward navigation and also has search options. You can go to the beginning and the end of a file instantly. 
    
## Some Useful Commands 

1. `man` - **View a manual page**
   - **Usage**:

     ```bash
     $ man command_name
     #You view the manual page for every commands
     #Example usage
     $ man ls
     ```
2. `wc` - **Count the number of lines, words, and characters in a file**
   - **Usage**:

     ```bash
     $ wc file_name
     ```
     - **Flags (Frequently used)**:
     - `-c` -> **Count the number of characters**
     - `-l` -> **Count the number of lines**
     - `-w` -> **Count the number of words**

     You can learn more about it [here](https://www.geeksforgeeks.org/wc-command-linux-examples/)

3. `history` - **View the command history**
   - **Usage**:

     ```bash
     $ history
     ```
    

## Network commands

1. `ping` - **Ping an IP address**
   - **Usage**:

     ```bash
     $ ping google.com
     # Checks the network connectivity to specific server.
     ```
2. `ifconfig` - **View wired network information**
   - **Usage**: 

     ```bash
     $ ifconfig
     # Displays the ip address and more stuffs related to network connection.
     ```
3. `iwconfig` - **View wireless network information**   
   - **Usage**:

     ```bash
     $ iwconfig
     ```
4. `ssh` - **Securely connect to a remote server**

   - **Usage**: 

     ```bash
     $ ssh [username]@[hostname or IP address]
     ```
5. `netstat` - **Network Statistics**
   - **Usage**:

     ```bash
     $ netstat
     ```
   - **Flags**:
     - `-a` -> **List all network connections**
     - `-l` -> **List all listening ports**
     - `-at`-> **List all network connections with TCP ports**
     - `au` -> **List all network connections with UDP ports**

     You can learn more about it [here](https://www.geeksforgeeks.org/netstat-command-linux/).

## OS,Process Commands

1. `ps` - **List all processes**   
   - **Usage**:

     ```bash
     $ ps
     ```
   - **Flags (Commonly Used)**:
     - `-ef` -> **List all the process of the entire system with parent pid**
     - `-aux` ->**List all the process with the CPU and memory usage**  
2. `pstree` - **List all processes in a tree format**
   - **Usage**:

     ```bash
     $ pstree
     ```
     This image shows the senior most process with the sub process.

     ![pstree](./assets/Screenshot%20from%202024-06-25%2018-22-18.png)
3. `top` - **View running processes**
   - **Usage**:

     ```bash
     $ top
     #This command is used to view the running processes.
     ```
4. `df` - **View disk usage**
   - **Usage**:
     ```bash
     $ df -h
     #This command with -h is used ofter to display in human readable format.
     ```    
5. `uname` - **Unix name**

   - **Usage**:

     ```bash
     $ uname
     #Displays information about the system.
     ```
    - **Flags**:
      - `-a` -> **Display all information**

      You can learn more about it [here](https://www.geeksforgeeks.org/uname-command-in-linux-with-examples/)
6. `free` - **View memory usage**
   - **Usage**:
     ```bash
     $ free -h
     #Displays memory usage in human readable format.
     ```
7. `lspci` - **List all the PCI devices**
   - **Usage**:

     ```bash
     $ lspci
     #displaying information about PCI buses in the system and devices connected to them..
     ```
8. `kill` - **Kill a process**
   - **Usage**:

     ```bash
     $ kill [pid]
     ```
    - ** Flags**:
       - `-9` -> **Kill the process forcefully**
       - `-15` -> **Kill the process gracefully**

       You can learn more about it [here](https://www.geeksforgeeks.org/kill-command-in-linux-with-examples/)

## File permission 

1. `chmod` - **Change file permission**
   - **Usage**:

     ```bash
     $ chmod [permission] file_name
     ```
   - **Arguments**:
     - `ugo` -> **User, Group and Others**
     ```bash
     $ chmod u+rwx g+rwx o+rwx file_name
     #The user,group,others have read,write and execute the file.You can modify the permission.
     ```
   - **Binary Flags**
     - Read (4) - Write (2) - Execute (1) the values are represented like this.

     ```bash
     $ chmod 755 file_name
     #The file will be readable,writeable and executable for user and readable, executable for group and other.
     ```
     ![chmod](./assets/vkxuqbatopk21.jpeg)

     - You can learn more about [here](https://www.geeksforgeeks.org/chmod-command-linux/)

2. `chown` - **Change file owner**
   - **Usage**:

     ```bash
     $ chown new_owner[:new_group] file_name
     ```
    - **Flags (Frequently used)**:
       - `-R` -> **Change the owner of the files and its subdirectories**

3. `sudo` - **Run a command as root user**
   - **Usage**:

     ```bash
     $ sudo command
     # Gives you the root user privileges.

     #Example usage
     $ sudo apt-get update
     ```

## Package manager

1. `apt-get` - **Install a package**
   - **Usage**:

     ```bash
     $ sudo apt-get install package_name
     #root user privileges are used to install a package.
     ```
     
## Searching Finding and Manipulating data

1. `grep` - **Search and manipulating text patterns in a file**

   - **Usage**: 

     ```bash
     $ grep [pattern] file_name
     ```
   - **Flags (Frequently Used)**:
     - `-i` -> **Case insensitive**
     - `-l` -> **List the files that contain the pattern**
     - `-o` -> **Print only the matched pattern**

     You can learn more about it [here](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
2. `sort` - **Sort a file**

   - **Usage**:

     ```bash
     $ sort file_name
     ```
    - **Flags (Frequently used)**:
       - `-r` -> **Reverse the order of the sort**
       - `-u` -> **Remove duplicate lines**
3. `find` - **Find files**

   - **Usage**:

     ```bash
     $ find [path] [type]-name pattern
     #Example command . Use type if necessary. 
     $ find . -name '*.txt'
     ```
    - **Flags (Frequently used)**:
       - `-name` -> **Find files with the pattern**

       You can learn more about it [here](https://www.geeksforgeeks.org/find-command-in-linux/)

## Bash Related Commands

1. Pipe Operator `|` - **Combines the list of commands**

   - **Usage**:

     ```bash
     #The first command output is passed to the second command.
     $ command1 | command2
     ```
    - Example usage:
    
      ```bash    
      $ cat filename | sort
      ```
2. `printenv` - **Print environment variables**

   - **Usage**: 

     ```bash
     $ printenv
     #Print all the environment variables.
     ```
3. `xargs` - **Execute commands from a input**

   - **Usage**: 

     ```bash
     $ xargs command
     ```

     
   - **Example usage**

     ```bash
     $ pgrep firefox | xargs kill -9

     $ find . -name "*.txt" | xargs rm

     #xargs get input from previous command and execute it.
     ```
4. `sed` - **Search replace filtering text in a file and much more stuffs**

   - **Usage**:

     ```bash
     $ sed 's/searchString/replaceString/' file_name
     # s-String 

     $ sed '1,2p' file_name
     # Print the first two lines.
     ```
   - It can do much more other stuffs .You can learn from [here](https://www.geeksforgeeks.org/sed-command-in-linux-unix-with-examples/).

5. `awk` - **Search and manipulate text patterns in a file**

   - **Usage**:

     ```bash
     $ awk 'pattern' file_name
     ```
   - **Arguments (Frequently used)**:
     - NR -> **Get the line number**
     - NF -> **Get the number of fields**
     
   - **Example usage**

     ```bash
     $ awk '{print $0,$1}' file_name
     # Print the first and second columns.
     ```

     It is similar to sed . There are lot more useful patterns.You can learn from [here](https://www.geeksforgeeks.org/awk-command-unixlinux-examples/). 

## Conclusion

- These are some useful commands for a Software Engineer who just started with linux. 

- I hope you like this article.