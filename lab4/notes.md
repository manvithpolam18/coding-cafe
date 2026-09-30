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

9.  You now have two commits. Without looking it up: what are the four steps of the loop you just did twice?
Ans. 1. Edit – Make changes or create new files in your working directory.
2. Stage – Use `git add` to select and track those changes in the staging area.
3. Commit – Run `git commit` to save a permanent snapshot to your local history.
4. Verify – Check `git status` or `git log` to confirm your changes were saved.

10. Why does this file get a special name and a special place, rather than being called notes.md like everything else?
Ans. `README.md` is the standard "front door" of any software repository. When anyone opens your project on GitHub, the site automatically renders this file directly on the main page as the project's documentation. While `notes.md` is just for internal lab answers, `README.md` lives at the root so both visitors and developer tools instantly know what the project does and how it's organized.

11. What did gh auth login do that means you will not be asked for a password when you push?
Ans. `gh auth login` authenticated my machine by generating a secure Personal Access Token (PAT) or OAuth token on GitHub and storing it locally in my Git credential helper.
When I push, Git automatically sends this stored token instead of requiring me to manually type my username and password every time.

12. Refresh the repository page on GitHub. What is showing on the front page, and why that file?
Ans. On the front page, GitHub displays your repository files along with the rendered preview of your **`README.md`** file right below them.
GitHub automatically looks for a root `README.md` file whenever a repository page is opened. It renders this file on the landing page so visitors and collaborators can immediately read the project's documentation and structure without having to open individual files.

13. Run git log --oneline again. Did pushing change your local history in any way?
Ans. Running  git log --oneline again won't see any difference even if you use pushing. 
Pushing simply uploads a copy of your existing local commits to the remote repository on GitHub and updates your tracking reference (origin/main now points to your latest commit). Your commit hashes, order, and commit messages remain completely identical locally.

14. Your repository is private but your TAs can now read it. In your own words, what is the difference between a repository being private and a repository not existing on GitHub at all?
Ans. A private repository exists on GitHub with all your files and commit history intact, but access is restricted exclusively to you and invited collaborators. If a repository does not exist at all, no code or history is stored on GitHub, making it impossible for anyone to view or access it.