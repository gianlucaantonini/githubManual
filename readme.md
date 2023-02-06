## General info
This project is a reminder for some command I usually use to create a new repo on Github.

## Creating a Project Locally
First I create a local project in my home folder and git init:

```
mkdir projectName
cd projectName
touch projectFile.txt
git init
touch .gitignore
```

## Creating a Repository on github

```
gh repo create yourProjectName --public
```

or

```
gh repo create yourOrganizationName/yourProjectName --private
```

## Pushing your local project on github

```
git remote add origin https://github.com/yourUsername}/yourProjectName.git
git branch -M main
git add --all
git commit -m 'initial commit'
git push -u origin main
```

## (Optional Reminder: Create a virtual env with virtualenv)
```bash

#(OPTIONAL)install virtualenv with pip
pip install virtualenv

#(OPTIONAL)create virtualenv in current project folder
virtualenv yourEnvName

#(OPTIONAL)activate virtualenv
#you have to reactivate everytime you open a new terminal window
source yourEnvName/bin/activate
```
