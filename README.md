# git-commands

If you have already pushed the changes to a remote repository and need to revert some files, it's generally not recommended to modify the commit history directly, especially if others have already pulled the changes. Instead, you can create a new commit that undoes the changes you want to revert. Here are the steps:


**1.Identify the commit hash:**
Use git log to find the hash of the commit you want to revert.

**git log**

Note the commit hash of the specific commit.

**3. Revert the changes but don't commit immediately:**
Use the git revert command with the -n option to stage changes without committing.

**git revert -n <commit-hash>**

**4. Unstage the changes you don't want to revert:**
Use git reset to unstage the changes you don't want to revert.

**git reset path/to/unwanted/file1 path/to/unwanted/file2**

Replace path/to/unwanted/file1, path/to/unwanted/file2, etc., with the paths of the files you want to keep unchanged.

**5. Commit the changes:**
Commit the changes using git commit.

**git commit -m "Revert changes to specific files"**

**6. Push the new branch (optional but recommended):**
If you created a new branch, push it to the remote repository.

