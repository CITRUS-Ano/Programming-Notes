# Git Manager

### Git basic command

#### Initialize a repository
```command line
git init
```

#### View the status of repository
```command line
git status
```

#### Add files into buffer
1. Add all files in current directory
```command line
git add .
```

2. Add designated file
```command line
git add index.html
```

3. Commit only desinated files and don't use 'git add ...'
```command line
git commit -a ""
```

#### View edits that haven't been added yet 
```command	line
git diff
```

#### Undo the last addition
```command line
git reset
```

#### Sign in
```command line
git config --global user.name ""
git config --global user.email ""
```

#### Commit files
1. The most concise way
```command line
git commit -m "some description of commit"
```

2. Open a file to commit a description
```command line
git commit
```

3. Use other editor to open a file to commit a description
```command line
git config --global core.editor emacs
```

#### Ignore some files
```command line
nvim .gitignore
```

#### Stop caching a file
```command line
git rm --cached filename
```
---


### Git branch
#### Add a new branch
```command line
git branch branch_name
```

#### Switch to another branch
```command line
git checkout branch_name
```

#### merge branch
```command line
git merge another_branch
```

#### Check branch
```command line
git branch
```

#### Delete branch
1. Common delete
```command line
git branch -d branch_name
```

2. Force delete
```command line
git branch -D branch_name
```

---


### Push to website
#### Bind repository address
```commnand line
git remote add origin url_repository
```

#### commit files to website
```command line
git push --set-pustream origin branch_name(master)
```

#### Remember username and password
```command line
git config creadential.helper store
```
---


### Modify repository content
#### Download repository
```command line
git clone url_repository
```

#### Resubmit to website
```command line
git push
```

#### Update repository from website
```command line
git pull
```




