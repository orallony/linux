# Linux Regex Practice Exercises

## Exercises with Commands

1.  Find all files starting with 'log' and ending with '.txt'
   ```bash
   ls | grep '^log.*\.txt$'
   ```

2.  Display all lines from a file that contain a 4-digit number
   ```bash
   grep '[0-9]\{4\}' filename.txt
   ```

3.  List files that have a dash in their name
   ```bash
   ls | grep '-'
   ```

4.  Find lines starting with 'ERROR' in a log file
   ```bash
   grep '^ERROR' syslog.log
   ```

5.  Show all lines not containing the word 'success'
   ```bash
   grep -v 'success' report.txt
   ```

6.  Find all filenames that start with 'data_' and end with a number
   ```bash
   ls | grep '^data_.*[0-9]$'
   ```

7.  Find lines where an email is mentioned
   ```bash
   grep '[a-zA-Z0-9._%+-]\+@[a-zA-Z0-9.-]\+\.[a-zA-Z]\{2,\}' file.txt
   ```

8.  Display lines that have repeated words
   ```bash
   grep '\b\([a-zA-Z]\+\) \1\b' file.txt
   ```

9.  List all hidden files
   ```bash
   ls -a | grep '^\.'
   ```

10.  Find all lines that start and end with a digit
   ```bash
   grep '^[0-9].*[0-9]$' file.txt
   ```

11.  Find IP addresses in a file
   ```bash
   grep -E '\b([0-9]{1,3}\.){3}[0-9]{1,3}\b' file.txt
   ```

12.  Show lines with a date in format YYYY-MM-DD
   ```bash
   grep -E '[0-9]{4}-[0-9]{2}-[0-9]{2}' file.txt
   ```

13.  Find phone numbers in the format (123) 456-7890
   ```bash
   grep -E '\([0-9]{3}\) [0-9]{3}-[0-9]{4}' file.txt
   ```

14.  Find lines with tabs in them
   ```bash
   grep '\t' file.txt
   ```

15.  Display lines that do not start with a letter
   ```bash
   grep -v '^[a-zA-Z]' file.txt
   ```

16.  Find all .sh files that start with a lowercase letter
   ```bash
   ls | grep '^[a-z].*\.sh$'
   ```

17.  Show all lines that contain only digits
   ```bash
   grep '^[0-9]\+$' file.txt
   ```

18.  Find lines with hexadecimal numbers (e.g. 0x1A3F)
   ```bash
   grep -E '0x[0-9A-Fa-f]+' file.txt
   ```

19.  List all files that do not contain numbers in their name
   ```bash
   ls | grep -v '[0-9]'
   ```

20.  Find lines that are exactly 10 characters long
   ```bash
   grep -x '.\{10\}' file.txt
   ```

21.  Find filenames with spaces
   ```bash
   ls | grep ' '
   ```

22.  Find lines that end with a question mark
   ```bash
   grep '\?$' file.txt
   ```

23.  Find environment variable patterns like $HOME
   ```bash
   grep '\$[A-Z_][A-Z0-9_]*' file.txt
   ```

24.  Find lines that have both 'error' and 'failed' in any order
   ```bash
   grep -i 'error' file.txt | grep -i 'failed'
   ```

25.  Show only empty lines
   ```bash
   grep '^$' file.txt
   ```

## Exercises without Commands

26.  Find lines in a file that contain exactly 3 words.

27.  Find all filenames that end with a digit followed by '.log'.

28.  Match lines that start with a '#' and are at least 10 characters long.

29.  Identify all lines containing a URL.

30.  Detect filenames that include a capital letter.

31.  Find all lines that contain the same word repeated three times in a row.

32.  Locate usernames that start with 'user' followed by two digits.

33.  Match filenames that do not start with a letter.

34.  Find lines that have a mix of letters and numbers only.

35.  Search for sentences that start with a capital letter and end with a period.

36.  Find lines where the first and last characters are the same.

37.  Match all lines containing a number between 1000 and 9999.

38.  Identify all environment variables written as $VARIABLE.

39.  Find commands that use pipes (|) in them.

40.  Find lines where a word is inside double quotes.

41.  Find filenames that start and end with an underscore (_).

42.  Match all lines that contain any currency symbol (like $, €, £).

43.  Find MAC addresses (e.g., 00:1A:2B:3C:4D:5E).

44.  Match lines that are either entirely uppercase or lowercase.

45.  Find all dates written as DD/MM/YYYY.

46.  Match lines that have a time format like HH:MM.

47.  Identify commands that include redirection operators like > or >>.

48.  Find files whose names include both digits and special characters.

49.  Search for lines with email addresses ending in '.org'.

50.  Find lines that contain a hashtag followed by a word (e.g., #linux).
