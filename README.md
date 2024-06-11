# GIT Course

Kind of guide for Git Course by [**Codesai**](www.codesai.com)


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
git log --graph --all --pretty='%Cred%h%Creset -%C(auto)%d%Creset %s %Cgreen(%ar) %C(bold blue)<%an>%Creset'

git checkout main
echo "A change in main branch" >> hola.txt
git commit -am 'Change in main'

git log --graph --all --pretty='%Cred%h%Creset -%C(auto)%d%Creset %s %Cgreen(%ar) %C(bold blue)<%an>%Creset'
```


### Day 5 -- My first Merge

```shell
git checkout main

git merge
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

