1. What did --global mean here? What would happen if you left it out? Guess, then check with man git-config or ask. 

Ans. --global saves your configuration across all Git repositories on your account (in ~/.gitconfig). Without it, settings apply only to the current project, which fails with fatal: not in a git directory if you aren't inside a Git repository. 

2. What appeared in ls -a but not in ls? What is inside it? 

Ans. In ls -a, hidden items starting with a dot appeared: .git, .venv, . (current folder), and .. (parent folder). Inside .git, Git stores version history and configuration, including project settings, active branch pointers, branches, and saved file snapshots. 

3. Roughly how many files and folders is Git offering to track? Does anything in that list look like something you did not write? 

Ans. Git is offering to track 2 items  

File: README.md 

Folder: week02/ (the trailing slash / indicates it is a directory) 

4. Compare this git status with the one from Question 3. What disappeared? 

Ans. Nothing disappeared because .venv was already ignored or hidden in the initial status. However, .gitignore was added to the untracked files list. 

5. .gitignore itself shows up as untracked. Should it be committed, or ignored too? Why? 

Ans.  It should be committed. Committing .gitignore ensures every team member and environment automatically uses the same rules to ignore unwanted files. 

6. README.md moved from one heading to another in the git status output. Which two? In the three-places model from the session, what just happened to it? 

README.md moved from Untracked files to Changes to be committed. In the three-places model, it moved from the Working Directory to the Staging Area. 

 

7. What did Git print after the commit? How many files did it say changed? 

Ans. Git printed the branch name, root commit status, commit hash (e0426bb), and commit message, followed by the insertion count and list of created files. It stated that 4 files changed. 

 

8. What are the first seven characters of your commit called, and what are they for? 

Ans. They are called the short commit hash (or short SHA-1). They serve as a unique ID to identify and reference that specific commit in Git commands. 

9. 

 

 

 

 

 