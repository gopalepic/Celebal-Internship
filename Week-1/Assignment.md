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


