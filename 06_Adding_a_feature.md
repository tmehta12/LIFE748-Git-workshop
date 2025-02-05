# Chapter 6. Adding a feature

## Learning Outcomes
> - Updating something e.g., code.
> - Creating a new branch for updating. 
> - Retrieving or examining previous versions of something e.g., code.

## 6.1 Modifications

Now, we need to update our `random-reads.py` code to allow us to alter the length of the reads returned.
We'll do this in a new branch in case our modifications break something.

First, let's create a new branch my checking out the latest commit into a new branch (called `specify-readlength`) by running:

~~~bash
git checkout -b specify-readlength
~~~
this will output:
~~~console
Switched to a new branch 'specify-readlength'
~~~

Now, when we check `git status` we will see we're on the new `specify-readlength` branch by running:

~~~bash
$ git status
~~~
this will output:
~~~console
On branch specify-readlength
nothing to commit, working tree clean
~~~

Update the `random-reads.py` script to take an optional length argument by updating the following line numbers.
For this, I suggest using the text editor VScode by: 
> 1. copying the original code into a new file in VScode
> 2. adding the lines below at the specified line numbers (make sure to properly indent)
> 3. copying the new code into the `random-reads.py` file using:
>> 3a. `nano random-reads.py`
>> 
>> 3b. followed by holding down `Control + K` to delete ALL line blocks
>> 
>> 3c. pasting the new code in
>> 
>> 3d. followed by `Control + 0` then `ENTER` to write out
>> 
>> 3e. then `Control + X` to exit 

Update line 10:

~~~python
__version__ = "0.2.0"
~~~

Add a new line 24:

~~~python
    parser.add_argument("-l", "--length", dest="length", type=int, default = "100", metavar="N", help="Read length to yield")
~~~

Update line 40 `print("".join(choices(nucleotides, k=10)))` to:

~~~python
        print("".join(choices(nucleotides, k=args.length)))
~~~

Update line 42 `print("".join(choices(phred, k=10)))` to:

~~~python
        print("".join(choices(phred, k=args.length)))
~~~

## 6.2 Committing the modifications

Now that we've made some modifications, we make a new index and commit it as before by running both:

~~~bash
git add random-reads.py
~~~
and ..
~~~bash
git commit -m"Update random-reads.py to allow user-specified read length"
~~~
this will output:
~~~console
[specify-readlength 57c676a] Update random-reads.py to allow user-specified read length
 Committer: Tarang Mehta <tarangmehta@Tarangs-MacBook-Pro.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 4 insertions(+), 2 deletions(-)
~~~

> Obviously, in the real world, features are a little more complex to implement, and would likely require multiple rounds of code editing and committing.

## 6.3 Getting the old version

Although we've now edited `random-reads.py`, we can still get the unedited version by switching branches back to main/master (in Mac/Linux) or master (in Windows) - please FOLLOW the CORRECT commands for your system!!!

> *For Mac/Linux - NB: the main branch could also be 'master' so use `git switch master` if instead, but if not, run:*
>> ~~~bash
>> git switch main
>> ~~~
>> this will output:
>> ~~~console
>> Switched to branch 'main'
>> ~~~
>> now run:
>> ~~~console
>> ./random-reads.py --version
>> ~~~
>> this will output:
>> ~~~console
>> random-reads.py 0.1.0
>> ~~~



> *For Windows*, run:
>> ~~~bash
>> git switch master
>> ~~~
>> this will output:
>> ~~~console
>> Switched to branch 'master'
>> ~~~
>> now run:
>> ~~~bash
>> python random-reads.py --version
>> ~~~
>> this will output:
>> ~~~console
>> random-reads.py 0.1.0
>> ~~~

NOTE: IF you get the following error `zsh: permission denied: ./random-reads.py`, then run
>> ~~~bash
>> chmod +x random-reads.py
>> ~~~
>> followed by:
>> ~~~bash
>> ./random-reads.py --version
>> ~~~
>> this will output:
>> ~~~console
>> random-reads.py 0.1.0
>> ~~~

As you can see, this version of `random-reads.py` is the old version "0.1.0" instead of "0.2.0"!

## 6.4 Merging branches to finalise main

Once we're happy with this new feature, we can merge the branch back into the main branch, run:

~~~bash
git merge -m"Update random-reads.py to allow user-specified read length" specify-readlength
~~~
this will output:
~~~console
Merge made by the 'ort' strategy.
 random-reads.py | 5 +++--
 1 file changed, 3 insertions(+), 2 deletions(-)
~~~

<!-- ~~~console -->

<!-- $ git merge specify-readlength -->
<!-- Updating 0200bb9..a2fe48f -->
<!-- Fast-forward -->
<!--  random-reads.py | 5 +++-- -->
<!--  1 file changed, 3 insertions(+), 2 deletions(-) -->

<!-- ~~~ -->

<!-- Depending on versions, you may get thrown into vim with the message "Please enter a commit message to explain why this merge is necessary, especially if it merges an updated upstream into a topic branch." At this point do the following in vim: -->


<!-- > 1. Press `i` (i for insert) -->
<!-- > 2. Write your merge message e.g., `Update random-reads.py to allow user-specified read length` -->
<!-- > Press `esc` (escape) -->
<!-- > Write `:wq` (write & quit) -->
<!-- > Then press `enter` to exit -->



> OK, we've now merged the `specify-readlength` code back into our main branch and added a commit message for this. We're back in the main branch but our code has been updated.


You can test the code has been updated by running
~~~bash
./random-reads.py --version
~~~
this will output:
~~~console
random-reads.py 0.2.0
~~~


## Key Points
> - It is advised to create a new branch if you want to modify something e.g., existing code.
> - Use `git checkout` to create a new branch and `git status` to check the new branch.
> - Use `git add` and `git commit` to add the modified version via a new index.
> - Use `git switch main` to get back to main and view the original version.
> - Use `git merge` to implement the new feature into the main branch.
