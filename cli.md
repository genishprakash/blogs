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
     cd  is used to move forward to the child directory.

     ```bash
     $ cd ..
     ```
     cd .. is used to move backward to the parent directory.

     ```bash
     $ cd ~
     ```
      cd ~ is used to move to the home directory.
     
   - **Relative paths**

     ```bash
     $ cd ./directory_name/subdirectory_name
     ```
     We can also use [relative paths](https://www.codingrooms.com/blog/file-paths) to move to a certain folder.
    
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
3. 'rmdir' - **Remove a directory**
   - **Usage**:

     ```bash
     $ rmdir directory_name
     ```
     This is the syntax to remove a directory.

     If we want to ***remove a directory which contains files***, we can use this command.

     ```bash
     $ rm -r directory_name
     ```
4. 'rm' - **Remove a file** 
   - **Usage**:

     ```bash
     $ rm file_name
     ```
     This is the syntax to remove a file. You can learn more about it [here](https://www.ibm.com/docs/en/power6?topic=commands-rm-command).

5. 'cp' - **Copy a file**
   - **Usage**:

     ```bash
     $ cp file_name destination
     ```
     This is the syntax to copy a file.

6. 'mv' - **Move a file**
   - **Usage**: 

     ```bash
     $ mv file_name destination
     ```
     This is the syntax to move a file.To rename a file we can also use this command.

