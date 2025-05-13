# Linux Links and Permissions Practice

## ✅ 30 Exercises with Commands

1. Create a file `file1.txt` and a hard link to it named `link1.txt`  
   `touch file1.txt && ln file1.txt link1.txt`

2. Create a symbolic link to `file1.txt` called `sym1.txt`  
   `ln -s file1.txt sym1.txt`

3. Create `project.log` and make it read-only for all users  
   `touch project.log && chmod 444 project.log`

4. Make `link1.txt` writable by the owner only  
   `chmod u+w,go-w link1.txt`

5. Create a file `shared.txt` and give full permissions to all users  
   `touch shared.txt && chmod 777 shared.txt`

6. Create `backup/` directory and make it accessible only by owner  
   `mkdir backup && chmod 700 backup`

7. Create `notes.txt` and revoke read permission from others  
   `touch notes.txt && chmod o-r notes.txt`

8. Add execute permission for group on `run.sh`  
   `chmod g+x run.sh`

9. Create a file and set permissions to 644  
   `touch file2.txt && chmod 644 file2.txt`

10. Set permissions of `log.txt` to 755  
   `chmod 755 log.txt`

11. Create a symbolic link to a directory  
   `ln -s /etc sym_etc`

12. Use `ls -li` to check inode numbers for `file1.txt` and `link1.txt`  
   `ls -li file1.txt link1.txt`

13. Remove the source file and access it via the hard link  
   `rm file1.txt && cat link1.txt`

14. Check that symbolic link breaks after deletion of the source  
   `rm sym1.txt && ls -l sym1.txt`

15. Create a file and make it executable only by the owner  
   `touch script.sh && chmod 700 script.sh`

16. Remove all permissions from `secret.txt`  
   `chmod 000 secret.txt`

17. Grant read permission to group on `shared.txt`  
   `chmod g+r shared.txt`

18. Create a file and give read/write to owner and group, none to others  
   `touch dual.txt && chmod 660 dual.txt`

19. Create multiple files and set them to 600  
   `touch a.txt b.txt c.txt && chmod 600 a.txt b.txt c.txt`

20. Create a directory and set 755 recursively  
   `mkdir -p dir/sub && chmod -R 755 dir`

21. Create a hard link in same partition  
   `ln log.txt loglink.txt`

22. Create symbolic link to `/var/log/syslog`  
   `ln -s /var/log/syslog syslog_link`

23. Use `stat` to check permissions of a symbolic link  
   `stat sym1.txt`

24. Make a script executable for all users  
   `chmod a+x script.sh`

25. Remove write permissions from group on all `.conf` files  
   `chmod g-w *.conf`

26. Set file permission to `rw-r--r--` using numeric format  
   `chmod 644 example.txt`

27. Grant only execute permission to others  
   `chmod o=x execute.sh`

28. Revoke all permissions from group and others on a file  
   `chmod 700 private.key`

29. Create a script and give it `rwxr-xr-x` permission  
   `touch deploy.sh && chmod 755 deploy.sh`

30. Set directory `secure_data` to `rwx------`  
   `mkdir secure_data && chmod 700 secure_data`

---

## 🔹 20 Exercises Without Commands

1. Create a hard link and confirm both files share the same inode.  
2. Create a symbolic link to a non-existent file and observe behavior.  
3. Make a file executable by group and others only.  
4. Revoke all permissions from a file and then try to access it.  
5. Create a directory and remove all permissions from it.  
6. Create a file and allow only group access (read/write).  
7. Grant execute permissions on all `.sh` files in the current directory.  
8. Remove read permissions from a file for all users except the owner.  
9. Change a file’s permission to be readable by all, but writable by none.  
10. Make a symbolic link inside `/tmp` pointing to a file in your home directory.  
11. Create a file and set `640` permissions using symbolic notation.  
12. Remove execute permission from owner only.  
13. Create a hidden file and link to it with a symbolic link.  
14. Set directory permissions to `rwxr-x---` for a group collaboration folder.  
15. Create two hard links to a file, then delete the original and verify access.  
16. Make a file writable by others only.  
17. Assign full permissions to a file and then limit to read-only for group.  
18. Test access of a broken symbolic link.  
19. Create a file and deny all access to it using `chmod`.  
20. Create a symbolic link to a directory and navigate into it using `cd`. 
