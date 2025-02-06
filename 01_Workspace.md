# Chapter 1. Creating your workspace

## Learning Outcomes
> - Setting up Git.
> - Creating a workspace.

## 1.1. Prerequisites

Before you start, you should have the following things set up:

1. Your computer needs to have `git` installed;
2. You need to be able to type commands into a terminal on your computer;
3. Ideally, you need to have a suitable text editor (such as [`VSCode`](https://code.visualstudio.com)) installed; and
4. You need to have created a [GitHub](https://github.com) account for yourself

## 1.2. Create a workspace directory

> The first thing we're going to do is to create an empty folder to hold our code in one place.  This folder is going to become the git *workspace*.
> We'll then create a git repository within that folder.
> There are many different ways we can do this (like, for example, directly on the website), but for now we're going to use the terminal.

Open the terminal application on your laptop and use the `cd` command to navigate to a sensible location for your work e.g., ~/Documents
> If you're on a Windows computer you can shortcut this process by using File Explorer to go to a location and then right-clicking on a folder and selecting "Open Git bash here".
>
> **NB**: If you're struggling to navigate around your computer using the shell, either ask one of the demonstrators, or have a look at the LIFE748: Intro to Linux workshop on Canvas or [Software Carpentry Unix Shell refresher workshop](https://swcarpentry.github.io/shell-novice/index.html).

Create a new directory to hold our code using the bash terminal.
In this example, we're going to call it `random-reads`.
Once we've created the directory, we can change directory into it so that it becomes the current working directory:

~~~bash
mkdir random-reads
~~~

~~~bash
cd random-reads
~~~

Make sure that it is empty, by listing all of the directory contents:

~~~bash
ls -a
~~~
this will show:
~~~console
./    ../
~~~

> The `-a` argument to `ls` show hidden files and folders. Without this then the directory would not contain anything.

## Key Points
> - Creating a local workspace is the starting point for any/all repositories.
> - There are many ways to create and manage repositories, including via the terminal.
