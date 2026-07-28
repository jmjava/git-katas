# Git Katas Cheatsheet

Quick command reference for the exercises. For situation-based help (“I committed on the wrong branch…”), see [HOWTO.md](HOWTO.md). For shell basics, see [SHELL-BASICS.md](SHELL-BASICS.md).

## Setup & config

```shell
git init
git clone <url>

git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --local  user.name "Repo Name"     # overrides global for this repo
git config --list --show-origin

# Editor
git config --global core.editor nano
# Windows Notepad:
git config --global core.editor notepad
```

Practice: [configure-git](configure-git/README.md), [alias](alias/README.md), [signed-commits](signed-commits/README.md)

## Everyday status

```shell
git status
git diff                    # unstaged changes
git diff --cached           # staged changes (also: --staged)
git diff <branchA> <branchB>
git diff --name-only
git diff --word-diff
```

Practice: [basic-staging](basic-staging/README.md), [diff-advance](diff-advance/README.md)

## Staging & commits

```shell
git add <file>
git add .                   # stage everything in the working tree
git restore --staged <file> # unstage (keep working-tree changes)
git reset <file>            # older unstage spelling

git commit
git commit -m "message"
git commit -a               # stage tracked files + commit
git commit -am "message"
git commit --amend          # rewrite last commit (local only!)
git commit --fixup=<sha>   # mark commit for autosquash rebase
```

Practice: [basic-commits](basic-commits/README.md), [basic-staging](basic-staging/README.md), [amend](amend/README.md), [restore](restore/README.md)

## History

```shell
git log
git log --oneline
git log --oneline --graph --all
git log --pretty=fuller
git log --follow <file>
git log --stat
git log --patch             # or: git log -p
git log branch2..branch1    # reachable from branch1 but not branch2
git show <ref>
```

Handy alias:

```shell
git config --global alias.lol "log --graph --oneline --all"
git lol
```

Practice: [investigation](investigation/README.md), [alias](alias/README.md)

## Branches

```shell
git branch                  # list
git branch <name>           # create
git switch <name>           # switch
git switch -c <name>        # create + switch
git branch -d <name>        # delete (merged)
git branch -D <name>        # force delete
git branch -v
```

Practice: [basic-branching](basic-branching/README.md)

## Merge & rebase

```shell
git merge <branch>
git rebase <branch>
git rebase -i <ref>                 # interactive
git rebase --autosquash -i <ref>    # with fixup/squash commits
git rebase --exec '<cmd>' <ref>     # run a command on each commit
git rebase --continue
git rebase --abort
```

Practice: [ff-merge](ff-merge/README.md), [3-way-merge](3-way-merge/README.md), [merge-conflict](merge-conflict/README.md), [rebase-branch](rebase-branch/README.md), [rebase-multiple-commits](rebase-multiple-commits/README.md), [advanced-rebase-interactive](advanced-rebase-interactive/README.md), [rebase-interactive-autosquash](rebase-interactive-autosquash/README.md)

## Undo safely (public history)

```shell
git revert <ref>            # new commit that undoes <ref>
git revert -m 1 <merge>     # revert a merge commit
```

Practice: [basic-revert](basic-revert/README.md), [reverted-merge](reverted-merge/README.md)

## Undo locally (dangerous if already pushed)

```shell
git restore <file>                  # discard working-tree changes
git restore -s <ref> <file>         # restore file from a ref/tag
git reset --soft <ref>              # move HEAD; keep index + worktree
git reset --mixed <ref>             # move HEAD + index; keep worktree (default)
git reset --hard <ref>              # move HEAD + index + worktree (destructive)
```

Practice: [reset](reset/README.md), [restore](restore/README.md), [save-my-commit](save-my-commit/README.md)

## Stash & clean

```shell
git stash
git stash list
git stash apply [<stash>]
git stash pop [<stash>]

git clean -n                # dry run
git clean -n -d
git clean -f -d             # delete untracked files/dirs
```

Practice: [basic-stashing](basic-stashing/README.md), [basic-cleaning](basic-cleaning/README.md)

## Remotes & collaboration

```shell
git remote
git remote -v
git fetch
git pull
git push
git push -u origin <branch>
git push --force-with-lease   # safer than --force when rewriting
```

Practice: [master-based-workflow](master-based-workflow/README.md)

## Cherry-pick, tags, ignore

```shell
git cherry-pick <sha>
git cherry-pick <shaA>^..<shaB>   # inclusive range ending at shaB

git tag
git tag <name> [<ref>]
git tag -d <name>

# .gitignore patterns; remove a tracked file from the index:
git rm --cached <file>
git rm <file>
git mv <src> <dst>
```

Practice: [basic-cherry-pick](basic-cherry-pick/README.md), [git-tag](git-tag/README.md), [ignore](ignore/README.md)

## Finding & recovering

```shell
git bisect start
git bisect bad
git bisect good <ref>
git bisect reset
git bisect run <cmd>

git reflog                  # where HEAD has been — lifesaver
```

Practice: [bisect](bisect/README.md), [bad-commit](bad-commit/README.md), [save-my-commit](save-my-commit/README.md), [detached-head](detached-head/README.md)

## Advanced / extras

```shell
# Submodules / subtrees
git submodule update --init --recursive

# LFS (after installing git-lfs)
git lfs install
git lfs track "*.psd"

# Objects / plumbing (for internals katas)
git cat-file -t <sha>
git cat-file -p <sha>
git rev-parse HEAD
```

Practice: [submodules](submodules/README.md), [subtree](subtree/README.md), [lfs](lfs/README.md), [objects](objects/README.md), [git-attributes](git-attributes/README.md), [pre-push](pre-push/README.md), [merge-driver](merge-driver/README.md), [change-author](change-author/README.md)

## Kata workflow reminder

```shell
cd <kata-folder>
source setup.sh          # bash/zsh — or: .\setup.ps1 in PowerShell
# work inside the generated exercise/ repo
```

Cleanup exercise artifacts from the katas clone:

```shell
git clean -ffdX
```
