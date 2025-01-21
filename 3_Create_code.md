# Chapter 3. Create our first code

## Learning Outcomes
> - Preparing some code to add to our repository.
> - Examining the status of our repository before committing.

## 3.1 Write some code
Now that we have a repository set up it is time to write some code.
This can be anything, but here we'll use a python script to generate random fastq data.

Open your text editor or use a terminal text editor (like nano) to write the python code into a new file

Make sure you save the file into your workspace directory, calling it `random-reads.py`.

For example, you could do:
> `nano random-reads.py`
> copy and paste the contents below into the file
> then `Control + O` and `ENTER` to write out
> then `Control + X` to exit

~~~python
#!/usr/bin/env python3

# Include the necessary modules:
import argparse
import logging
import sys
from random import choices

# Define a version for your code:
__version__ = "0.1.0"

# Define a function that returns an error with a sensible error message:
def error(msg, exit_code=1):
    logging.error(msg)
    sys.exit(exit_code)

if __name__ == "__main__":
    # Set the CLI. This is the primary way that your users will interact with your program.
    parser = argparse.ArgumentParser(description="Generate random FASTQ data")
    parser.add_argument("-V", "--version", action="version", version=f"%(prog)s {__version__}")
    parser.add_argument("-v", "--verbose", dest="verbosity", default="warning", choices=["error", "warning", "info", "debug"], help=f"Set logging level (default warning")
    parser.add_argument(dest="n_reads", type=int, metavar="N", help="Number of reads to generate")
    args = parser.parse_args()

    # Set up logging:
    logging.basicConfig(format="%(levelname)s: %(message)s", level=args.verbosity.upper())
    
    # Define the nucleotide set:
    nucleotides = "ACGT"
    logging.info(f"selecting from nucleotide character set: {nucleotides}")

    # Define the phred score set:
    phred = """!"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJ"""
    logging.info(f"selecting from PHRED character set: {phred}")

    # Generate the random reads:
    logging.info(f"generating {args.n_reads} reads")
    for read_i in range(args.n_reads):
        print(f"@READ_{read_i + 1}")
        print("".join(choices(nucleotides, k=10)))
        print("+")
        print("".join(choices(phred, k=10)))
~~~

## 3.2 Check the status of our new code

Now that we've created a file, let's see what git tells us:

~~~console
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        random-reads.py

nothing added to commit but untracked files present (use "git add" to track)
~~~

> This is telling us that there is a new file in the workspace (`random-reads.py`) but that it has not yet been added to the index.

## Key Points
> - You can prepare any form of material e.g., code, text, figures etc. to commit to your repository.
> - Always check the status of your repository after creating files, and before committing.
