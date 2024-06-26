# A Guide to Essential Git Commands

 - **Git is a free and open source distributed version control system.**
 - **Git’s purpose is to keep track of projects and files as they change over time with changes happening from different users.**

# List of some important git commands

1. `git init` - **Initialize a new git repository**

    - **Usage**:

      ```bash
      $ git init
      Initialized empty Git repository in [path].
      ``` 

2. `git config` - **Configure git settings**

    - **Usage**:

      ```bash
      $ git config --global user.name "Your Name"
      $ git config --global user.email "name@example.com"
      ```

    - **Flags (Frequently used)** :

      - `--global` - **Configure settings for all the repo**
      - `--local` - **Configure settings for the current repo**
      - `--list` - **List all the configurations**

    - You can learn more about it [here](https://www.atlassian.com/git/tutorials/setting-up-a-repository/git-config)

3. `git add` - **Add files to the staging area**

    - **Staging Area**:
      - Preview the changes before committing.
      - You can verify the tracked and untracked files.

    - **Usage**:
      

      ```bash
      $ git add file1 file2
      #Add the mentioned files
      
      $ git add .
      # Add all files
      ```

4. `git status` - **Show the status of the repository**

    - **Usage**:

      ```bash
      $ git status
      ```

      You may get a similar output like this. It shows which are the tracked and untracked files.

      ![status](./assets/git/Screenshot%20from%202024-06-26%2021-36-02.png)

      > [!NOTE]
      > You can always remove tracked files using `git rm --cached file_name`


5. `git commit` - **Commit changes to the repository**

6. `git push` - **Push changes to a remote branch**

7. `git pull` - **Pull changes from a remote branch**

8. `git clone` - **Clone a repository**

9. `git remote` - **Manage remote repositories**

10. `git branch` - **Manage branches**

11. `git merge` - **Merge branches**

12. `git log` - **View the commit history**

13. `git checkout` - **Switch branches**

14. `git reset` - **Reset the index and working tree to match the HEAD commit**

# Advanced commands

