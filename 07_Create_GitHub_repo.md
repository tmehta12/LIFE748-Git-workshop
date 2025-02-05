# Chapter 7. Create a GitHub Repository

## Learning Outcomes
> - Creating a remote GitHub repository.
> - Pushing the content of our local repository to the remote repository.

## 7.1 Creating a remote repository

Now that we have an active local repository, we need to get it uploaded to a remote repository for safekeeping and security.
We will do this using [GitHub](https://www.github.com).

* Log into your Github account, and click on the "New" button (or go directly to [https://github.com/new](https://github.com/new)).
* You should be greeted by the "Create a new repository" page.
* Choose a sensible name for your repository (for example "random-reads").
* Add a brief description of the repository to help you remember what it contains.
* Select "Private" to make your repository private.
* For now, leave the "Add a README file" unticked, and select "None" for the `.gitignore` and license options.
* Click the "Create repository" button at the bottom.

Once you've done this, your new repository will be created.
Currently there is nothing in this repo.

## 7.2 Linking the local and remote repository

So, we now need to push the contents of our local repository to this remote one.
For this to happen, we need to link this new remote repository the local repository.
We do this using the Github repository URL.

* Write down or copy the remote repository URL. It will be located in the "Quick Setup" section of the remote repository page.

Now that we have the remote repository created and have its URL, we can link it to the local repository.
We will give the remote repository a name to identify it.
By default, the main remote repository is called `origin` - you could use whatever name you wanted though.

NOTE: The `git remote add` command takes two arguments:

> A remote name, for example, origin
> 
> A remote URL, for example, https://github.com/OWNER/REPOSITORY.git


Link the local repository to the new remote repository (we will use the default name `origin`), by running:

~~~bash
git remote add origin git@github.com:tmehta12/random-reads.git
~~~

> **NB**: You will have a different URL, as this repository is private to me.

## Key Points
> - Create a remote repository on the GitHub website using the "Create a new repository" page. 
> - On the terminal, use `git remote add` to link your local repository to the remote repository you created.
