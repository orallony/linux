# Linux File Management Practice

## Creating Directories and Files

1. Create a directory named `Data` and inside it the following files (note: some are hidden files):
   - `.data`
   - `data1`
   - `data2`
   - `data_3`
   - `my_name`

2. Create a directory named `Zoo` and inside it the following files:
   - `keeper`
   - `animals`
   - `Visitors`

3. Create a directory named `Progs` and inside it the following files:
   - `prog1.c`
   - `prog2.c`
   - `small_prog`
   - `medium_prog`
   - `.pro1.exe`
   - `my_prog`

4. Create a directory named `Family` inside the `Zoo` directory.

## Creating Files and Writing to Them

5. Use the `nano` text editor to create a file named `My_name` and write:
   - On the first line: your name
   - On the second line: your address

6. Create a file named `My_family` and write the names of three family members — one per line.

7. Make sure the files `My_name` and `My_family` are under the `Family` directory.

## File Operations

8. Copy the file `My_name` to a new file named `name`:
   ```bash
   cp My_name name
   ```

9. Rename the file `My_family` to `Family`:
   ```bash
   mv My_family Family
   ```

10. Create a file named `Whole_family` by concatenating the files `Family` and `name`:
    ```bash
    cat name Family >> Whole_family
    ```

11. Display the contents of the `Whole_family` file:
    ```bash
    cat Whole_family
    ```

## Directory Operations

12. Navigate to your home directory:
    ```bash
    cd ~
    ```

13. Rename the `Zoo` directory to `My_zoo`:
    ```bash
    mv Zoo My_zoo
    ```

14. Copy the `Family` directory and its contents to your home directory:
    ```bash
    cp -r My_zoo/Family ~
    ```

15. Delete the `My_zoo` directory and its contents:
    ```bash
    rm -rf My_zoo
    ```

## Checking Home Directory Size

16. Check the size of your home directory:
    ```bash
    du -hs ~
    ```

## Additional Practice Tasks

17. Create a directory named `Projects` and inside it create two subdirectories: `2023` and `2024`.

18. Inside the `2023` directory, create files named `report1.txt`, `report2.txt`, and `summary.log`.

19. Move the files `report1.txt` and `report2.txt` into a new subdirectory named `Reports` under `2023`.

20. Rename `summary.log` to `yearly_summary.txt`.

21. Create a symbolic link in your home directory pointing to `~/Projects/2023/Reports`.

22. Create a hidden directory named `.config` inside your home directory.

23. Inside `.config`, create a file named `settings.conf` and add at least three configuration lines (key=value format).

24. List all hidden files and directories in your home directory using the appropriate command.

25. Use the `touch` command to create five empty files named `a.txt`, `b.txt`, `c.txt`, `d.txt`, `e.txt` in one command.

26. Combine the contents of three files (`a.txt`, `b.txt`, and `c.txt`) into a new file named `abc_combined.txt`.

27. Append the current date to a file named `logfile.txt` using the `date` command.

28. Display the number of lines, words, and characters in the file `Whole_family` using a single command.

29. Create a compressed archive (`.tar.gz`) of the `Projects` directory.

30. Extract the archive you just created into a directory named `Projects_backup`.

31. Find all `.txt` files in your home directory and list their paths in a file named `all_txt_files.txt`.
