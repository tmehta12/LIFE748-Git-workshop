# Chapter 8. Pushing the local repository to GitHub

## Learning Outcomes
> - Pushing your local repository to the cloud (GitHub)
> - Evaluating the uploaded repository.

## 8.1 Pushing to the cloud

Now that the local repository is linked to a remote location, we can push it to the cloud:

~~~console
$ git branch -M main
$ git push -u origin main
Enumerating objects: 20, done.
Counting objects: 100% (20/20), done.
Delta compression using up to 11 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (20/20), 2.63 KiB | 2.63 MiB/s, done.
Total 20 (delta 6), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (6/6), done.
To github.com:tmehta12/test.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
~~~

*NOTE:* you may get the following error
~~~console
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
~~~

If so, you will need to add a new SSH key to your GitHub account for authentication. Please follow the instructions here: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account 

Once done, then re-run
~~~console
$ git push -u origin main
~~~

## 8.2 Checking the repository on GitHub

Congratulations! You've just pushed your local repository to GitHub!
If you go back to the GitHub and refresh the repository page, you should see that your code has been uploaded.

## Key Points
> - Use `git push` to push the local repository to the cloud. 
> - Make changes to you repository directly on GitHub and/or via the terminal. 
