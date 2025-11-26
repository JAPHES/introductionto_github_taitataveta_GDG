# introductionto_github_taitataveta_GDG

##Initialize Repository
Git init - This command initializes Git functionality in your working directory
         - This “hidden” directory keeps track of the files and special reference markers needed by the Git program

##Configure Your Git User
##Initialize Repository
 -You will first want to make sure that you have added a username to your Git installation
 - This is done on the local workstation.
 - Otherwise, Git will not know what name and email to sign on your commits
 - Git keeps great records, and that part of that process involves knowing who is contributing what.
          - git config --global user.name "Joe Example"
          - git config --global user.email joe@example.com
   
##The Staging Index
   -You will constantly find yourself adding files to the staging index in Git.
   -You will be both adding new files for tracking and adding modifications to files that are already being tracked.
   - To add a new file for tracking, use the “add” command followed by the name of the file
       # git add file.txt "this is for adding files by their names"
-There will likely be occasions in which you will want to add the full contents of a sub-directory to the staging index.
       # git add assets/*
- You can also add the entire contents of your working directory to staging with the “add” command followed by the -A option.
       # git add -A
- If you have already added files to tracking and only want to record modifications without adding new files, you can use the “add” command followed by the . option.
     # git add .
##Checking the Status of Your Files
- This can tell you which files are being tracked, not tracked, or modified.
  # git status
##Commit Changes in Git
-Committing tracked files to the repository means that we are adding changes to the permanent record of the project.
#To commit the changes you’ve made, you will only need to run a simple command in your terminal.
   #git commit -m "Added new test feature"
### Automatically Adding Changes
- git add .
- git commit -am "Added new test feature"
- git push origin -u master


####Create a New Branch Locally
- To create a new local branch and switch to it, you can use the checkout command. For this example, we will presume you want to name the new branch “staging”
  ##git checkout -b staging
- You now have a new branch called “staging” and you can view all branches with the git branch command as below:
  ##git branch
###Push New Branch To Remote and Set as Upstream
The Git push command is the first one you will want to run, effectively placing your new branch on the remote repository:
    #git push origin staging
--Then, while the branch is still checked out, you can set it an “upstream” branch for it, which means the local branch will be tracking its remote counterpart for changes instead of the master branch:
   git push origin -u staging
  
