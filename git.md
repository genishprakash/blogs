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

      >  **Note:** 
      > You can always remove tracked files using `git rm --cached file_name`


5. `git commit` - **Commit changes to the repository**

    - It captures a snapshot of a current modified files.
    - **Usage**:    

      ```bash
      $ git commit -m "commit message"

      #-am flag is used to add and commit only the modified changes
      $ git commit -am "commit message"

      ```  
6. `git clone` - **Clone a repository** 

    - It clones a remote repository into your local machine.

    - **Usage**:

      ```bash
      $ git clone https://github.com/username/repository_name
      ```
7. `git remote` - **Manage remote repositories**

    - **Usage**:

      ```bash
      #Add a origin for a remote branch
      $ git remote add origin https://github.com/username/repository_name

      #Remove a remote branch
      $ git remote remove origin
      ```
    - You can learn more about it [here](https://www.atlassian.com/git/tutorials/syncing)
8. `git push` - **Push changes to a remote branch**

    - `push` command is used to push the changes to a remote branch.
    - **Usage**:    

      ```bash
      $ git push origin branch_name

      #Setting an upstream so that you can use git push next time.
      $ git push origin -u branch_name

      ```
9. `git fetch` - **Fetch changes from a remote branch**

    - It fetches the changes from the remote branch , but doesn't merge them.

    - **Usage**:

      ```bash
      $ git fetch origin branch_name
      ```
10. `git pull` - **Pull changes from a remote branch**

    - `pull` command is used to pull the changes from the remote branch and merge them.

    - **Usage**:

      ```bash
      $ git pull origin branch_name
      ```


11. `git branch` - **Manage branches**

    - **Usage**:

      ```bash
      #Create a new branch
      $ git branch branch_name

      #Delete a branch
      $ git branch -d branch_name
      ```

12. `git merge` - **Merge branches**

    - It merges the changes from one branch to another.

    - **Usage**:

      ```bash
      $ git merge branch_name
      ```
    - **Usecase Scenario**:
      - When a lot of developers are working on various branches. We can merge the changes from one branch to another.
    - **Merge conflicts**

      - When there is a conflict in the merge,you need to resolve it in your text editor and commit the changes and push it.

      - **Example Usage**

        ```bash
        $ git merge branch_name
        #Conflict occurs , resolve it , add and commit
        $ git commit -am "commit message"
        ```
    ![merge](./assets/git/git-three-way-merging.png)

13. `git log`, `git reflog` - **View the commit history**

    - **Usage**:

      ```bash
      #View the commit history of a specific branch
      $ git log

      #View the commit history of all the branches
      $ git reflog
      ```

14. `git checkout`, `git switch` - **Switch branches**

    - **Usage**:

      ```bash
      #Switch to  a branch
      $ git checkout branch_name
      $ git switch branch_name

      #Create a branch
      $ git checkout -b branch_name

      #Delete a branch
      $ git checkout -d branch_name
      ```

15. `git reset`, `git revert`- **Go back to previous state**

    - Both `reset` and `revert` are used to go back to previous state but `revert` creates a ***new commit*** with the previous state and `reset` go back to previous state without creating a new commit.
    ![revert](https://wac-cdn.atlassian.com/dam/jcr:a6a50d78-48e3-4765-8492-9e48dec8fd2f/04%20(2).svg?cdnVersion=1866)
    - **Usage**:

      ```bash
      $ git reset HEAD^
      $ git revert commit_hash
      ```
    - **Frequently used**:
      
      ```bash
      #reset to previous state also force deletes
      $ git reset --hard HEAD^ 
      
      #reset to previous state without deleting the staged files
      $ git reset --soft HEAD~n
      ```

16. `git rebase` - **Rebase a branch**

    - A pretty useful commands which acts  like `git merge`.
    - The main difference is that `rebase` have a straight line of commits.
    - It doesn't create a new commit for conflicts.
    ![rebase](https://wac-cdn.atlassian.com/dam/jcr:4e576671-1b7f-43db-afb5-cf8db8df8e4a/01%20What%20is%20git%20rebase.svg?cdnVersion=1866)

    - **Usage**:

      ```bash
      $ git rebase branch_name

      ##After fixing the conflicts use 
      $ git rebase --continue
      ```
    - **Interactive rebase**

      You can specify the order of commits you want to rebase. 

      ```bash
      $ git rebase -i 
      ```
17. `git stash` - **Stash changes**

    - It is like a temporary storage for a commit.You store those commit and pop them later.
    - **Usage**:

      ```bash
      $ git stash
      ```

    - **Frequently used**:

      ```bash
      #pop the last stash
      $ git stash pop

      #list all the stash
      $ git stash list
      ```
    - You can learn more about it [here](https://www.atlassian.com/git/tutorials/saving-changes/git-stash)
    
18. `git cherry-pick` - **Pick a specific commit**

    - Used to pick a specific commit on other branches and use them to our current branch.
    - **Usage**:

      ```bash
      $ git cherry-pick commit_hash
      ```
    - You can learn more about it [here](https://www.atlassian.com/git/tutorials/cherry-pick)

19. `git diff` - **View changes in a file**
    - Last but the most used and important command.
    - It helps to view all the changes in the file. 

    - **Usage**:

      ```bash
      $ git diff
      ```

## Conclusion

- These are the most common and frequently used comment.
- I hope you like this article.