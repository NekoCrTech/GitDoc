---
icon: file-lines
---

# Commits in Details

Before going deeper into git here is a book from git with everything it provides in details

{% embed url="https://git-scm.com/book/en/v2" %}

## &#x20;Atomic Commits

When possible, a commit should encompass a single feature, change, or fix. In other words, try to keep each commit focused on a single thing.&#x20;

This makes it much easier to undo or rollback changes later on. It also makes your code or project easier to review.

## Commit Messages

**From the Git docs:**

> Describe your changes in imperative mood, e.g. "make xyzzy do frotz" instead of "\[This patch] makes xyzzy do frotz" or "I changed xyzzy to do frotz", as if you are giving orders to the codebase to change its behavior.

{% hint style="info" %}
Though the Git docs suggest using present-tense imperative messages, many developers prefer to use past-tense messages. All that matters is consistency, especially when working on a team with many people making commits
{% endhint %}

If you are using git with commands the first line of the message should be treated as title, then you can leave a blank line and then describe in some more details what your commit is. This way when you or someone else contributing tries to log with one line  he will see what the commit is about.

## Amending Commits

Suppose you just made a commit and then realized you forgot to include a file! Or, maybe you made a typo in the commit message that you want to correct.&#x20;

Rather than making a brand new separate commit, you can "redo" the previous commit using the --amend option.

```git
git commit --amend
```

{% hint style="warning" %}
Amend is for editing ONLY the last commit
{% endhint %}

## Ignoring Files

We can tell Git which files and directories to ignore in a given repository, using a .gitignore file. This is useful for files you know you NEVER want to commit, including:

* Secrets, API keys, credentials, etc.&#x20;
* Operating System files (.DS\_Store on Mac)&#x20;
* Log files&#x20;
* Dependencies & packages

Create a file called .gitignore in the root of a repository. Inside the file, we can write patterns to tell Git which files & folders to ignore:

* .DS\_Store (_will ignore files named .DS\_Store)_&#x20;
* folderName/ _(will ignore an entire directory)_&#x20;
* \*.log _(will ignore any files with the .log extension)_

{% hint style="info" %}
It is recommended to use [gitignore.io](https://www.toptal.com/developers/gitignore/) to generate an ignore list
{% endhint %}
