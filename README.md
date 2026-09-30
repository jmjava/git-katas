---
maintainer: JKrag
---
# Git Katas

## Quick Start

### In the Cloud

[![Open in Cloud Shell](https://gstatic.com/cloudssh/images/open-btn.svg)](https://console.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/praqma-training/git-katas.git)

### On Your Local Machine

![Quick Start](/images/quickstart.gif)

- Clone this repository
- Go into the folder you want to solve an exercise in
- Run the `setup.sh` script
- Consult the README.md in that folder to get a description of the exercise

## Purpose of Git Katas

This repository is a collection of Git exercises.
The concept is stolen without shame from [Schauderhaft.de](http://blog.schauderhaft.de/gitkata/).
Unfortunately, they have not maintained the system - and we need more good Git exercises.

The exercises are designed for use when we are teaching Git courses. You should be able to use them as self-contained exercises that will allow you to keep your Git skills sharp.

Exercises starting with _basic_ are entry-level - other exercises vary greatly in difficulty.

To get an overview of the exercises in here look in [Overview.md](Overview.md).

**Reference docs**

- [CHEATSHEET.md](CHEATSHEET.md) — command quick reference
- [HOWTO.md](HOWTO.md) — situation → fix → matching kata
- [SHELL-BASICS.md](SHELL-BASICS.md) — minimal shell survival guide

Feel free to use these exercises, that's why they're public!

## Suggested Learning Path

If you are coming to this repository for some basic Git knowledge, we recommend going through the exercises in the following order.
This is the order that Jan Krag at Praqma teaches Git and might change over time. There are more exercises than this, but these should take you through
everything you need to be able to use Git effectively in your day to day life.

- [Basic Commits](./basic-commits/README.md)
- [Basic Staging](./basic-staging/README.md)
- [Investigation](./investigation/README.md)
- [Basic Branching](./basic-branching/README.md)
- [Fast Forward Merge](./ff-merge/README.md)
- [3 way Merge](./3-way-merge/README.md)
- [Merge Mergesort](./merge-mergesort/README.md)
- [Rebase Branch](./rebase-branch/README.md)
- [Basic Revert](./basic-revert/README.md)
- [Reset](./reset/README.md)
- [Basic Cleaning](./basic-cleaning/README.md)
- [Amend](./amend/README.md)
- [Reorder the History](./reorder-the-history/README.md)
- [Advanced Rebase Interactive](./advanced-rebase-interactive/README.md)
- [Rebase using autosquash](./rebase-interactive-autosquash/README.md)
- [Basic Stashing](./basic-stashing/README.md)

See [Overview.md](Overview.md) for a more complete list and suggested order.

## Contributing

If you miss exercises or find errors in any of them, feel free to improve them and make a pull request.

You can also make an issue so we notice an opportunity to improve!

Thank you!

### Celebrating success

On September 6th, 2023, we reached the milestone of having 1000 stars on GitHub. Thank you all for your support! This repository would not be where it is without the valuable contributions from the community.

![1000 stars](/docs/1000stars-git-katas.png)

## Cheatsheet & How-To

The full command reference and situation guides live in dedicated docs (kept out of this README so they stay easy to scan):

- **[CHEATSHEET.md](CHEATSHEET.md)** — commands grouped by topic (status, commit, branch, merge/rebase, undo, remotes, …), each section linking to practice katas
- **[HOWTO.md](HOWTO.md)** — “I want to…” tables that map real problems to the right command *and* the matching exercise

Snippet of the most-used commands:

```shell
git status
git diff / git diff --staged
git add <file> && git commit -m "message"
git log --oneline --graph --all
git switch -c my-branch
git merge <branch>          # or: git rebase <branch>
git stash / git stash pop
git restore <file>          # discard worktree changes
git restore --staged <file> # unstage
git revert <sha>            # safe undo on shared history
```

## Testing

There is a very small test that you can run in powershell or bash.
It is contained in the scripts `test.sh` and `test.ps1`.

### Cleanup

You can remove testing artifacts, `exercise` directories, with the git clean command:

```sh
git clean -ffdX
```
