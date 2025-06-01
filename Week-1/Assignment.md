# Assignments of week 1 

##  1) Create a file, assign permissions (read, write, execute) to different user categories (owner, group, others), and practice changing permissions using chmod.

```bash
 touch file1.txt

 ls -l file1.txt

 # output : -rwxrwxrwx 1 gopal gopal 0 Jun  1 06:19 file1.txt

 chmod 400 file1.txt

# output : -r-xr-xr-x 1 gopal gopal   0 Jun  1 06:19 file1.txt

chmod 711 file1.txt

 # output : -rwx--x--x 1 gopal gopal    0 Jun  1 06:41 file1.txt
 ``` 

## 2) Execute basic Linux commands (e.g., ls, cd, mkdir, rm, touch) to manipulate files and directories, with an emphasis on understanding their usage.

```bash
touch id.txt 

mkdir learningDevops 

ls

ls -l

ls -la

cd learningDevops

cd ..

rm -r learningDevops

rm file1.txt

mkdir -p parent/child1/chile2

rm -rf parent
```

## 3) Using the terminal, practice navigating through directories, listing file contents, and moving files to different locations.

```bash
mkdir movefile

touch sharetoShift.txt

cp sharetoshift.txt movefile

mv sharetoshift.txt filemoved

```

## 4) Create a new user and group, set their permissions, and explore user management commands like useradd, usermod, and userdel.

```bash 
sudo useradd user_name

sudo passwd user_name

sudo userdel --remove user_name 

sudo useradd -s /bin/bash -d /home/dir

sudo chown user_name:user_name_group /path/to/file



```

## 5) Git Commands

```bash

git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"

git init

git add file1 file2 file3

git add .

git ls-files

git commit -m "commit message" 

git push origin main 

git pull origin main 
```
## 6) Setup a remote repository in Local , Add a file and commit or save the changes and push to master branch

```bash
mkdir project

cd project

git init

git remote add origin https://github.com/gopalepic/Celebal-Internship.git

echo "making connection with a remote repositary and uploading files on it " > Readme.md

git add Readme.md

git commit -m "Commit"

git branch -M master 

git push -u origin master 

```

## 7) Merge types, Create a new branch then commit and push the changes to new branch and merge it with the master branch using pull request.

```bash

git checkout -b Branch1

touch fileinBranch1

git add fileinBranch1

git commit -m "Commited in Branch 1 " 

git push -u origin Branch1

```

## 8) Undo the last commit or remove the last created file from remote repo using CLIdcgh

```bash

PS E:\Celebal\Week-1> git log --oneline

#   a4268a2 (HEAD -> Branch1, origin/Branch1) added new branch and uploading content on it
#   0dfd9e5 (origin/main, origin/HEAD, main) 4 parts done
#   9b999c0 more detailing
#   d7b280b 1st question completed
#   639f57d first upload

git reset --hard HEAD~1          # Removes last commit locally
git push origin HEAD --force     # Forces remote to match local


```