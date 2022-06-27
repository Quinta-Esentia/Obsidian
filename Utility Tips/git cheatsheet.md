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