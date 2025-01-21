# Pre-Workshop Git Setup

## Installing Git on different platforms

### Git Installation on Windows

If your computer runs Windows, please follow the instructions provided by Cloud-SPAN for [installing git on Windows](https://cloud-span.github.io/00genomics/setup).

**NB**: You can now access a terminal using the "Git Bash" icon.

### Git Installation on Mac

1. Start the Terminal.app program to start an interactive terminal
2. Type `git --version`
3. If you don’t have it installed already, it will prompt you to install it.

**NB**: You can access a terminal using the Terminal.app.

## Post-Install Git Setup

Once git has been installed, you need to tell it who you are, so that any commits you make are in your name.  

You can do this by firstly starting a terminal (see above), and then typing the following commands:

~~~bash
git config --global user.name "Your Name"
git config --global user.email "your.email@mail.com"
~~~

**NB**: Use your own name and email address.

Also, I would recommend adding the SSH key of your laptop to your GitHub account for authentication. Please follow the instructions here: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account

## Github Account Setup

In order to use GitHub, you need an account.  

Follow the instruction on the [GitHub signup page](https://github.com/signup).

**NB**: It will help if you use the same email address for GitHub as you did when setting up git above.

## VSCode Installation & Setup [This will be useful here and for your project]

VSCode is a code editor with lots of features, including the ability to connect your GitHub account. In VSCode, you can share your source code and collaborate with others right within your editor.

If you wish to use VSCode and do not already have it installed, download it from the [VSCode downloads page](https://code.visualstudio.com/download).
