# Git and GitHub
Git is a free and open-source [[version control system]] where as GitHub is the most popular hosting website for git repositories.
# Usage of Git
Git is used for taking history of changes of our code. It also helps us for collaboration by making a system where multiple people can work on same project and someone else code does not bother other people's.
# Git Commands
1. `git --version`:- executing this command on terminal will display the version of Git installed on the local machine.
2. `git status`:- displays the status of the repo, you are currently in.
3. `git config --global user.email "your-email@example.com`:- this command will set a global configuration about your email, When we push to git repo hosting sites it will registry in commits who committed the change.
4. `git config --global user.name "Your Name"`:- this command will set a global configuration about your user name, When we push to git repo hosting sites it will registry in commits who committed the change.
	**Configuration can be set to a particular repo also but the --global flag will set the change for all git repos.**
5. `git config --list`:- This command will list the changes made in configuration of git.
6. `git init`:- This command will create .git folder in present working directory(pwd) and Git is ready to track any change inside that Git repo.
7. `git config --global init.defaultBranch <name>`:- This command will change the default branch name globally.
	The preset default branch name is master, but using the above command will change default branch name to whatever we choose to be.  
	When we initialize Git in new folder, It will create branch in that Git repo by the default branch name.
8. `git add`:- This command will add changes to staging area.
	1. `git add <file1.txt> <file2.text`:- Add Changes manually one by one.
	2. `git add .`:- Add all the changes at the same time.
9. `git rm --cached <file>`:- This command will unstage changes which are staged by `git add` command.
10. `git commit -m "message"`:- This command will commit a change and send the changes to repo.
11. `git log`:- This command will list all the commits made.
	1. `git log --oneline`:- `git log` command with --oneline flag will simplify the list of commits made.
12. `git config --global core.editor "code --wait`:- This command will change the Git's default code editor from VIM to VS Code.
	**code is command to open VS Code, And code \<file\> will create 'file' if not existed and open up the 'file' with VS Code.**  
	**Git open up code editor, When you did not type message while committing and when solving conflicts.**
13. `git branch`:- This command displays the current branch where we are working on.
14. `git branch 'Branch Name'`:- This command creates a new branch with the given name.
15. `git switch 'Branch Name'`:- This command will take the user from current branch to the branch you typed.
16. `git switch -c <branch name>`:- This command will both create and switch to new branch.
	If branch already exists, Above command will only switch to it.
17. `git checkout <Branch Name>`:- This command will also switch to given branch. But this command has multi-purpose like restore etc.
18. `git merge <branch name>`:- This command will merge the \<branch name\> commits(changes) to the current branch.
# Terminologies
1. Repositories :- Same meaning as folder or directory, Specifically where we store our code.
2. Git Repositories :- A repo which have .git(files/folders starting with . are hidden) folder inside it, is called a Git Repositories.
3. Atomic Commits :- It is a concept of committing the changes when a unit of work is done and to write the message with commit in Present tense , Imperative.
# Work Flow with Git
**Working Directory**-->`git init`-->**Git Repository**-->`git add`-->**Staging Area**-->`git commit`-->**Repo**-->`git push`-->**GitHub**
****
**We create a file with file name `.gitignore` and we will paste the file names which we want to get ignored by Git.**
****
**Git does not track empty folders, If we want the empty folders are also being tracked by Git then we add `.gitkeep` file inside those empty folders.**
****
# Head in Git
The head is a pointer which points towards the current branch on which we are working.
**There are multiple ways to know the current branch.**
1. By `git branch` command.
2. By going to .git/HEAD, This is a txt file.
3. By going to .git/refs/heads, In this folder the branches are listed and when we open each branch txt file, It has ever commits' unique hash ID.
# Branches
We can create multiple branches in a git repository. When we create a branch, The newly created branch will have all the files and folder of the current branch. After that when we do some changes in a branch, Nothing will be changed in other branches until we merge two or more branches.
# Merge
Two or more branches can be merged with `git merge <branch name>` command.  
Merge will bring all the work of a branch which is typed with `git merge` to the branch user is currently at. But the branch which is being merge is not deleted, It stays same.  
Sometimes merge will create conflicts which comes when both branch will have different new commits in a same file.
**There are two types of merges.**
1. Fast-forward merge :- When one branch does not have any new commits after creation/merge to the other branch and only the other branch have new commits and In that other branch, There is no deletions in any commits. Then if when we merge that other branch to the current branch, There will be no conflicts.
2. Non fast-forward merge :-
	1. When we work on two or more branches simultaneously, But not in same file. Then if we merge those branches there will be no conflicts but Git will ask for a message to merge those branches and we will also get an extra commit.
	2. This time we work in same file from different branches. When merging those branches, We will get conflicts and we need to resolve those.