# Assignments of week 1 

##  1) Create a file, assign permissions (read, write, execute) to different user categories (owner, group, others), and practice changing permissions using chmod.

```bash
 touch file1.txt

 ls -l file1.txt

 # output : -rwxrwxrwx 1 gopal gopal 0 Jun  1 06:19 file1.txt

 # Changing Permissions

 chmod 400 file1.txt

<!--# output : -r-xr-xr-x 1 gopal gopal   0 Jun  1 06:19 file1.txt-->

chmod 711 file1.txt

<!-- # output : -rwx--x--x 1 gopal gopal    0 Jun  1 06:41 file1.txt-->

## 2) Execute basic Linux commands (e.g., ls, cd, mkdir, rm, touch) to manipulate files and directories, with an emphasis on understanding their usage.
