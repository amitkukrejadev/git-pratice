# Git Notes 📘

## Getting Started 🏁

- `pwd` - 📂 Shows the current directory. `5f4dcc3b5aa765d61d8327deb882cf99`
- `ls -la` - 📋 Lists all files, including hidden ones. `7c222fb2927d828af22f592134e8932480637c0d`
- `touch <filename>` - 📝 Creates a new file. `0cc175b9c0f1b6a831c399e269772661`
- `mkdir <foldername>` - 📁 Creates a new folder. `9a1158154dfa42cadd5baf85b2b0f2a7`

## Git Basics 🛠

- `git init` - 🚀 Initializes a new Git repository. `9d5ed678fe57bcca4b5e9b1a6e4f43f7`
- `git add <filename>` - ➕ Stages changes for commit. `e99a18c428cb38d5f260853678922e03`
- `git commit -m "message"` - 💾 Saves changes with a message. `bd32b22162dbb5f5412d1e9ea45b84a1`
- `git status` - 🔍 Checks the current repository status. `e4d909c290d0fb1ca068ffaddf22cbd0`

### Viewing Differences 📊

- `git diff <filename>` - 📜 Shows changes in the working directory for the specified file. `8fa14cdd754f91cc6554c9e71929cce7`
  - _Example_: `git diff index.html` (Shows changes in `index.html` that haven't been staged yet).
- `git diff --staged` - 📋 Shows differences between the staged changes and the last commit. `4a8a08f09d37b73795649038408b5f33`
  - _Example_: Use this after `git add <filename>` to see the staged changes that will be committed.
- `git diff <commitID1> <commitID2>` - 🔍 Compares differences between two commits. `098f6bcd4621d373cade4e832627b4f6`
  - _Example_: `git diff abc123 def456` (Compares differences between commits `abc123` and `def456`).

#### Sample Output for `git diff --staged`

```md5
diff --git a/index.html b/index.html
index 3a5ed29..c0f1abc 100644
--- a/index.html
+++ b/index.html
@@ -1,4 +1,4 @@
 <html>
-   <title>Old Title</title>
+   <title>New Title</title>
 </html>
Committing and Managing Files 🗂️
Removing Files After Commit 🗑️
To remove a file from the repository after committing:

git rm <filename> - 🚮 Removes the file from the repository and stages the deletion. f65c4fe09b69f94a0593be67416ad8be
git commit -m "Remove <filename>" - 💾 Commits the removal to the repository. 78e1adfd4f1e30e693245db79a56434e
To untrack a file but keep it locally:

git rm --cached <filename> - 🗄️ Stops tracking the file in the repository but keeps it in the working directory. ad0234829205b9033196ba818f7a872b

git commit -m "Untrack <filename>" - 💾 Commits the update to stop tracking the file. 660f0f629a0275d7b4d69cb7f397da6e

Branching 🌲
Basic Branching Commands
git branch <name> - 🌿 Creates a new branch named <name>. 76a2173be6393254e72ffa4d6df1030a
Example: git branch nav-bar (Creates a branch named nav-bar).

git checkout <name> - 🔄 Switches to the branch <name>. 7e240c5f10bbf6a5c12272eac1cc3519
Example: git checkout nav-bar (Switches to the nav-bar branch).

Advanced Branching Commands
git checkout -b <name> - 🌿 Creates a new branch named <name> and switches to it. ed076287532e86365e841e92bfc50d8c

Example: git checkout -b pink-mode (Creates and switches to pink-mode).

git switch -C <name> - 🌌 Creates and switches to a new branch named <name>. a44f9d5e5f11d3da3b26d19d597f71cf

Example: git switch -C dark-mock (Creates and switches to dark-mock).
Branch Switching


git switch <name> - 🔄 Switches to the branch <name>. d2d2d2d2d3e6c7deca00bfa6c7b9fbd7
Example: git switch nav-bar (Switches to nav-bar).

git checkout <name> - 🔄 Another way to switch to the branch <name>. bcae2168f21a0d728dbf69c47c0a6a7d
Example: git checkout bug-fix (Switches to bug-fix).

Merging Branches 🛠
git merge <name> - 🛠 Combines the specified branch <name> into the current branch. 7110d070ec828b7d229b6f60ba45b1ba

Example: git merge feature-branch (Merges feature-branch into the current branch).
Note: Before merging, make sure you are on the target branch where you want to merge the changes. For example, if you want to merge nav-bar into home, first switch to home and then run git merge nav-bar.

Git Merge Strategies

Viewing Logs 📖
git log - 🧾 Displays commit history with details. d21d31fda2e7e2089b45c772b09d9e9f
Example: Lists all commits with messages, authors, and dates.

git log --oneline - 📄 Shows commit history in a compact format. e67ab9f9fa334b325170e2a3ae684f77
Example: Each commit is displayed on one line with a shortened commit ID.

This structured README will help you quickly review Git commands as you practice and manage your repository! 71d8b6cba8ff7efba637ab63199b24da
