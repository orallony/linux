# Linux File Permissions Practice (`rwx`)

## ✅ 30 Exercises with Commands

1. Create three new text files: `report.txt`, `data.txt`, and `log.txt`
```bash
touch report.txt data.txt log.txt
```

2. Grant the owner read and write access to `report.txt` and `data.txt`
```bash
chmod u+rw report.txt data.txt
```

3. Remove write permissions from the group on `log.txt`
```bash
chmod g-w log.txt
```

4. Add execute permission for others on both `log.txt` and `data.txt`
```bash
chmod o+x log.txt data.txt
```

5. Give full permissions to the owner for all `.txt` files in the directory
```bash
chmod u=rwx *.txt
```

6. Revoke all permissions for others on all `.txt` files
```bash
chmod o= *.txt
```

7. Enable read and write permissions for everyone on `report.txt`
```bash
chmod a+rw report.txt
```

8. Remove the execute bit for all users from `data.txt`
```bash
chmod a-x data.txt
```

9. Set permissions of `report.txt` and `data.txt` to `644`
```bash
chmod 644 report.txt data.txt
```

10. Apply `rwxr-xr-x` permissions to `log.txt`
```bash
chmod 755 log.txt
```

11. Create two scripts: `start.sh` and `stop.sh`, then make them executable
```bash
touch start.sh stop.sh
chmod +x start.sh stop.sh
```

12. Remove all group permissions from `start.sh` and `stop.sh`
```bash
chmod g= start.sh stop.sh
```

13. Make `start.sh` readable and executable only by the owner
```bash
chmod 500 start.sh
```

14. Grant group execute permission on `stop.sh`
```bash
chmod g+x stop.sh
```

15. Make `data.txt` readable by all but writable only by the owner
```bash
chmod 644 data.txt
```

16. Create a directory named `configs` and make it accessible only by the owner
```bash
mkdir configs
chmod 700 configs
```

17. Make all `.sh` files in the directory executable by all users
```bash
chmod a+x *.sh
```

18. Remove read access from group and others on `private.key`
```bash
chmod go-r private.key
```

19. Set `report.txt` and `log.txt` to allow full access to owner and group, read-only to others
```bash
chmod 774 report.txt log.txt
```

20. Set `readonly.md` and `readonly.txt` as read-only for all users
```bash
chmod 444 readonly.md readonly.txt
```

21. Create a directory `shared_docs` with full access for all users
```bash
mkdir shared_docs
chmod 777 shared_docs
```

22. Set `admin.sh` to be executable only by owner and group
```bash
chmod 750 admin.sh
```

23. Remove write access from all users for `template.docx`
```bash
chmod a-w template.docx
```

24. Allow only others to execute `example.sh`
```bash
chmod o=x example.sh
```

25. Set permissions of `info.sh` to read and execute for all
```bash
chmod 555 info.sh
```

26. Set `backup.tar` to have all access removed for group and others
```bash
chmod 700 backup.tar
```

27. Grant write and execute permissions to group on `team.log`
```bash
chmod g=wx team.log
```

28. Remove execute permission for the owner only from `deploy.sh`
```bash
chmod u-x deploy.sh
```

29. Set `locked.file` to no access for any user
```bash
chmod 000 locked.file
```

30. Recursively apply `rw-r--r--` to all `.log` files under the `logs/` folder
```bash
chmod -R 644 logs/*.log
```

---

## 🔹 10 Exercises Without Commands

1. Create three files and assign write-only permissions to the group.
2. Remove all permissions for others from multiple `.conf` files.
3. Add read and execute permissions for everyone on two shell scripts.
4. Set a file to be writable by the owner only, and readable by all.
5. Create a new folder and make it readable and executable by all users.
6. Revoke read permissions from the group on two configuration files.
7. Assign full permissions to group on a `.docx` and `.xlsx` document.
8. Remove execute permission from all `.sh` files in the directory.
9. Set multiple `.txt` files to be accessible only by the owner.
10. Change permissions of three specific files so they are shared only between the owner and the group.
