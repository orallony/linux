# Linux Final Exercise 8855/21 2026

---

## Exercise 1: Basic Filesystem Operations and Navigation

1. Navigate to your home directory and create a directory named `tivonily_basics`.
2. Enter the `tivonily_basics` directory and create three files: `tivonily1.txt`, `tivonily2.txt`, and `tivonily3.txt`.
3. List the files in the directory using a long listing format and verify their creation.
4. Delete `tivonily3.txt`.
5. Rename `tivonily1.txt` to `renamed_tivonily.txt`.

---

## Exercise 2: Filesystem Exploration and Core Shell Commands

1. List the contents of the root directory (`/`) and explore the following directories: `/usr`, `/etc`, `/boot`, `/var`, and `/dev`.
2. Use the `file` command to determine the type of different entries in the root directory (for example: directory, regular file, symbolic link, block device).
3. Use `pwd` to display your current working directory, then navigate to `/`, move to `/usr`, and finally return to your home directory using both `cd` with no arguments and `cd ~`.
4. In your home directory, create a new directory named `tivonily_test` and inside it create four files using expansion: `tivonily_1.txt` to `tivonily_4.txt`.
5. Copy one of the files to a new file named `copy_of_tivonily_1.txt`, rename it to `renamed_tivonily_copy.txt`, and remove the copied file.

---

## Exercise 3: Permissions, umask, and Ownership Management

1. Create a file named `tivonily_symb.txt` and use symbolic `chmod` syntax to grant read, write, and execute permissions to owner, group, and others.
2. Create a file named `tivonily_num.txt` and use numeric `chmod` syntax to set permissions so that:

   * Owner has full permissions
   * Group has read and execute permissions
   * Others have no permissions
3. Set the default file creation mask to `0022` using `umask`, and verify that it was applied.
4. Create two users and groups:

   * User `carlo` with group `fofo`
   * User `lala` with group `bobo`
5. Create a file named `tivonily_data.txt` and change its ownership to `carlo`. Then create a directory named `tivonily_docs` and change its group ownership to `fofo`.

---

## Exercise 4: Text Processing, Wildcards, and Regular Expressions

1. Create the following files with the specified content:

   * `tivonily_example.txt` (basic demonstration text)
   * `tivonily_sample.txt` (text including the word Linux)
   * `tivonily_data.txt` (different variations of the word linux in different cases)
   * `tivonily_logfile.txt` (at least 15 numbered lines)
2. Display the contents of `tivonily_example.txt` using `cat`.
3. Search for the word "Linux" in `tivonily_sample.txt` using `grep`.
4. Display the first 10 lines of `tivonily_data.txt` using `head` and the last 10 lines of `tivonily_logfile.txt` using `tail`.
5. Use wildcards to:

   * List files starting with `t`
   * List files with exactly five characters where the third character is `v`
   * List files ending with `.txt` or `.pdf`
     Then use `grep` with a regular expression to display lines in `tivonily_data.txt` that start with the word "linux" (case insensitive).

---

## Exercise 5: User Management, Processes, Packages, Services, and Scheduling

1. Add a new user named `carlo`, rename it to `fofo`, and then delete the user from the system.
2. Create a group named `lala`, rename it to `bobo`, and then delete the group.
3. Use `top` to observe running processes, use `ps` to list active processes, use `pgrep` to find a specific process ID, and terminate a chosen process using `kill`.
4. Install the `nginx` web server using the system package manager, then remove it from the system.
5. Use `systemctl` to start, stop, enable, and disable the nginx service, and finally create a cron job that runs every hour and writes the text `Hello, tivonily world` into a file named `tivonily_hello.txt`.

---

Good Luck!
