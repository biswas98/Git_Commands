# Git Command

### Useful Git commands

- ### To change the email id in git:
  ```sh
  git config --global user.email "email_id"
  ```
- ### To change the username in git:
  ```sh
  git config --global user.name "name"
  ```
- ### To change both Username & Email at the same time:
  ```sh
  git config --global --edit
  ```
- ### For command help:

  ```sh
  git --help
  ```

- ### To initialize git inside a directory:
  ```sh
  git init
  ```
- ### To check the status of the git directory:

  ```sh
  git status
  ```

  or

  ```sh
  git status -s     #short status
  ```

- ### To add a new code files to the `staging area`:

  ```sh
  git add file_name
  ```

  or

  ```sh
  git add .     # add all files
  ```

- ### Remove new code files from `staging area`:

  ```sh
  git reset file_name
  ```

  or

  ```sh
  git reset .   # remove all files
  ```

- ### To commit the files which is are in the `staging area`:
  ```sh
  git commit -m "commit message"
  ```
- ### Directly add & commit the files at the same time:
  ```sh
  git commit -am "commit message"
  ```
- ### To displays the commit history of the current branch in your Git repository:
  ```sh
  git log
  ```
- ### Compare working directory to the last commit:
  ```sh
  git diff
  ```
- ### If you don't want to track certain files create a `.gitignore` file and add the files which you don't want git to track:
  ```sh
  touch .gitignore
  ```
- ### Create a new branch:
  ```sh
  git branch <branch_name>
  ```
  For example:
  ```sh
  git branch feature_branch
  ```
- ### Switch to newly created branch:

  ```sh
  git checkout <branch_name>
  ```

  For example:

  ```sh
  git checkout feature_branch
  ```

- ### Create and switch to newly created branch at the same time:

  ```sh
  git checkout -b <branch_name>
  ```

  For example:

  ```sh
  git checkout -b feature_branch
  ```

- ### If you want to merge one branch to another branch:

  - ### First checkout to the branch you want to merge:
    ```sh
    git checkout main   # supposedly "main" is the branch where I want to merge
    ```
  - ### Then merge the branch with below mention command:
    ```sh
    git merge feature_branch
    ```

- ### If you want to stash your current code progress:
  ```sh
    git stash
  ```
- ### To retrieve your stashed code:
  ```sh
    git stash pop
  ```
- ### To add a new remote repository(hosted on internet) to your Git project(local):

  ```sh
    git remote add <remote_name> <url>
  ```

  For example:

  ```sh
   git remote add origin https://github.com/user69/test_git_command.git
  ```

  > _Note: generally remote_name is `origin` by default._

- ### To change the URL of an existing remote repositor which is useful if the URL of the remote repository has changed, or if you want to switch from using HTTPS to SSH (or vice versa):

  ```sh
    git remote set-url origin <new_url>
  ```

  For example:

  ```sh
   git remote set-url origin https://github.com/new_user69/bhai_ka_repo.git
  ```

- ### To check your remote's name:

  ```sh
    git remote
  ```

- ### To show both the fetch and push URLs for each remote:

  ```sh
    git remote -v
  ```

- ### To remove a remote repository from your local Git repository's configuration, which is useful if you no longer need to fetch or push to that remote, or if you've replaced it with a different remote:

  ```sh
  git remote rm origin
  ```

- ### To push your local branch to a remote repository and set the upstream (tracking) branch. This simplifies future push and pull commands because you won't need to specify the remote and branch name each time:

  ```sh
  git push -u origin branch_name
  ```

  or

  ```sh
  git push --set-upstream origin branch_name
  ```

  > _Note: after setting the the upstream we can use `git push` & `git pull` directly._

- ### Pull from a specific remote and branch:
  ```sh
  git pull <remote> <branch>
  ```
  For example:
  ```sh
  git pull origin develop
  ```
  If, we have already set up tracking, we can only use:
  ```sh
  git pull
  ```
