# Git Commands Guide

## Introduction to Git

Git is a distributed version control system designed to handle everything from small to very large projects with speed and efficiency. It allows multiple developers to work together on the same codebase, managing changes and ensuring that conflicts between versions are minimized. In a local environment, Git works by creating a ".git" directory in your project, where it keeps all the versioning information. This enables you to track changes, revert to previous states, and manage your project development more effectively.

### How Git Works

At its core, Git operates on a local repository, including all your project's files and history. Changes are committed to this local repository and can be shared with others by pushing to a remote repository.

- **Local Operations**: Create, edit, delete, and organize files in your project. Commit changes to track the evolution of your project.
- **Remote Operations**: Share changes with others, pull updates, and collaborate on projects across the globe.

#### Diagrams

- Insert diagram of Git basic operations: `![Git Basic Operations](https://graphviz.org/Gallery/directed/git.svg)`
- Insert diagram of Git workflow from local to remote: `![Git Workflow](https://res.cloudinary.com/practicaldev/image/fetch/s--M_fHUEqA--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/128hsgntnsu9bww0y8sz.png)`

## Git Commands

This section covers Git commands from basic setup and configuration, to more advanced use cases.

### Setup and Config

- **`git init`**
  - Initializes a new Git repository.
  - `git init`

- **`git config`**
  - Configures user information, email, and other preferences.
  - `git config --global user.name "Your Name"`
  - `git config --global user.email "youremail@example.com"`

### Basic Commands

- **`git clone`**
  - Clones a repository into a new directory.
  - `git clone [URL]`

- **`git add`**
  - Adds file changes in your working directory to your staging area.
  - `git add .`

- **`git commit`**
  - Commits your staged content as a new commit snapshot.
  - `git commit -m "Your commit message"`

- **`git status`**
  - Displays the state of the working directory and staging area.
  - `git status`

- **`git push`**
  - Updates remote refs along with associated objects.
  - `git push origin main`

- **`git pull`**
  - Fetches from and integrates with another repository or a local branch.
  - `git pull origin main`

### Branching and Merging

- **`git branch`**
  - Lists, creates, or deletes branches.
  - `git branch` (list branches)
  - `git branch [branch-name]` (create new branch)

- **`git checkout`**
  - Switches branches or restores working tree files.
  - `git checkout [branch-name]`

- **`git merge`**
  - Joins two or more development histories together.
  - `git merge [branch-name]`

### Advanced Commands

- **`git rebase`**
  - Reapplies commits on top of another base tip.
  - `git rebase main`

- **`git stash`**
  - Temporarily shelves changes so you can work on a different branch.
  - `git stash`

- **`git tag`**
  - Marks specific points in history as important.
  - `git tag [tag-name]`

## Conclusion

Git is a powerful tool for managing software projects, allowing for efficient collaboration and version control. By understanding and utilizing the commands outlined above, developers can effectively manage their development workflows, from basic tasks to more complex operations.
