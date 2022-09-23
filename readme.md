## General info
This project is a reminder for some command I usually use to create a new repo on Github.

## Creating a Project Locally
First I create a local project in my home folder and git init:

```
$ mkdir projectName
$ cd projectName
$ touch projectFile.txt
$ git init
$ touch .gitignore
```

## Creating a Repository on github

```
$ gh repo create {projectName} --public
or
$ gh repo create {organizationName}/{projectName} --private
```

## Pushing your local project on github

```
$ git remote add origin https://github.com/{username}/{projectName}.git
$ git branch -M main
$ git add --all
$ git commit -m 'initial commit'
$ git push -u origin main
```