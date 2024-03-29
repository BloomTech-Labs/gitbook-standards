# Git Rebase

## Rebasing a feature branch from main

On occassion you'll find that you've been working on a feature branch and you need to merge in changes from the main branch. This could just be a final step before you push a series of commits to github in order to creating a PR. Or, it's to update your branch from main at the end of a day or so.

These steps are similar to what the "Rebase and Merge" action does on github. \(which you should always use if "Squash and Merge" isn't available.

### Objective

This guide will show you how to rebase \(rebuild\) a feature branch to begin at the current HEAD of the main branch. Think of it as if you are starting a new branch based on the current main and pasting all of your commits to the new branch.

![](../.gitbook/assets/git-rebase.svg)

{% hint style="danger" %}
Be careful when rebasing a branch that has already been pushed to a remote \(public, eg. the main branch\) repository, such as github; doing so will cause conflicts and confusion among your team. 
{% endhint %}

#### Technologies

* git \(cli\)

#### References

* [The Pro Git book](https://git-scm.com/book/en/v2/Git-Branching-Rebasing)
* [bitbucket tutorials](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)

### Getting Started

1. Make sure all changes are committed to your feature branch
2. You will need to update your local main branch
   * `> git checkout main`
   * `> git pull origin main`
3. Go back to your feature branch
   * `> git checkout feature-branch`
4. Now we can rebase the feature branch onto `main`

   * `> git rebase main` 

   > First, rewinding head to replay your work on top of it... 
   >
   > Applying: added staged command

5. Your commits will now show in the git log after the commits merged from main

### Review of 2 merge strategies

{% embed url="https://youtu.be/rxwHczFef5E" %}

