# Chapter 2. Initialising an empty local repository

## Learning Outcomes
> - Initialising a local repository.
> - Examine the status of the local repository.

## 2.1 Initialise an empty git repo
Now that we've made a workspace directory, we need to initialise an empty git repository:

~~~bash
git init
~~~
this will show:
~~~console
Initialized empty Git repository in /Users/tarangmehta/random-reads/.git/
NOTE: This will be different for each user
~~~

> This command has created a new directory in the `random-reads` directory called `.git`.
> As it starts with a dot, it is hidden (at least in bash), so we need to use the `-a` argument in `ls` to see it:

~~~bash
ls -a
~~~
this will show:
~~~console
./    ../   .git/
~~~

## 2.2 Check the status
Check that git thinks that the repository is OK:

~~~bash
git status
~~~
this will show:
~~~console
On branch main # NB: this may show as 'master' - please take note of this for later

No commits yet

nothing to commit (create/copy files and use "git add" to track)
~~~

> The above message is saying that there is a repository here, but that it is empty.

## Key Points
> - `git init` initialises a repository.
> - Git stores all of its repository data in the .git directory.

