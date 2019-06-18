
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
