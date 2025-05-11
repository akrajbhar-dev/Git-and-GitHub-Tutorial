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
7. `git add`:- This command will add changes to staging area.
	1. `git add <file1.txt> <file2.text`:- Add Changes manually one by one.
	2. `git add .`:- Add all the changes at the same time.
8. `git rm --cached <file>`:- This command will unstage changes which are staged by `git add` command.
9. `git commit -m "message"`:- This command will commit a change and send the changes to repo.
10. `git log`:- This command will list all the commits made.
	1. `git log --oneline`:- `git log` command with --oneline flag will simplify the list of commits made.
# Terminologies
1. Repositories :- Same meaning as folder or directory, Specifically where we store our code.
2. Git Repositories :- A repo which have .git(files/folders starting with . are hidden) folder inside it, is called a Git Repositories.
3. Atomic Commits :- It is a concept of committing the changes when a unit of work is done and to write the message with commit in Present tense , Imperative.
# Work Flow with Git
**Working Directory**-->`git init`-->**Git Repository**-->`git add`-->**Staging Area**-->`git commit`-->**Repo**-->`git push`-->**GitHub**