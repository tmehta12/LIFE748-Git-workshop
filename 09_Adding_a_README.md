# Chapter 9. Adding a README file

## Learning Outcomes
> - Creating a README file describing the project in the markdown format - this is for the benefit of yourself and any other users (if made 'public').
> - Pushing the README file to GitHub.

## 9.1 Creating a README file

Currently, the repository is not very well documented.
By convention, a file named `README` or `README.md` in the root of your workspace is taken to contain a description of the project.
If such a file exists, GitHub will display it on the main repository page.
Let's create such a file for our repository.

Go back to your text editor e.g., VScode or `nano`, and create a second file called `README.md` in the workspace folder.

Add the following text to the file:

```markdown
# Generate Random FASTQ Reads

The `random-reads.py` python script generates random nucleotide FASTQ data.

## Usage

~~~python
usage: random-reads.py [-h] [-V] [-v {error,warning,info,debug}] [-l N] N

Generate random FASTQ data

positional arguments:
  N                     Number of reads to generate

options:
  -h, --help            show this help message and exit
  -V, --version         show program's version number and exit
  -v {error,warning,info,debug}, --verbose {error,warning,info,debug}
                        Set logging level (default warning
  -l N, --length N      Read length to yield
~~~
```

## 9.2 Committing the README file

As we've added a file, we need to make a new commit (remember, this is a snapshot of your Git project), by running:

~~~bash
git add README.md
~~~
followed by running:
~~~bash
git commit -m"Add README file"
~~~
this will output:
~~~console
[main d75b82e] Add README file
 1 file changed, 21 insertions(+)
 create mode 100644 README.md
~~~

## 9.3 Pushing the committed README file to GitHub

We can now push this new commit to GitHub:

~~~bash
git push
~~~
this will output:
~~~console
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 11 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 607 bytes | 607.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:tmehta12/test.git
   a55e621..f3e88dd  main -> main
~~~

> We didn't need to specify a branch or remote name, as git will use the current branch and the only remote (as there is only one).

Go back to Github and refresh the page again.
Hopefully, you'll see the new README documentation appear.

## Key Points
> - Create a README file in your workspace to document and describe the project and it's features.
> - Commit and Push the README file to GitHub - this will position in main branch for all to see on the landing page.
