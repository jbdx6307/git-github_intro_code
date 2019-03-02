# quick introduction to use github and github
this repostory contains some basic git commands and tutorials to get things to work. Just in case, in future, if I forgot everything, I can always come back here to pick it up.
## git install and initialization

1. go to https://git-scm.com/downloads
download the software for Windows
install Git choosing all of the default options
2. open the git terminal
  type the following code:
```
# sets up Git with your name
git config --global user.name "<Your-Full-Name>"

# sets up Git with your email
git config --global user.email "<your-email-address>"

# makes sure that Git output is colored
git config --global color.ui auto

# displays the original state in a conflict
git config --global merge.conflictstyle diff3

git config --list

#use atom as editor
git config --global core.editor "atom --wait"
```

## some common commands in shell:
1. list the document in folder `ls`
2. make directory `mkdir` `mkdir -p udacity-git-course/new-git-project && cd $_`
3. change folder `cd`
4. remove folder or directory `rm`

## create a repostroy on the local machine
create a folder to store the repostory
in the folder, right click and choose _git bash here_
type:
`git init`

## create a repostory on github and clone it to local machine
login to github, create a new repostory, copy the link of the repostory
type:
'git clone https://github.com/jbdx6307/git-github_intro_code.git'
after that make sure you cd to the folder of this cloned reporstory
`cd git-github_intro_code`

## check status
`git status`
for example, I just added a readme.md file in to my repostory folder
use `git status`, it will show:
`On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        README.MD

nothing added to commit but untracked files present (use "git add" to track)`
since the file is just placed in this foder , it has not been added to staging,
it has not been committed either

## add file to staging index
`git add <file name>`
`git add README.MD`

after running this commands, check status:
`On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)`

you can also use `git add .`
this will include everyfile in the folder to staging

## commit file
`git commit -m "Initial commit"`
this will commit the files in staging to the reporstory
the -m followed by a string wil aded a short descprtion to this commit.