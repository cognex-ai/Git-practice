# Git Cheat Sheet

## Basic Concepts
- **Commit:** Represents a specific state of your codebase, like a snapshot of your files at a certain point in time.
- **Branch:** A parallel version of your repository that enables you to work on different versions of your code simultaneously.
- **Tag:** A label used to mark specific points in Git history, often used to indicate release versions.
- **HEAD:** A reference to the most recent commit in the branch you are currently working on.

## Git Configuration
- `git config --global user.name “Your Name”`: Sets the username that will be attached to your commits and tags for identification.
- `git config --global user.email “you@example.com”`: Sets the email address that will be associated with your commits for contact purposes.
- `git config --global color.ui auto`: Enables helpful colorization of Git output for better readability.

## Starting a Project
- `git init [project name]`: Initializes a new Git repository, creating a new directory with the given project name.
- `git clone <project url>`: Copies an existing Git repository from a remote server to your local machine.
- `git rm [file]`: Removes a file from both the working directory and the staging area, preparing it for deletion from the repository.

## Day-to-Day Work
- `git status`: Displays the current state of your working directory and staging area, showing which changes are ready to be committed.
- `git add [file]`: Adds specific changes from the working directory to the staging area, preparing them to be included in the next commit.
- `git diff [file]`: Shows the differences between the current state of the file in the working directory and the version in the staging area.

## Storing Your Work
- `git stash`: Temporarily stores changes that are not ready to be committed, allowing you to work on something else before coming back to them.
- `git stash pop`: Retrieves the most recently stashed changes and applies them to your working directory, removing them from the stash.
- `git stash drop`: Discards the most recently stashed changes, removing them from the stash permanently.

## Git Branching Model
- `git branch [-a]`: Lists all the local branches in your repository, providing an overview of the different branches you have.
- `git branch [branch_name]`: Creates a new branch with the given name, allowing you to work on a new feature or experiment without affecting the main codebase.
- `git rebase [branch_name]`: Incorporates changes from one branch into another, making the branch's commit history appear linear.
- `git checkout [-b] [branch_name]`: Switches to the specified branch, creating it if it doesn't already exist.

## Inspect History
- `git log [-n count]`: Shows the commit history of the current branch, with the option to limit the number of displayed commits.
- `git log --oneline --graph --decorate`: Provides a compact visualization of the commit history, including a graph representation and reference labels.
- `git log ref`: Displays a list of commits that exist on the current branch but have not been merged into the specified reference.

## Tagging Commits
- `git tag`: Lists all the tags in the repository, providing an overview of the different tagged versions or milestones in the project.
- `git tag [name] [commit sha]`: Creates a new tag with the specified name for the given commit, allowing you to mark specific points in your project's history.

## Reverting Changes
- `git reset [--hard] [target reference]`: Resets the current branch to the specified target reference, potentially discarding all changes.
- `git revert [commit sha]`: Creates a new commit that undoes the changes made in the specified commit, allowing you to safely remove changes without altering the commit history.

## Synchronizing Repositories
- `git fetch [remote]`: Retrieves the latest changes from the remote repository, allowing you to review them before merging.
- `git pull [remote]`: Fetches the latest changes from the remote repository and automatically merges them into your current branch.
- `git push [--tags] [remote]`: Sends your local commits to the remote repository, updating the remote branch with your latest changes.

## Ignoring Files
To ignore specific files, you can create a `.gitignore` file in your repository, listing patterns for files you want Git to ignore. For example, to ignore all files in a directory named "logs" except for a file named `.gitkeep`, you can use the following pattern:
