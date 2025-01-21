## 8. Pushing the local repository to GitHub

## Learning Outcomes
> - Pushing your local repository to the cloud (GitHub)
> - Evaluating the uploaded repository.

## 8.1 Pushing to the cloud

Now that the local repository is linked to a remote location, we can push it to the cloud:

~~~console
$ git push -u origin main
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 1.35 KiB | 1.35 MiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To github.com:tmehta12/random-reads.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
~~~

## 8.2 Checking the repository on GitHub

Congratulations! You've just pushed your local repository to GitHub!
If you go back to the GitHub and refresh the repository page, you should see that your code has been uploaded.

## Key Points
> - Use `git push` to push the local repository to the cloud. 
> - Make changes to you repository directly on GitHub and/or via the terminal. 
