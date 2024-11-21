### **Task List: Focused on Repository Management, Commits, Branching, and Merging**

### **Part 1: Creating and Cloning Repositories**

#### **Task 1: Create a Local Git Repository**
1. Create a new project folder:  
   ```bash
   mkdir MyProject
   cd MyProject
   ```
* Answer:- Make new folder name MyProject and go to the folder and initialize it repo.

2. Initialize it as a Git repository:  
   ```bash
   git init
   ```
* Answer:- initialize folder.

3. Verify the repository status:  
   ```bash
   git status
   ```
* Answer:- this command shows the current state of the working directory and staging area. also tells that which files are modifieded,untracked,stage for commit.

#### **Task 2: Clone a Remote Repository**
1. Clone a GitHub repository:  
   ```bash
   git clone https://github.com/username/repo.git
   ```
* Answer:- Download repo to local system.  

2. Verify the cloned repository structure:  
   ```bash
   cd repo
   ls -a
   ```
 * Answer:- ls -a command lists all files and directories in the current directory, including hidden files.
---

### **Part 2: Understanding Commits and Commit Messages**

#### **Task 3: Commit Changes Locally**
1. Create a new file and add content:  
   ```bash
   echo "Welcome to Git" > README.md
   ```
 * Answer :- Create a new file with content "Welcome to Git".

2. Stage the file:  
   ```bash
   git add README.md
   ```
 * Answer :- Stage the file.

3. Commit the staged file:  
   ```bash
   git commit -m "Initial commit: Added README.md"
   ```
 * Answer :- this command save the current state of the repository with a message describing the change.

#### **Task 4: Write Effective Commit Messages**
1. Create a detailed commit message:  
   ```bash
   git commit -m "Added initial version of README.md with project overview"
   ```

2. Commit multiple files with one message:  
    
        touch file1.txt file2.txt
* Answer :- touch use for make multiple files at once.
      
        git add .
* Answer :- Stage all files.
    
        git commit -m "Added two new files for feature setup"
* Answer :- commit both file with proper message.
---

### **Part 3: Viewing Commit History with `git log`**

#### **Task 5: View Detailed Commit History**
1. View full commit logs:  
   ```bash
   git log
   ```
* Answer :- This command shows a detailed list of commits with hash, author, date, and message.

2. View commit history in a compact format:  
   ```bash
   git log --oneline
   ```
* Answer :- this command condenses the commit history into a single line per commit for quick review.

#### **Task 6: Customize Log Outputs**
1. View logs with a graphical representation:  
   ```bash
   git log --oneline --graph --decorate
   ```
* Answer :- 

  --oneline:this command shows each commit as a single line, including a shortened commit hash and message.

  --graph: this command adds a graphical representation of the commit history, including branch and merge relationships.

  --decorate: this command shows references such as branch names, tags, or HEAD pointers.

2. Filter logs for a specific file:  
   ```bash
   git log README.md
   ```
* Answer :- this command show the commits that modified the file README.md.

---

### **Part 4: Understanding Branching and Merging**

#### **Task 7: Understanding Branching**
1. List all branches:  
   ```bash
   git branch
   ```
* Answer :- this command Displays the current branch and all other branches.

2. Create a new branch:  
   ```bash
   git branch feature-branch
   ```
* Answer :- Creates a new branch without switching to it.

3. Switch to the new branch:  
   ```bash
   git checkout feature-branch
   ```
* Answer :- Switch to feature-branch.

   - **Alternative Command**:  
     ```bash
     git checkout -b feature-branch
     ```
     * Answer :- Creates and switches to the branch in one command.

---

### **Part 5: Creating and Working with Branches**

#### **Task 8: Make Changes in a Branch**
1. Add content to a file in the new branch:  
   ```bash
   echo "Feature in progress" > feature.txt
   git add feature.txt
   git commit -m "Added feature.txt in feature-branch"
   ```
* Answer :- create new file with added some text,stage it and commit file.

#### **Task 9: Merging Branches**
1. Switch back to the `main` branch:  
   ```bash
   git checkout main
   ```
* Answer :- switch to main branch from feature-branch.

2. Merge the `feature-branch` into `main`:  
   ```bash
   git merge feature-branch
   ```
* Answer :- merge branches means combines the changes from `feature-branch` into `main`.

---

### **Part 6: Resolving Merge Conflicts**

#### **Task 10: Simulate a Merge Conflict**
1. Modify the same line in a file on two branches:  
   ```bash
   echo "Main branch content" > conflict.txt
   git add conflict.txt
   git commit -m "Added conflict.txt in main branch"
   ```
* Answer :- make first change in file ,stage the file and commit it.

2. Switch to the other branch and make conflicting changes:  
   ```bash
   git checkout feature-branch
   echo "Feature branch content" > conflict.txt
   git add conflict.txt
   git commit -m "Modified conflict.txt in feature-branch"
   ```
* Answer :- make second change in file ,stage the file and commit it.

3. Merge `feature-branch` into `main`:  
   ```bash
   git checkout main
   git merge feature-branch
   ```
* Answer :- switch to main branch and merge it with feature-branch.

4. Resolve the conflict by editing the file and choosing the correct version:  
   - Open `conflict.txt` and decide which changes to keep.
   - Stage the resolved file:  
     ```bash
     git add conflict.txt
     ```
   - Commit the merge:  
     ```bash
     git commit -m "Resolved conflict in conflict.txt"
     ```
* Answer :- in conflict.txt decided which changes are commit,stage the resolved file and commit it with message.

---

### **Part 7: Deleting and Renaming Branches**

#### **Task 11: Delete a Branch**
1. Delete a local branch:  
   ```bash
   git branch -d feature-branch
   ```
* Answer :- this command deletes the branch safely,but it's only when it has been fully merged.

2. Force-delete a branch:  
   ```bash
   git branch -D feature-branch
   ```
* Answer :- this command deletes the branch forcibly ,even it hasn't been fully merged.which also do some data lose.

#### **Task 12: Rename a Branch**
1. Rename the current branch:  
   ```bash
   git branch -m new-branch-name
   ```
* Answer :- rename the current branch.

2. Rename another branch (not checked out):  
   ```bash
   git branch -m old-branch-name new-branch-name
   ```
* Answer :- rename old branch without switch to it.
---
