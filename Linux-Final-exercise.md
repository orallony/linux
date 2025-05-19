# Linux Advanced Exercises

## Exercise 1: Advanced Navigation and File Operations
1. Use the `ls -l` command to list files and directories in the current location with detailed information.
2. Navigate to your home directory using a relative path with the `cd` command.
3. Create a directory structure: Inside your home directory, create `projects` directory, and within it, create `project1` and `project2` directories using a single command.
4. Move the `duplicate.txt` file from `exercise_folder` to `project1` using a single `mv` command.
5. Rename `project2` to `completed_project` using the `mv` command.

## Exercise 2: Text Editing and Input/Output Redirection
1. Use `nano` to edit `duplicate.txt` and add some sample text to it.
2. Use the `cat` command to display the contents of `duplicate.txt` while numbering all lines.
3. Create a new file called `output.txt` and use `echo` to write the contents of `duplicate.txt` into `output.txt`.
4. Append the contents of `duplicate.txt` to `output.txt` using the `>>` operator.

## Exercise 3: Advanced File Manipulation
1. Inside `project1`, create a directory named `images`.
2. Move all files from `exercise_folder` into `images`.
3. Use the `rm -r` command to remove the `exercise_folder` and its contents.
4. Create a hard link named `hardlink.txt` to `duplicate.txt` using the `ln` command.
5. Check the inode numbers of `duplicate.txt` and `hardlink.txt` using the `ls -i` command.
6. Investigate the manual for the `rm` command using the `man` command.

## Exercise 4: Advanced Permissions and Ownership
1. Create a new group called `developers` using the `addgroup` command.
2. Add both `student` and `student2` to the `developers` group using the `usermod` command.
3. Set the group ownership of the `project1` directory to the `developers` group using the `chown` command.
4. Grant execute permissions for the owner and the group on `output.txt` using `chmod`.
5. Create a new user named `manager` and make them the owner of the `completed_project` directory using `chown`.

## Exercise 5: Symbolic and Hard Links
1. Create a symbolic link named `sym_link.txt` pointing to `duplicate.txt` using the `ln -s` command.
2. Verify the symbolic link by listing files with `ls -l`.
3. Create another hard link to `output.txt` named `output_hardlink.txt`.
4. Delete the original `output.txt` file. Check if you can still access its content through `output_hardlink.txt`.
5. Identify the differences between symbolic links and hard links using the `stat` command on both types of links.

## Exercise 6: Basic Regular Expressions (Regex)
1. Use `grep` to find all occurrences of the word `error` in a file named `log.txt`.
2. Search for lines starting with the word `Warning` in `log.txt`.
3. Find lines ending with the word `completed` in `log.txt`.
4. Using `grep`, list lines containing either `error` or `failed` from `log.txt`.
5. Use `grep` to match lines with exactly 5 characters from a file named `codes.txt`.
