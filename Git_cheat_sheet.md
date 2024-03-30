## Git Cheat Sheet

* **Setup**
    * `git config --global user.name "Your Name"`: Sets your name for Git commits
    * `git config --global user.email "your_email@example.com"`: Sets your email address for Git commits
* **Init**
    * `git init <directory>`: Creates a new Git repository in the specified directory
    * `git clone <url>`: Clones an existing Git repository from the specified URL
* **Branches**
    * `git branch`: Lists all local branches
    * `git branch <branch_name>`: Creates a new branch
    * `git checkout <branch_name>`: Switches to a different branch
    * `git checkout -b <branch_name>`: Creates a new branch and switches to it
    * `git merge <branch_name>`: Merges a branch into the current branch
    * `git branch -d <branch_name>`: Deletes a local branch (can only be deleted if already merged)
    * `git branch -D <branch_name>`: Deletes a local branch (can be deleted even if not merged)
* **Stashing**
    * `git stash`: Saves your current changes without committing them
    * `git stash list`: Lists all stashes
    * `git stash apply`: Applies the most recent stash
    * `git stash drop`: Deletes the most recent stash
* **Rebasing**
    * `git rebase <branch_name>`: Rebases the current branch onto another branch
* **Status**
    * `git status`: Shows the status of your working directory
* **Adding and Committing**
    * `git add <file>`: Adds a file to the staging area
    * `git commit -m "<message>"`: Commits the changes in the staging area with a message
* **Diff**
    * `git diff`: Shows the difference between your working directory and the staging area
* **Remote**
    * `git remote add <alias> <url>`: Adds a remote repository
    * `git remote show <alias>`: Shows information about a remote repository
    * `git remote remove <alias>`: Removes a remote repository
    * `git fetch <alias>`: Downloads all branches from the remote repository without merging them
    * `git pull <alias>`: Fetches changes from the remote repository and merges them into the current branch

This is not an exhaustive list of all the Git commands, but it should give you a good starting point for learning how to use Git. For more information on Git, you can refer to the official Git documentation [https://git-scm.com/doc](https://git-scm.com/doc).

**Remote Repositories (Forking & Pull Requests):**

 * Forking: Create a copy of a repository on your account for modifications.
 * Cloning a Fork: Clone your forked repository to work on it locally.
 * Pushing Changes: Use git push to upload local commits to your remote repository.
 * Pull Requests: Submit proposed changes from your fork for review and merging.

**Collaboration:**

 * Issues: Track bugs, feature requests, and discussions.
 * Pull Requests: Collaborate on code changes through code review and comments.
 * Wiki: Create collaborative knowledge base for your project.

**Markdown:**

***Use Markdown for formatting text in README files, comments, and issues.***
*Headers (#, ##, ###)
*Bold and italics with ** or _
*Lists with - or *
*Code blocks with ```
*...and more...

**Additional Resources:**

*Git Basics https://git-scm.com/
*GitHub Guides https://docs.github.com/
*Markdown Tutorial https://www.markdownguide.org/