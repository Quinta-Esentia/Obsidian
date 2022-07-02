# GIT cheat sheet:

## Open Terminal:
	In jupyter lab, go: File -> New -> Terminal
	
## Basic Terminal commands:
	ls = list directory (dir in CMD)
	cd = change directory
	
### REVERT SINGLE FILE
	git checkout <COMMIT #> <file path/name>
	git commit

when asked to explain git message: 
git uses an editor your default editor.
To solve this, use these vim commands:

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