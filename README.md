# Just enought Git for a non-developer

In Sharetribe almost everyone has to deal with code. That's the spirit of a small tech startup. We use git and Github for source code management and when dealing with code, you have to have basic skills for using git.

This article was meant to be an internal document for our non-developers who have to deal with code, namely our designer and analytics experts. However, as this stuff migth interest others, the blog post was written.

The best way to learn is by doing. That's why this tutorial contains also an interactive part. The tutorial can be found here https://github.com/sharetribe/just-enough-git. Feel free to make your own fork.

## Prerequisite

The article concentrates on branching. I expect that you already have the basic knowledge of git, that is:

* You know how to access and use command-line
* You have git installed
* You have a Github account
* You know how to `git clone` a repository
* You know how to see current `git status`
* You know how to `git add` changes to next commit and how to `git commit` them
* You know how to `git push` the commits to Github
* You know how to `git pull` others’ commits from Github
* You know what is a code branch

That is, you already know quite a lot! However, to be efficient with Git, there’s still a couple tricks you need to learn.

## The branching model.

At Sharetribe, we you so called Github branching model. The model is pretty simple and easy to grasp. It goes like this:

1. **Branch:** When you start working with a new feature/bug fix/document improvement/anything, you create a new branch.
1. **Pull Request:** As soon as possible, even before the feature is ready, push the branch to Github and create a Pull Request, so that others can see what you are up to.
1. **Rebase:** Make sure, that your branch is up to date. If not, rebase.
Review: When the feature is ready, ask a fellow teammate for a review. Fix the issues the reviewer found, if any
1. **Merge:** When the reviewer gives green light, merge the Pull Request to master.

A rule of thumb is that you should **never brake the master branch**. Master branch goes always to production.

## Learning goals

In order to follow that branching model, you need to learn a couple new git skills:

* Your git is properly configured
* You know how to create a branch
* You know how to jump from branch to another
* You know how to push the branch to Github
* You know how to update (rebase) your branch to include newest changes by others
* You know how to resolve merge conflicts

## Git configurations

In order to work efficiently with the branching model, you need to have following git configurations set. Open command-line and type:

```
git config --global push.default current
git config --global branch.autosetuprebase always
```

Now you’re ready to start.

How to create a branch and jump from branch to another.

git checkout is a command which jumps from branch to another. If you give it an option -b, it will create a new branch. Let’s try it.

git branch -b add-description

Next, type git status

git status

The first line says that you are now in the add-description branch

Let’s make a change to index.html. You can see that there’s a paragraph with class description, but the paragraph doesn’t have any content. Let’s add a description, so that the result is

<p class=“paragraph”>This is how you branch like a rockstar!</p>

Next, use add, commit and push to save and push your changes.

git add index.html
git commit
git push

Now, go to your repository at Github. You can see that Github is suggesting you to make a Pull Request.

Hit the Compare and create a Pull Request button and create you first Pull Request


