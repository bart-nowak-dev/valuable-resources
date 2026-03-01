# What is repo:
A catalog containing all information about the current status of the project and its history

THis course is not about git commands. We will learn about how git works. There is a many tutorials in the internet showing commands. Also you can ask LLM.


git config --list
git config --list --global 
git config --list --local
git config --list --show-origin

git init - creates a new local repo

mkdir git_course
cd git_course
git init

WHat inside repo:
.git ?
Just a text files. We can open it and see what is inside.

VIM WTF?

git config core.editor notepad
git config core.editor "open -W -n"

Create directory
replace vim


COMMIT:
What is commit?
The state of the repository at a given moment marked with the calculated SHA1
Contains informationa about: author, creation time, commit message(description of changes)
With Git 3.0 SHA1 will be replaced with SHA256

First commit is a root commit. Good practice is to create it the sooner the better. WIthout code. Only MD file which contains project description. MD -> MArkdown

create file README.md
git add README.md
git commit

Modify README.md
What happened? We have modified working copy/directory
The actual files you see in your folder. This is where you add, delete, or modify code. 

git status  

Good practice:
If your status is longer than one screen it means that probably you had to create commit a long time ago.
So good practice is to commit often.

Why do we need Vesrion Control Systems?
Simplifies work of many people on same project.
Replace ZIP RAR files ;)

CVCS = Centralized Version Control System
SVN = Subversion, CVS
Only one commit locally, Server keeps whole Repository
DVCS = Distributed Version Control System
Git, Mercurial, Bazaar
All machines keep a copy of the whole repository.
