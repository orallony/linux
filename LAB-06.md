# Linux Process Management, Pipes & Filters Practice

## ✅ 30 Exercises with Commands

1. Display all processes running in the current terminal

```bash
ps
```

**svg**

2. Display a detailed list of all running processes

```bash
ps aux
```

**svg**

3. Open a live view of the running processes

```bash
top
```

**svg**

4. Start the `sleep` command for 60 seconds

```bash
sleep 60
```

**svg**

5. Start a `sleep` process in the background

```bash
sleep 60 &
```

**svg**

6. Display the jobs running in the current terminal

```bash
jobs
```

**svg**

7. Start a `sleep` process for 300 seconds in the background and check the jobs list

```bash
sleep 300 &
jobs
```

**svg**

8. Bring background job number 1 to the foreground

```bash
fg %1
```

**svg**

9. Resume stopped job number 1 in the background

```bash
bg %1
```

**svg**

10. Display all running processes and search for processes containing the word `bash`

```bash
ps aux | grep bash
```

**svg**

11. Display all running processes and search for processes containing the word `sleep`

```bash
ps aux | grep sleep
```

**svg**

12. Find the Process ID (PID) of a running `sleep` process

```bash
ps aux | grep sleep
```

**svg**

13. Stop a process using its PID

```bash
kill PID
```

Replace `PID` with the Process ID of the process you want to stop.

**svg**

14. Force a process to stop using its PID

```bash
kill -9 PID
```

**svg**

15. Start a `sleep` process in the background and then stop it

```bash
sleep 500 &
jobs
kill PID
```

**svg**

16. Display the contents of `/etc/passwd`

```bash
cat /etc/passwd
```

**svg**

17. Display `/etc/passwd` and show only lines containing the word `root`

```bash
cat /etc/passwd | grep root
```

**svg**

18. Display `/etc/passwd` and show only the first 5 lines

```bash
cat /etc/passwd | head -n 5
```

**svg**

19. Display `/etc/passwd` and show only the last 5 lines

```bash
cat /etc/passwd | tail -n 5
```

**svg**

20. Count the number of lines in `/etc/passwd`

```bash
cat /etc/passwd | wc -l
```

**svg**

21. Display all files in `/etc` and show only the first 10 results

```bash
ls /etc | head -n 10
```

**svg**

22. Display all files in `/etc` and show only the last 10 results

```bash
ls /etc | tail -n 10
```

**svg**

23. Display the files in the current directory in alphabetical order

```bash
ls | sort
```

**svg**

24. Display the files in the current directory in reverse alphabetical order

```bash
ls | sort -r
```

**svg**

25. Count how many files and directories are displayed by `ls`

```bash
ls | wc -l
```

**svg**

26. Display files in `/etc` that contain the word `conf` in their name

```bash
ls /etc | grep conf
```

**svg**

27. Display processes that belong to the current user

```bash
ps aux | grep "$USER"
```

**svg**

28. Display all processes and show only the first 10 lines

```bash
ps aux | head -n 10
```

**svg**

29. Display all processes and count how many lines are returned

```bash
ps aux | wc -l
```

**svg**

30. Display the first 5 files from `/etc` whose names contain `conf`, sorted alphabetically

```bash
ls /etc | grep conf | sort | head -n 5
```

**svg**

---

## 🔹 10 Exercises Without Commands

1. Display all processes running in the current terminal.

2. Display a detailed list of all running processes.

3. Start a process that sleeps for 200 seconds in the background.

4. Display all background jobs running from the current terminal.

5. Find a running process that contains the word `sleep` in its name.

6. Stop a process using its Process ID (PID).

7. Display the contents of `/etc/passwd` and show only lines containing the word `root`.

8. Display the first 10 lines of `/etc/passwd`.

9. List the files in `/etc` and count how many results are returned.

10. List the files in `/etc`, find names containing `conf`, sort the results alphabetically, and display only the first 5 results.
