## Category

### What commands do I execute every morning?
```
$ git remote -v
$ git fetch -p --all
$ git status
$ git branch -avv
```

### How do I change default editor into vim?
`$ git config --global core.editor "vim"`

### What is difference between long and short hashes?
- https://stackoverflow.com/questions/43665836/in-git-what-is-the-difference-between-long-and-short-hashes
- Long hash is checksum of hex of length 40 using SHA-1 hash function

### How do I skip log-in when `git push`?
- Switch remote URL from HTTPS to SSH: https://help.github.com/en/github/using-git/changing-a-remotes-url

### How do I extract submodule from existing project?
- https://github.blog/2016-02-01-working-with-submodules/
- https://git-scm.com/book/id/v2/Git-Tools-Submodules
- https://stackoverflow.com/questions/6031494/git-submodules-and-ssh-access

### How do I diff visually?
- https://git-scm.com/docs/git-difftool

### How do I use short commands?
- https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases
- Not possible to use same verb: https://stackoverflow.com/questions/5916565/define-git-alias-with-the-same-name-to-shadow-original-command/16410521

### Where is configuration file?
`~/.gitconfig`: https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup

### What is HEAD?
HEAD is a reference to the last commit in the currently check-out branch. You can think of the HEAD as the "current branch". When you switch branches with git checkout, the HEAD revision changes to point to the tip of the new branch.
- http://researchhubs.com/post/computing/git/what-is-HEAD-in-git.html
- https://stackoverflow.com/questions/354312/why-is-origin-head-shown-when-running-git-branch-r

### How do I create new branch from another branch?
`git checkout -b <new_branch> [<start point>]`
- https://git-scm.com/docs/git-checkout#Documentation/git-checkout.txt-emgitcheckoutem-b-Bltnewbranchgtltstartpointgt

### How do I see log?
`git log --decorate --oneline --graph`

### Does `git log` show another branch's latest commit?
No, `git log` shows log until the current branch's HEAD if you don't add `--all` or `--branches`.
- https://git-scm.com/docs/git-log#Documentation/git-log.txt---all

### How do I duplicate a repository?
- https://help.github.com/en/github/creating-cloning-and-archiving-repositories/duplicating-a-repository

### How do I check merged branch?
`$ git branch --merged`: https://git-scm.com/book/en/v2/Git-Branching-Branch-Management
- https://stackoverflow.com/questions/226976/how-can-i-know-if-a-branch-has-been-already-merged-into-master

### How do I delete remote branch?
`$ git push <remote_name> :<branch_name>`
- https://stackoverflow.com/questions/2003505/how-do-i-delete-a-git-branch-locally-and-remotely

### Can I merge branch-a into branch-b on branch-c without checkout branch-b?
Impossible (because a working copy is needed to resolve any potential conflicts): https://stackoverflow.com/questions/3216360/merge-update-and-pull-git-branches-without-using-checkouts

### How do I recover when I merged wrong branch by mistake (e.g. upstream/release → master)?
`$ git reset --hard upstream/master`
- https://stackoverflow.com/questions/19271058/git-merge-mistake

### How do I resolve merge conflict?
- https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-using-the-command-line

### How do I undo `git reset`?
`$ git reset HEAD@{1}`
- https://stackoverflow.com/questions/2510276/how-to-undo-git-reset
- https://stackoverflow.com/questions/2221658/whats-the-difference-between-head-and-head-in-git
- https://stackoverflow.com/questions/26785118/head-vs-head-vs-head-also-known-as-tilde-vs-caret-vs-at-sign/26785200

### Why `git branch -d <branch>` says "not fully merged" although the commits were merged into master?
- https://stackoverflow.com/questions/5412599/git-is-stating-a-branch-is-not-merged-after-rebasing-why
- https://git-scm.com/book/en/v2/Git-Branching-Rebasing
