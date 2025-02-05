# Chapter 4. Making our first commit

## Learning Outcomes
> - Adding and committing to our repository.
> - Explaining what was committed (for future reference). 

## 4.1 Add our file to the index
We now need to commit this new file to the index, and commit it to our repository.

Commits can be thought of as snapshots or milestones along the timeline of a Git project

The first step is to add it to the index:

~~~bash
git add random-reads.py
git status
~~~

this will output:
~~~console
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   random-reads.py
~~~

> This message tells us that the new file is now in the index ready to be committed.

## 4.2 Store the changes to a commit
We can now store this set of changes into a commit:

~~~bash
git commit -m"Initial commit of the random-reads.py script"
~~~

this will output:
~~~console
[main (root-commit) a91347b] Initial commit of the random-reads.py script
 Committer: Tarang Mehta <tarangmehta@Tarangs-MacBook-Pro.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 42 insertions(+)
 create mode 100644 random-reads.py
~~~

> This will look different for each user
> Don't worry about the initial comments of name and email address, this will be sorted out in the next few steps.
> The main point is that the changes have now been committed.

## 4.3 Check the log of the commit

Now, let's check the log:

~~~bash
git log
~~~

this will output:

~~~console
commit a91347bacb56b9c1cd8b14e38ed16aabc67d8bc4 (HEAD -> main)
Author: Tarang Mehta <tarangmehta@Tarangs-MacBook-Pro.local>
Date:   Tue Jan 21 12:54:58 2025 +0000

    Initial commit of the random-reads.py script
~~~

> Your log will look different.
> Your commit will have a different ID, and your username should be different to this one!
> This is the "standard loop" of git: generate content; fill up an index of modified files; commit those changes to the repository.

## Key Points
> - Use `git add` to commit a something to your repo.
> - Commits are snapshots/milestones along the timeline of a Git project.
> - Use `git commit` to add precise details of what was committed to the repo.
> - Use `git log` to track the commitments.
