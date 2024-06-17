# GIT Course

Kind of guide for Git Course by [**Codesai**](https://www.codesai.com)


## Install Git

[Getting Started - Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)


## Individual workflow


### Day 1 -- Init and first commit

```shell
mkdir my_project
cd my_project

git init
git status

echo "Hola Mundo" > hola.txt
git status

git add hola.txt
git status

# config your name and email
git config user.name "My Name"
git config user.email "myname@codesai.com"

git commit
# "Add my first file to project"
git status
git log
```

### Day 2 -- Edit file

```shell
echo "Hola Europa" >> hola.txt
git status

git diff

git add .  # Add all new and modified files and folders
git status

git commit -m "Add a very interesting line"
git status
git log
```

### Day 3 -- Revert changes

```shell
echo "A little mistake" >> hola.txt
git status

git diff

git restore .
git status
```

### Day 4 -- My first Branch

```shell
git branch feature1
git checkout feature1
# or
git checkout -b feature1

echo "A change in another branch" > another.txt
git add . 
git commit -m 'Change in another branch'

git status

# now is the ugly one
git log

# nice log
git log --oneline --decorate --graph --all

git checkout main
echo "A change in main branch" >> hola.txt
git commit -am 'Change in main'

git log --oneline --decorate --graph --all
```


### Day 5 -- My first Merge

```shell
git checkout main

git merge
```


## GIT BASIC COMMANDS -- some code


### Setup

**Option A: global**
```shell
git config --global user.name "Your name"
git config --global user.email "email@dominio.com"
git config --global core.editor "loved_editor"
```

**Option B: or local to this repo**
```shell
git config user.name "Your name"
git config user.email "email@dominio.com"
git config core.editor "loved_editor"
```

## WORKING WITH REMOTE

### Day 0 -- Alias

```shell
alias | grep git
```


### Day 1 -- Clone and Push

```shell
# Check where we are
pwd

git clone git@github.com:Codesai/git-course-practices.git
git log

echo 'hello' > new-file.txt
git add .
git commit -m 'New file'

git push
```



### Day 2 -- Pull

```shell
#check where we are
pwd
git clone git@github.com:Codesai/git-course-practices.git user1
git clone git@github.com:Codesai/git-course-practices.git user2

# user1 - push some changes

cd user2
git pull
git log

# or

git fetch
git merge
```

### Day 3 -- Diverge with Merge
```shell
# user1 push new changes 

cd user2

# add some changes & commit

git push
#rejected

git pull

# or

git fetch
git merge

# then

git push
```


### Day 4 -- Diverge with Rebase
```shell
# user1 push new changes 

cd user2

# add some changes & commit

git push
#rejected

git fetch
git rebase

# then

git push
```

### Day 5 -- Tag
```shell
git tag
git tag v1.0
git tag -a v1.1 -m 'v1.1'
git show v1.0
git show v1.1

# push
git push --tags
#or
git push origin v1.0
```


## BASICS


### Setup

Option A) global
```shell
git config --global user.name "Your name"
git config --global user.email "email@dominio.com"
git config --global core.editor "loved_editor"
```

Option b) or local to this repo 
```shell
git config user.name "Your name"
git config user.email "email@dominio.com"
git config core.editor "loved_editor"
```

