# Git Basic Knowledge Assignment

## Step 1: Setup Git Repository

### Initialize a new Git repository
```bash
mkdir my_project
cd my_project
git init
```
**Explanation:** This initializes a new Git repository in the `my_project` folder. Git will now track changes in this directory.

### Screenshot
![Initialize Git repository](<Screenshot 2024-05-24 at 4.05.43 PM.png>)

### Create a file named `README.md`
```bash
echo "# My Project" > README.md
```
**Explanation:** This command creates a `README.md` file and adds a brief description to it.

### Screenshot
![Create README.md](<Screenshot 2024-05-24 at 4.09.02 PM.png>)

### Stage and commit the `README.md` file
```bash
git add README.md
git commit -m "Initial commit with README.md"
```
**Explanation:** Staging (`git add`) prepares the file to be committed, and committing (`git commit`) saves the snapshot of the file to the repository.

### Screenshot
![Stage and commit README.md](<Screenshot 2024-05-24 at 4.10.52 PM.png>)

## Step 2: Making Changes and Version Control

### Create a new branch named `feature-1`
```bash
git branch feature-1
```
**Explanation:** This command creates a new branch called `feature-1`.

### Screenshot
![Create branch feature-1](image.png)

### Switch to the `feature-1` branch
```bash
git checkout feature-1
```
**Explanation:** This switches the current working branch to `feature-1`.

### Screenshot
![Switch to branch feature-1](image.png)

### Add a new file named `app.py`
```python
# app.py
print("Hello, World!")
```
```bash
echo 'print("Hello, World!")' > app.py
git add app.py
git commit -m "Add app.py with Hello, World! script"
```
**Explanation:** This creates a new Python file, stages it, and commits it to the `feature-1` branch.

### Screenshot
![Add app.py](<Screenshot 2024-05-24 at 4.12.22 PM.png>)

### Modify the `app.py` file
```python
# app.py
def print_name():
    print("Your Name")

print("Hello, World!")
print_name()
```
```bash
echo 'def print_name():\n    print("Your Name")\n\nprint("Hello, World!")\nprint_name()' > app.py
git add app.py
git commit -m "Add function to print name"
```
**Explanation:** This modifies the `app.py` file, stages the changes, and commits them to the `feature-1` branch.

### Screenshot
![Modify app.py](<Screenshot 2024-05-24 at 4.13.21 PM.png>)

## Step 3: Merging Branches

### Switch back to the main branch
```bash
git checkout main
```
**Explanation:** This switches the working branch back to `main`.

### Screenshot
![Switch back to main branch](<Screenshot 2024-05-24 at 4.14.07 PM.png>)

### Merge the `feature-1` branch into the main branch
```bash
git merge feature-1
```
**Explanation:** This merges the changes from `feature-1` into `main`. Resolve any conflicts if they arise.

### Screenshot
![Merge feature-1 into main](<Screenshot 2024-05-24 at 4.14.12 PM.png>)
## Step 4: Using GitHub

### Create a new repository on GitHub named `my_project`
- Go to GitHub, create a new repository named `my_project`.

### Screenshot
![Create GitHub repository](<Screenshot 2024-05-24 at 4.15.29 PM.png>)

### Push the local `my_project` repository to GitHub
```bash
git remote add origin https://github.com/yourusername/my_project.git
git push -u origin main
```
**Explanation:** This sets the remote repository and pushes the local repository to GitHub.

### Screenshot
![Push to GitHub](<Screenshot 2024-05-24 at 4.30.55 PM.png>)
![Github Repo](<Screenshot 2024-05-24 at 4.30.28 PM.png>)

### Ensure both `main` and `feature-1` branches are available on the remote repository
```bash
git push origin feature-1
```
**Explanation:** This pushes the `feature-1` branch to GitHub.

### Screenshot
![Push feature-1 to GitHub](path_to_push_feature_1_to_github_screenshot)

## Step 5: Collaboration Simulation

### Create another branch named `bugfix-1`
```bash
git branch bugfix-1
git checkout bugfix-1
```
**Explanation:** Creates and switches to the `bugfix-1` branch.

### Screenshot
![Create and switch to bugfix-1 branch](path_to_create_and_switch_to_bugfix_1_branch_screenshot)

### Simulate a bug fix
```python
# Corrected typo in the function name
def print_name():
    print("Your Corrected Name")
```
```bash
echo 'def print_name():\n    print("Your Corrected Name")\n\nprint("Hello, World!")\nprint_name()' > app.py
git add app.py
git commit -m "Fix typo in print_name function"
```
**Explanation:** This corrects a typo, stages the changes, and commits them.

### Screenshot
![Simulate bug fix](path_to_simulate_bug_fix_screenshot)

### Push the `bugfix-1` branch to the remote repository
```bash
git push origin bugfix-1
```
**Explanation:** This pushes the `bugfix-1` branch to GitHub.

### Screenshot
![Push bugfix-1 to GitHub](path_to_push_bugfix_1_to_github_screenshot)

### Open a pull request on GitHub to merge `bugfix-1` into `main`
- Go to GitHub, open a pull request from `bugfix-1` to `main`.

### Screenshot
![Open pull request](path_to_open_pull_request_screenshot)

### Complete the pull request
- Merge the pull request on GitHub.

### Screenshot
![Complete pull request](path_to_complete_pull_request_screenshot)

## Step 6: History and Reversion

### Viewing the Commit History
```bash
git log
```
**Explanation:** The `git log` command shows a list of commits in the current branch, with each commit's unique hash, author, date, and commit message. This helps you review the history of changes in your project.

### Screenshot
![View commit history](path_to_view_commit_history_screenshot)

### Reverting the Last Commit
```bash
git checkout main
git revert HEAD
```
**Explanation:** The `git revert HEAD` command creates a new commit that undoes the changes introduced by the most recent commit (`HEAD`). This is useful if you realize that the last commit introduced a mistake or an unwanted change.

### Screenshot
![Revert last commit](path_to_revert_last_commit_screenshot)

### Undoing the Revert
```bash
git reset --hard HEAD~1
```
**Explanation:** The `git reset --hard HEAD~1` command moves the current branch pointer and the working directory to the previous commit, effectively removing the revert commit and restoring the project to its state before the revert.

### Screenshot
![Undo revert](path_to_undo_revert_screenshot)

### Issues Encountered

- No significant issues were encountered during this step.
- The commands executed successfully, and the changes were reflected as expected.


### Instructions:
1. Replace the placeholder `path_to_*_screenshot` with the actual paths to your screenshots.
2. Ensure all explanations and screenshots are correctly added.
3. Save and commit your `Git_Assignment_Report.md` file.
4. Push the changes to your GitHub repository.
