---
layout: post

title: Git Command at Work

tags: [Git]

comments: true
---



# Git Command at Work

## Vocab：
Staged: `git add`  
Committed : `git commit`   
Snapshot: a certain commit  
Untracked files: a file that is not staged  
Track a file: adding it to git, then `git status` can track it  
Index: files are staged  
Detached head: checkout an earlier commit history  

## Common Cases and Command
1. `git commit -a filename`: 
   add modified file automatically, then commit  
Short for the two-step command: git add & git commit  
Be careful, it is only for any tracked files, not for new files   

2. `git status`  
    It shows changes that have been staged, changes that haven't,
    and files that are untracked    
    `git status -s`: shorter version
     - ??: New files   
     - A:file has been staged for next commit  
     - MM: modified file that has already been staged before  
     - AM: staged and before commiting, modified again  

3. `git blame filename`  
    check out in lines what has been changed

4. check out what are the changes   
   1. local changes, not staged yet（before `git add` command)  
   `git diff`  
   2. local changes, but already staged  
   `git diff --cached`


5. Accidently modified files on the **wrong branch** and not staged yet
   1. want to simply reset it back (throw any changes being made) to the latest commit  
`Git checkout current_wrong_branch modified_file`  
   2. want to keep the changes, but not in this branch
        ```
        git stash 
        git checkout -b new_branch
        git stash apply
        ```
6. Accidently modified files and already staged, want to unstage them but still keep the changes
    ```
    git diff --cached                   #checkout where has been changed in detail
    git restore --staged filename
    ```

 7. Add an .gitignore under the directory in order to never push certain files   
    for instance, client_data.json
    use ! in front to the exception files

8. Committed with typos in commit message or realized some things in code still need to be changed  
   ```
   git reset –-soft HEAD^
   editing codes
   git commit -a -m "now it is fixed"
   ```

9. Merge conflicts    
   1.  no time to fix it: `git reset --hard`  
   2.  already commited and decided to throw it away: `git reset --hard ORIG_HEAD`

10. Delete feature branch after merging  
    `git branch -d`

11. Work along with other team members.Branch out from the master branch, doing some extra work while other people made some changes to the master branch.
  ``` 
  git rebase              #move HEAD to the master branch and apply all changes on my feature branch to it
  solving conflicts 
  git rebase --continue
 ```