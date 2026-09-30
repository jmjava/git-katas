# Git How-To (with matching katas)

Situation → what to do → which exercise to practice. Pair with the [CHEATSHEET.md](CHEATSHEET.md) for exact command flags.

## Getting started

| I want to… | Do this | Practice |
|---|---|---|
| Configure name/email/editor | `git config --global …` | [configure-git](configure-git/README.md) |
| Survive the shell (cd, ls, echo) | See [SHELL-BASICS.md](SHELL-BASICS.md) | — |
| Shorten long commands | `git config alias.…` | [alias](alias/README.md) |
| Sign commits with GPG | Generate key, `commit.gpgsign` | [signed-commits](signed-commits/README.md) |

## Day-to-day work

| I want to… | Do this | Practice |
|---|---|---|
| Record a change | `git add` → `git commit` | [basic-commits](basic-commits/README.md) |
| Understand staging vs working tree | `git status`, `git diff`, `git diff --staged` | [basic-staging](basic-staging/README.md) |
| Unstage or discard a file change | `git restore --staged`, `git restore` | [restore](restore/README.md) |
| Peek at history / who changed what | `git log --oneline --graph --all`, `git show` | [investigation](investigation/README.md) |
| Compare branches / word-level diffs | `git diff A B`, `--word-diff`, `--name-only` | [diff-advance](diff-advance/README.md) |
| Park unfinished work | `git stash` / `stash pop` | [basic-stashing](basic-stashing/README.md) |
| Remove build junk | `git clean -n` then `-f -d` | [basic-cleaning](basic-cleaning/README.md) |
| Stop tracking generated files | `.gitignore` + `git rm --cached` | [ignore](ignore/README.md) |

## Branches & integrating work

| I want to… | Do this | Practice |
|---|---|---|
| Create / switch branches | `git switch -c`, `git branch` | [basic-branching](basic-branching/README.md) |
| Fast-forward when histories didn’t diverge | `git merge` (FF) | [ff-merge](ff-merge/README.md) |
| Merge diverged branches | `git merge` (merge commit) | [3-way-merge](3-way-merge/README.md) |
| Resolve a merge conflict | edit → `git add` → `git commit` | [merge-conflict](merge-conflict/README.md), [merge-mergesort](merge-mergesort/README.md) |
| Replay my commits on top of another branch | `git rebase` | [rebase-branch](rebase-branch/README.md), [rebase-multiple-commits](rebase-multiple-commits/README.md) |
| Take only a few commits from elsewhere | `git cherry-pick` | [basic-cherry-pick](basic-cherry-pick/README.md) |
| Collaborate on a shared master | `fetch` / `pull` / `push`, resolve divergence | [master-based-workflow](master-based-workflow/README.md) |

## Fixing mistakes

| I want to… | Do this | Practice |
|---|---|---|
| Fix the *last* commit (message or forgotten file) | `git commit --amend` (**before** others pull it) | [amend](amend/README.md) |
| Undo a commit that is already shared | `git revert <sha>` | [basic-revert](basic-revert/README.md) |
| Move HEAD / uncommit without rewriting remotes carefully | `git reset --soft/--mixed/--hard` | [reset](reset/README.md) |
| Reorder, squash, or drop commits | `git rebase -i` | [reorder-the-history](reorder-the-history/README.md), [squashing](squashing/README.md), [advanced-rebase-interactive](advanced-rebase-interactive/README.md) |
| Fix an older commit with a clean history | `git commit --fixup=<sha>` then `rebase --autosquash -i` | [rebase-interactive-autosquash](rebase-interactive-autosquash/README.md) |
| I committed on the wrong branch | cherry-pick / reset / branch move | [commit-on-wrong-branch](commit-on-wrong-branch/README.md), [commit-on-wrong-branch-2](commit-on-wrong-branch-2/README.md) |
| I “lost” a commit | `git reflog`, then `branch` / `reset` / `cherry-pick` | [save-my-commit](save-my-commit/README.md) |
| Detached HEAD warning | create a branch at current commit: `git switch -c …` | [detached-head](detached-head/README.md) |
| Re-apply work after reverting a merge | careful `revert` of the revert / re-merge | [reverted-merge](reverted-merge/README.md) |
| Wrong author/email on early commits | config + interactive rebase / `--reset-author` | [change-author](change-author/README.md) |

## Finding bugs in history

| I want to… | Do this | Practice |
|---|---|---|
| Find which commit introduced a bug | `git bisect` | [bisect](bisect/README.md), [bad-commit](bad-commit/README.md) |
| Run tests on every commit in a range | `git rebase --exec` | [rebase-exec](rebase-exec/README.md) |

## Tags, remotes, large files, structure

| I want to… | Do this | Practice |
|---|---|---|
| Mark a release | `git tag` | [git-tag](git-tag/README.md) |
| Store large binaries efficiently | Git LFS | [lfs](lfs/README.md) |
| Vendor another repo (link) | submodules | [submodules](submodules/README.md) |
| Vendor another repo (merged history) | subtree | [subtree](subtree/README.md) |
| Control line endings / custom diffs | `.gitattributes` | [git-attributes](git-attributes/README.md) |
| Block bad pushes | client-side hook | [pre-push](pre-push/README.md) |
| Custom conflict resolution | merge driver | [merge-driver](merge-driver/README.md) |

## Look under the hood

| I want to… | Do this | Practice |
|---|---|---|
| See how Git stores commits/trees/blobs | `cat-file`, explore `.git` | [objects](objects/README.md), [investigation](investigation/README.md) |

## Suggested path

New to Git? Follow the order in [Overview.md](Overview.md) (or the shorter path in [README.md](README.md)). Use this page when you hit a real problem and want the matching kata.
