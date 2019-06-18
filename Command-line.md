
# GIT - with command line

Create folder: **C:\TMP\Jerboa**

Rightclick the folder and choose **GIT-bash here**

Create a file **index.html**

	echo "<h1>Jerboa</h1>" >> index.html

Show files in current directory

	ls
	ls -al

Look at the content in the file

    cat index.html

Create repo

	git init

Show files

	ls
	ls -al
    ls .git
    ls .git/refs



Check your name and email

	git config --global user.name
	git config --global user.email

Look at global configurationsfile

    cat c:/Users/YOURUSERNAME/.gitconfig

Stage and commit the file

	git add index.html
	git commit -m "Header"

To not show the warning about CRLF

    git config --global core.safecrlf false

Create a repo named **Jerboa** in Github

Connect your repo to the repo at Github, e.g:

	git remote add origin https://github.com/happy-bits/Jerboa

Push your changes:

	git push -u origin master

Show status

	git status

Add some introduction texts about jerboa in index.html and then run

	git status

Stage the file and show status

	git add index.html
	git status

(codealong to here)

Add a file **rodentia.html**

	echo "<h1>Rodentia</h1>" >> rodentia.html
	git status

	(index.html is green = staged 
	(rodentia.html is red = not staged)

Commit changes (only the staged file will be commmited)

	git commit -m "Introduction"
	git status

Push your changes

	git push

Remove the files that aren't tracked (in this case rodentia.html)
	
	git clean -f
	git status

Add a chapter about **Diet** in index.html. Stage, commit, push.

	git add index.html
	git commit -m "Diet"
	git push

Clear screen

	clear

Check your log:

	git log
	git log --oneline
	git log --oneline --decorate --graph

See who and when someone has changed a file

	git blame index.html

Add a chapter about **Reproduction**. Save. Use **stash** to put the changes to the side for now.

	git stash

See that the chapter is gone. Change the header **Jerboa** to **JERBOA**. Stage, commit, push.

	git add index.html
	git commit -m "Uppercase"
	git log --oneline

Apply your stash. This will add the chapter **Reproduction** to index.html

	git stash pop

Add, commit and push:

	git add index.html
	git commit -m "Reproduction"
	git push

Regret the last commit (this will remove the chapter Reproduction)

	git revert HEAD
	git push



## Extra 1

Read about and try the following git-commands:
- Stash
- Tag
- Amend
- Revert
- Fetch
- Reset (careful)


## Extra 2

Experiment with branches. Add and switch branches. Do merging.

## Extra 3

Create a new repository and try to do a similair exercise. Change, add and delete files. Stage files. Commit files. Look at the log. Push. Regret changes. Use a stash. Etc


## Extra 4

Collaborate with one of your collegues about a repository. Use the command line to checkin changes. Solve conflicts.

## Extra 5

Read about *hooks* and use try to use it in your repository.





