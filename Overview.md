# Overview of the Git Kata Exercises

Quick links: [Cheatsheet](CHEATSHEET.md) · [How-To (situation → kata)](HOWTO.md) · [Shell basics](SHELL-BASICS.md)

## Setup

1. [configure-git](configure-git/README.md) - If git is not configured, some basic configuration steps

## Basic Git Katas in Suggested Order

1. [basic-commits](basic-commits/README.md) - Very basic creation of commits.
2. [basic-staging](basic-staging/README.md) - Interacting with the stage (index).
3. [restore](restore/README.md) - Discard or unstage changes with `git restore`.
4. [basic-branching](basic-branching/README.md) - The first stride into branching.
5. [ff-merge](ff-merge/README.md) - A tour around the most trivial of merges.
6. [3-way-merge](3-way-merge/README.md) - A basic merge, involving multiple diverged branches.
7. [merge-conflict](merge-conflict/README.md) - A basic merge between diverging branches with incompatible (but simple) changesets.
8. [merge-mergesort](merge-mergesort/README.md) - A merge conflict with actual code.
9. [rebase-branch](rebase-branch/README.md) - Using rebase as an alternative to merging.
10. [rebase-multiple-commits](rebase-multiple-commits/README.md) - Compare merge vs rebase when a branch has multiple commits.
11. [basic-revert](basic-revert/README.md) - Use revert to revert a change
12. [reset](reset/README.md) - Reset is a powerful and slightly dangerous command if you do not know what you are doing. Go through the three modes of resetting here.
13. [basic-cleaning](basic-cleaning/README.md) - Cleaning the workspace.
14. [amend](amend/README.md) - Amending previous commits.
15. [reorder-the-history](reorder-the-history/README.md) - We might have created our commits in a suboptimal order, practice to fix that scenario here.
16. [squashing](squashing/README.md) - A lot of small commits is good when you are working locally, but for sharing your code, it might be more beneficial to deliver your code changes in large sets. Go here to experiment with that. Write a good commit
17. [advanced-rebase-interactive](advanced-rebase-interactive/README.md) - Practice using the interactive rebase commands.
18. [rebase-interactive-autosquash](rebase-interactive-autosquash/README.md) - Fix older commits cleanly with `--fixup` and `--autosquash`.
19. [basic-stashing](basic-stashing/README.md) - The first stride into stashing.
20. [ignore](ignore/README.md) - The basics of using the `.gitignore` file. And using `git rm`.
21. [basic-cherry-pick](basic-cherry-pick/README.md) - Copy selected commits onto another branch.
22. [git-tag](git-tag/README.md) - Tags are convenient for keeping track of commits that bump a version number. In this exercise, you will list, add and delete tags.
23. [alias](alias/README.md) - Create short aliases for common commands.
24. [diff-advance](diff-advance/README.md) - Advanced `git diff` options and practical uses.
25. [master-based-workflow](master-based-workflow/README.md) - Push/pull collaboration on a shared master branch.
26. [submodules](submodules/README.md) - Submodules are loathed by many. Run through this exercise to see what the ruckus is all about.
27. [subtree](subtree/README.md) - Embed another repository's history with subtree.

## Katas that solve standard problems

1. [commit-on-wrong-branch](commit-on-wrong-branch/README.md) - If we accidentally put unpushed commits on the wrong branch, how do we effectively _move_ them to another branch before our work on that branch.
2. [commit-on-wrong-branch-2](commit-on-wrong-branch-2/README.md) - Another exercise on what to do if you have accidentally committed on the wrong branch.
3. [reverted-merge](reverted-merge/README.md) - We revert a merge, but, after fixes are added to the merged branch, we want the changes from merge and the new fixes.
4. [save-my-commit](save-my-commit/README.md) - Should you accidentally or on purpose delete a commit, go here to try and save it. You will use the reflog.
5. [detached-head](detached-head/README.md) - git complains that you are in a "You are in 'detached HEAD' state". What do you do?
6. [change-author](change-author/README.md) - Fix author/email on commits you already made (and pushed).

## Katas On Advanced features

1. [git-attributes](git-attributes/README.md) - .gitattributes file allows you to specify how git handles files, such as line endings in text files or how to diff a binary file.
2. [Bad-commit](bad-commit/README.md) - Using `git bisect` to find a bad commit.
3. [bisect](bisect/README.md) - Another kata using `git bisect`.
4. [pre-push](pre-push/README.md) - A quick exercise in using Git hooks.
5. [Investigation](investigation/README.md) - Discover what is going on in a Git repo, figure out what it looks like under the hood.
6. [Objects](objects/README.md) - A small exercise into Git internals.
7. [merge-driver](merge-driver/README.md) - Defining a custom merge driver.
8. [rebase-exec](rebase-exec/README.md) - Run tests on every commit using `git rebase --exec`
9. [lfs](lfs/README.md) - Introduction to Git Large File Storage.
10. [signed-commits](signed-commits/README.md) - Set up and verify GPG-signed commits.

## Docs index

| Doc | Purpose |
|---|---|
| [README.md](README.md) | Quick start + suggested learning path |
| [Overview.md](Overview.md) | Full exercise list (this page) |
| [CHEATSHEET.md](CHEATSHEET.md) | Command quick reference |
| [HOWTO.md](HOWTO.md) | “How do I…?” situations mapped to katas |
| [SHELL-BASICS.md](SHELL-BASICS.md) | Minimal shell survival guide |
