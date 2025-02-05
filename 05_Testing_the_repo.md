# Chapter 5. Testing the repository

## Learning Outcomes
> - Deleting something.
> - Retrieving the deleted file using the backup.

## 5.1 Deleting something (to retrieve via backup)
One use of git is as a method of backup.
Let's test this by deleting the `random-reads.py` file.

~~~bash
rm random-reads.py
~~~
~~~bash
$ ls
~~~


> Here, you will have NOTHING appear on your terminal as the folder is now empty of any non-hidden files
> Oops!  We've accidentially deleted our precious code!
> Not to worry; we have a copy in the repository.
> First, let's check what git thinks about this:

~~~bash
git status
~~~

this will output:
~~~console
On branch main
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    random-reads.py

no changes added to commit (use "git add" and/or "git commit -a")
~~~

> This message is telling us that a file that is recorded in the repository is missing.
> We have the option of recording its deletion in the index and committing that (we'd use `git rm random-reads.py`), but in this case the deletion was accidental so we'll simply get the file back from the latest commit.

## 5.2 Retrieving the deleted file

We can retrieve the file from the latest commit:

~~~bash
git checkout random-reads.py
~~~

this will output:
~~~console
Updated 1 path from the index

now run:
~~~bash
ls
~~~

this should output:
~~~console
random-reads.py
~~~

> Great! We've got our code back again.
> This is a major benefit of `git`.

## Key Points
> - You can always look at the history of your repository.
> - A key benefit of git is the ability to retrieve deleted files/content.
