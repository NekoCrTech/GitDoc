---
icon: file-lines
---

# Working with Branches

On large projects, we often work in multiple contexts:

* You're working on 2 different color scheme variations for your website at the same time, unsure of which you like best&#x20;
* You're also trying to fix a horrible bug, but it's proving tough to solve. You need to really hunt around and toggle some code on and off to figure it out.&#x20;
* A teammate is also working on adding a new chat widget to present at the next meeting. It's unclear if your company will end up using it.&#x20;
* Another coworker is updating the search bar autocomplete.&#x20;
* Another developer is doing an experimental radical design overhaul of the entire layout to present next month.

Working in a linear way would never make this possible. That's why there are Branches

## Branches

Branches are an essential part of Git!&#x20;

Think of branches as alternative timelines for a project.&#x20;

They enable us to create separate contexts where we can try new things, or even work on multiple ideas in parallel.&#x20;

If we make changes on one branch, they do not impact the other branches (unless we merge the changes)



<figure><img src=".gitbook/assets/Screenshot 2024-12-06 175542.png" alt=""><figcaption></figcaption></figure>

***

### The Master Branch

The default branch name is master.&#x20;

It doesn't do anything special or have fancy powers. It's just like any other branch.

Many people designate the master branch as their "source of truth" or the "official branch" for their codebase, but that is left to you to decide.&#x20;

From Git's perspective, the master branch is just like any other branch. It does not have to hold the "master copy" of your project.

{% hint style="info" %}
In 2020, Github renamed the default branch from master to main. The default Git branch name is still master, though the Git team is exploring a potential change. We will circle back to this shortly.
{% endhint %}

***

### HEAD

We'll often come across the term HEAD in Git.&#x20;

HEAD is simply a pointer that refers to the current "location" in your repository. It points to a particular branch reference.&#x20;

So far, HEAD always points to the latest commit you made on the master branch, but soon we'll see that we can move around and HEAD will change!

***

### Viewing Branches

Use git branch to view your existing branches. The default branch in every git repo is master, though you can configure this. Look for the \* which indicates the branch you are currently on.

```git
git branch                        // Creates a list with all branches
```

Example list of `git branch`

\
`develop`\
`*feature/attributes`\
`feature/units`\
`feature/grid`\
`main`

We can get more info about branches by using the flag `-v`

```
git branch -v                    // Creates a list with all branches with some info
```

Example list with flag `-v`

`develop              5cecaec    merge branch 'feature/character' into develop`\
`*feature/attributes  6a5871d    create basic attribute list` \
`feature/grid         a0ef343    develop Pathfinding` \
`feature/units        6a5871d    add 3D models for aliens`\
`main                 f2fbe42    initialize Project`

***

### Creating Branches

Use `git branch <branch-name>` to make a new branch based upon the current HEAD.

&#x20;This just creates the branch. It does not switch you to that branch (the HEAD stays the same)

```git
git branch bugfix                // Creates a branch named bugfix
```

***

### Switching Branches

Once you have created a new branch, use git switch to switch to it.

```git
git switch bugfix                 // Switches to bugfix branch
```

***

Historically, we used git `checkout <branch-name>` to switch branches. This still works.&#x20;

The checkout command does a million additional things, so the decision was made to add a standalone switch command which is much simpler.&#x20;

You will see older tutorials and docs using checkout rather than switch. Both now work. git checkout.&#x20;

***

Use git switch with the `-c` flag to create a new branch AND switch to it all in one go.

```git
git switch -c bugfix            // Creates and switches to branch named bugfix
```

***

### Deleting Branches

We use  the flag `-d` to delete a branch.

```
git branch -d bugfix            // Deletes the branch named bugfix
```

The HEAD cannot point to the branch we want to delete

{% hint style="info" %}
The flag -d is used for merged branches. To delete an unmerged branch use the flag -D
{% endhint %}

***

### Renaming Branches

To rename a branch we must first switch to that branch and use the flag `-m`

```
git branch -m hotfix            // Renames the current branch to hotfix
```
