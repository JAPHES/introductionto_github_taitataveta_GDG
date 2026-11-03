# Introduction to GitHub: Taita Taveta GDG

## Initialize a Repository

- Run `git init` to initialize Git in your working directory.
- Git creates a hidden directory that stores:
  - The information needed to track your files.
  - Special references used to manage the repository.

## Configure Your Git User

- Add your name and email address to your Git installation.
- This configuration is saved on your local workstation.
- Git uses these details to identify who created each commit.
- Configure your details with:

  ```bash
  git config --global user.name "Joe Example"
  git config --global user.email "joe@example.com"
  ```

## Use the Staging Index

- Add a specific file to the staging index:

  ```bash
  git add file.txt
  ```

- Add all files from a subdirectory:

  ```bash
  git add assets/*
  ```

- Add all changes in the working directory:

  ```bash
  git add -A
  ```

- Add new and modified files from the current directory:

  ```bash
  git add .
  ```

## Check the Status of Your Files

- Use `git status` to see which files are:
  - Tracked.
  - Untracked.
  - Modified.
  - Staged for a commit.

  ```bash
  git status
  ```

## Commit Changes

- A commit adds staged changes to the permanent history of the project.
- Commit your staged changes with a short, descriptive message:

  ```bash
  git commit -m "Added new test feature"
  ```

### Stage and Commit Tracked Files Automatically

- Use the `-a` option to stage changes to files that Git already tracks and commit them.
- New, untracked files must still be added with `git add` first.

  ```bash
  git commit -am "Added new test feature"
  ```

- Push the branch to the remote repository and set its upstream branch:

  ```bash
  git push -u origin master
  ```

## Create a New Local Branch

- Create a branch named `staging` and switch to it:

  ```bash
  git checkout -b staging
  ```

- View all local branches:

  ```bash
  git branch
  ```

## Push a New Branch to the Remote Repository

- Push the new `staging` branch to the remote repository:

  ```bash
  git push origin staging
  ```

- Set the remote `staging` branch as the upstream branch for your local branch:

  ```bash
  git push -u origin staging
  ```

- After setting the upstream branch, Git can track changes between the local and remote `staging` branches.
