# Linux Hard Links & Symbolic Links Practice

## ✅ 30 Exercises with Commands

1. Create a directory for practicing links and enter it

```bash
mkdir -p ~/links-lab
cd ~/links-lab
```

**svg**

2. Create a text file named `original.txt`

```bash
echo "Hello Linux" > original.txt
```

**svg**

3. Display the contents of `original.txt`

```bash
cat original.txt
```

**svg**

4. Display the inode number of `original.txt`

```bash
ls -li original.txt
```

**svg**

5. Create a hard link named `hardlink.txt`

```bash
ln original.txt hardlink.txt
```

**svg**

6. Display the inode numbers of the original file and the hard link

```bash
ls -li original.txt hardlink.txt
```

Both files should have the same inode number.

**svg**

7. Display the inode number and hard-link count of both names

```bash
stat -c '%n: inode=%i, links=%h' original.txt hardlink.txt
```

**svg**

8. Add a new line through the hard link

```bash
echo "Added through the hard link" >> hardlink.txt
```

**svg**

9. Display both files and verify that their contents are identical

```bash
cat original.txt
cat hardlink.txt
```

**svg**

10. Change the permissions through the hard link

```bash
chmod 600 hardlink.txt
```

**svg**

11. Verify that the permission change appears on both names

```bash
ls -li original.txt hardlink.txt
```

Because both names use the same inode, they also share the same permissions.

**svg**

12. Create a regular copy of `original.txt`

```bash
cp original.txt copied-file.txt
```

**svg**

13. Compare the inode numbers of the original, hard link, and copied file

```bash
ls -li original.txt hardlink.txt copied-file.txt
```

The original and hard link should have the same inode. The copied file should have a different inode.

**svg**

14. Add information to the original file and compare all three files

```bash
echo "Another line" >> original.txt
cat original.txt
cat hardlink.txt
cat copied-file.txt
```

The new line should appear in the original and hard link, but not in the copied file.

**svg**

15. Find all names in the current directory that refer to the same file as `original.txt`

```bash
find . -samefile original.txt
```

**svg**

16. Delete the original filename

```bash
rm original.txt
```

**svg**

17. Verify that the data is still accessible through the hard link

```bash
cat hardlink.txt
ls -li hardlink.txt
```

Deleting one name does not remove the data while another hard link still exists.

**svg**

18. Create a new file using the old name `original.txt`

```bash
echo "This is a new original file" > original.txt
```

**svg**

19. Compare the new original file with the existing hard link

```bash
ls -li original.txt hardlink.txt
cat original.txt
cat hardlink.txt
```

They should now have different inode numbers and different contents.

**svg**

20. Create a symbolic link named `symlink.txt`

```bash
ln -s original.txt symlink.txt
```

**svg**

21. Display the symbolic link and its target

```bash
ls -l symlink.txt
```

The output should show:

```text
symlink.txt -> original.txt
```

**svg**

22. Display the path stored inside the symbolic link

```bash
readlink symlink.txt
```

**svg**

23. Compare the inode numbers of the symbolic link and its target

```bash
ls -li original.txt symlink.txt
```

The symbolic link and target should have different inode numbers.

**svg**

24. Read the original file through the symbolic link

```bash
cat symlink.txt
```

**svg**

25. Add a line through the symbolic link and display the original file

```bash
echo "Added through the symbolic link" >> symlink.txt
cat original.txt
```

The symbolic link redirects the operation to `original.txt`.

**svg**

26. Display the full resolved path of the symbolic link

```bash
readlink -f symlink.txt
```

**svg**

27. Delete the target of the symbolic link

```bash
rm original.txt
```

**svg**

28. Verify that the symbolic link is now broken

```bash
ls -l symlink.txt
cat symlink.txt
```

The `cat` command should return a “No such file or directory” error because the target no longer exists.

**svg**

29. Recreate the target and verify that the symbolic link works again

```bash
echo "The target exists again" > original.txt
cat symlink.txt
```

The symbolic link works again because its stored path now points to an existing file.

**svg**

30. Create a symbolic link to a directory and use it

```bash
mkdir documents
echo "Course notes" > documents/notes.txt
ln -s documents documents-link
ls -l documents-link
cat documents-link/notes.txt
```

A symbolic link can point to a directory.

**svg**

---

## 🔹 10 Exercises Without Commands

1. Create a directory named `links-practice` and enter it.

2. Create a file named `report.txt` containing the text `Linux Report`.

3. Display the inode number of `report.txt`.

4. Create a hard link named `report-hard.txt` that refers to `report.txt`.

5. Verify that `report.txt` and `report-hard.txt` have the same inode number.

6. Add a line through `report-hard.txt` and verify that it appears in `report.txt`.

7. Delete `report.txt` and verify that its data remains available through `report-hard.txt`.

8. Create a new file named `target.txt` and create a symbolic link named `target-link.txt` that points to it.

9. Display the path stored inside `target-link.txt` and compare its inode number with the inode number of `target.txt`.

10. Delete `target.txt`, verify that the symbolic link is broken, and then recreate the target to make the link work again.
