# GIT cheat sheet:
I like to use git bash terminal in windows - it's like a linux shell with git commands added, so the usual linux terminal commands work.

You can open a terminal like this in most cloud environments or a jupyter notebook

## Open Terminal:
	In jupyter lab, go: File -> New -> Terminal
	
## Basic [[Terminal]] commands :
	ls = list directory (dir in CMD)
	ls -a = list directory INCLUDING hidden files!
	cd = change directory
	

### Basic git commands:
Command | result
:----------|---------:
`git remote -v` | see URL of connected reposity (for fetch and push calls)
`git status` | show modified files in working directory, staged for your next commit
`git pull` | fetch and merge any commits from the tracking remote branch
`git fetch` |  that tells the local repository that there are changes without bringing them in
`git add -all` | stages **all changes**
`git add .` | stages new files and modifications, **without deletions**
`git add -u`  | stages modifications and deletions, **without new files**
`git commit -m “{descriptive message}”`| commit your staged content as a new commit snapshot
`git push` | 


### Author Identity
To set your account's default identity, run the following. Omit `--global` to set the identity only in this repository.

`git config --global user.email "you@example.com"` 
`git config --global user.name "Your Name"`  


### REVERT SINGLE FILE
	git checkout <COMMIT #> <file path/name>
	git commit

when asked to explain git message: 
git uses an editor your default editor.
To solve this, use these #vim commands:

		- press "i" (i for insert)
		- write your merge message
		- press "esc" (escape)
		- write ":wq" (write & quit)
		
then press enter

	git push

enter username
paste git token for pw (it will not show any characters to hide pw) then press enter

# Remove sensitive files & comit history
WARNING! ONLY DO THIS ON REPOS YOU ARE FULL OWNER OF!!
MAY BE CONCEQUENCES

https://stackoverflow.com/questions/872565/remove-sensitive-files-and-their-commits-from-git-history

# Changing directories
## Chang Home directory
https://www.shellhacks.com/git-bash-change-home-directory/

The easiest way to set the `%HOME%` environment variable for the current user is by using the built-in graphical editor for environment variables.

To start the environment variables editor: 
1. press the ⊞ Win keybutton to open the “Start” menu, type in `envi` and click on _“Edit environment variables for your account”_.
2. edit user variable with
	Variable name: `HOME`
	Variable value (example): `C:\Users\USER.NAME\`

Alternately, you can set the `%HOME%` environment variable using the following command in Windows PowerShell:

PS C:\> [Environment]::SetEnvironmentVariable("HOME", "**C:\path\to\home**", "User")

Start a new session of Git Bash and run the following commands to change the current directory to the user’s `%HOME%` and verify the new path:

$ cd ~
$ pwd

## Change default directory
https://www.shellhacks.com/git-bash-change-default-directory/
## Change Default Directory in Git Bash

To change the default startup directory of Git Bash, do the following steps:

1.  Right-click on Git Bash’s shortcut icon and go to the `Properties`
2.  In the `Start in` field, paste the path to the desired folder, e.g. `D:\WorkDir`
3.  Remove `--cd-to-home` from the `Target` field if it exists

old directory: `%HOMEDRIVE%%HOMEPATH%`