# Learnings

command prompt use for github.

1.goto gitbash or type
        cmd> git

2.create a local repository and then sync with the github web respository
        cmd>$ git clone https://github.com/KomathiK22/Learnings.git

3. check remote respositry version
        cmd>git remote -v
        cmd> git <command> -h - gives the help onthe given command
         cmd>echo Hello World! > Readme.md
   
4.git add . [adds all the files with the changes to the staging area]
       cmd>git add .
   
5. git commit -commits  has a hashKey so its always available and can be reverted, but always remains with same hashKey
        cmd> $ git commit -m "initial Commit from gitbash"
Error-----------------
Author identity unknown
*** Please tell me who you are.
Run
  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
to set your account's default identity.
Omit --global to set the identity only in this repository.
fatal: unable to auto-detect email address (got 'komat@LAPTOP-F4QG0KCM.(none)')
komat@LAPTOP-F4QG0KCM MINGW64 /c/MyGitRepo/Learnings (main)
        cmd> $ git config --global user.email "komathi.kandregula@gmail.com"
komat@LAPTOP-F4QG0KCM MINGW64 /c/MyGitRepo/Learnings (main)
        cmd>$ git config --global user.name "komathi"

6.git log  - gives us an overview of commits done so far
        cmd>$ git log
commit 80ebef4f4f4810b0ed1b78c76d9e2072a01526c6 (HEAD -> main)
Author: komathi <komathi.kandregula@gmail.com>
Date:   Wed Jan 8 11:09:51 2025 -0600
    initial Commit from gitbash
commit fbb7211e0ed3104b6c161a3ecd401868c55927b3 (origin/main, origin/HEAD)
Author: KomathiK22 <komathi.kandregula@gmail.com>
Date:   Wed Jan 8 10:32:58 2025 -0600
    Initial commit
    
7. Get the latest from the branch on github- push - send latest from repo, fetch the latest from the branch
       cmd>
8. staging - staging means marking files to be committed, git add will add all the files to the github repo
9. git add file1.text file2.txt file3.txt  -- adds one or more files to staging
sample commands:
        cmd>$echo staged > stagedFile.txt
        cmd>$echo unstaged >unstagedFile.txt
        cmd>$git add. stagedFile.txt
        cmd>$git status  - gives an overview of stage and commited/uncommited files
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   stagedFile.txt
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        unstagedFile.txt
10.git reset, to remove one or more files from stagging
        cmd>git reset   
11.create branches and work on them
        cmd> $git branch -- shows/Displayes all the branches in the current reporsitoy
        cmd> $git branch featureBranch --creates  name featureBranch
        cmd> $echo branch featureBranch > testFileCheckBranch.txt
        cmd> $git add .
        cmd> $git commit -m "Main branch commit test"
11. command to change the branches
        cmd> git checkout <branchName>
        cmd> git log
        
13. checking status and inspecting commands
        cmd> git show <commit-hashkey>   [-- gives extensive commit info]
        cmd  git show --name-only <hashkey>   [gies showrthand commit info]
        cmd> git reflog  [gives info about all commits on all branches]
15. push and pull  -git collaboration commands, sends commits to central reposity
        cmd>git push  - works if the new branches are aligned with remote repo else take the path and run below command
        cmd> git push --set-upstream origin featureBranch    [adds featureBranch to the origin path]
16. create new repo and file, then push the changes to git.
        cmd> cd.. to new folder
        cmd> git clone <git url> <new SpringBootMicroservices reponame>
        cmd> cd <new SpringBootMicroservices folder>
        cmd> git branch springBootMicroservices
        cmd> git checkout springBootMicroservices
        cmd> echo branch springBootMicroservice > "Hello World.java"
        cmd> git add .
        cmd> git commit -m "Firts checking to the springBootMicroservices Repository"
        cmd> git log   [ u should see ur results]
        cmd> git push --set-updateStream origin SpringBootMicroservices
        cmd> cd.. /learnings[different repo]
17. pull  -git collaboration commands  , retrives commits from central repository to the local project
        cmd> cd to old folder for the new repo
        cmd> git pull
        cmd> git log
18. Undo/Redo Changes
        cmd> git revert <hashkey>   [ creates new commit to undo whats done in the previous commit] use when on multipls users working on same branch/report for backtracking the commits. creates new commit to undo changes 
        cmd> git reset <hashkey>    [resets the current branch to shows only the commits upto the one we indicate inm <commit hashkey>]
        cmd> git reset --soft <hashkey>   [ disregards subsiquent commits but keeps the changes done to them, this default]  -- removes the commits from history but keeps changes
        cmd> git reset --hard <hashkey>    [ disregards subsiquent commits including the changes done to them]  - removes commits and changes from the history
20. merging the branches
    cmd> cd learnings [ other repo]
    cmd> git merge springBootMicroservices

21. conflicts resolutions, can happen when same files gets modified by different users same time
   cmd> navigate to repo folder
   cmd> git branch
   cmd> git push -f  [force override of the remote one]
   cmd> git checkout featureBranch
   cmd> git push -u origin featureBranch
   cmd> echo new commit > newCommit.txt
   cmd> git add.
   cmd> git commit -m "New Commit"
   cmd> git push
 

    
   
