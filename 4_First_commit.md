# Chapter 4. Making our first commit

## Learning Outcomes
> - How to add to and commit to our repository
> - How to add details to what was committed 

## 4.1 Add our file to the index
We now need to commit this new file to the index, and commit it to our repository.
The first step is to add it to the index:

~~~console
$ git add random-reads.py
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   random-reads.py
~~~

> This message tells us that the new file is now in the index ready to be committed.

## 4.2 Store the changes to a commit
We can now store this set of changes into a commit:

~~~console
$ git commit -m"Initial commit of the random-reads.py script"
[main (root-commit) 0200bb9] Initial commit of the random-reads.py script
 1 file changed, 45 insertions(+)
 create mode 100755 random-reads
~~~

## 4.3 Check the log of the commit

Now, let's check the log:

~~~console
$ git log
commit 0200bb9c18a83f8f3d8341d472f58b4a72563fe4 (HEAD -> main)
Author: Alastair Droop <alastair.droop@york.ac.uk>
Date:   Thu Aug 31 14:43:35 2023 +0100

    Initial commit of the random-reads.py script
~~~

> Your log will look different.
> Your commit will have a different ID, and your username should be different to this one!
> This is the "standard loop" of git: generate content; fill up an index of modified files; commit those changes to the repository.

## Key Points
> - Use git add to commit a something to your repo
> - Use git commit to add precide details of what was committed to the repo
> - Use git log to track the committments
