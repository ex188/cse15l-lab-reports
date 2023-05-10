# Lab Report 3

## Researching Commands

I have chosen the find command for this exercise. Here are four interesting command-line options for the find command along with two examples for each option:


### Option: -type

This option allows you to search for files based on their type.

* Example 1 (Files):

```$ find ./technical -type f -name "*.txt"```

* Output:

```
.
.
.
./technical/plos/pmed.0020272.txt
./technical/plos/pmed.0020273.txt
./technical/plos/pmed.0020274.txt
./technical/plos/pmed.0020275.txt
./technical/plos/pmed.0020278.txt
./technical/plos/pmed.0020281.txt
```
(All txt type files came out as result)

* Example 2 (Directories):

```$ find ./technical -type d -name "plos"```

* Output:

```./technical/plos```

Source: I found out about the -type option from the official find command manual page. You can access it by running man find in the terminal.


### Option: -size
This option allows you to search for files based on their size.

* Example 1 (Files):

```$ find ./technical -type f -size +1k```

* Output:

```
.
.
.
./technical/plos/pmed.0020268.txt
./technical/plos/pmed.0020272.txt
./technical/plos/pmed.0020273.txt
./technical/plos/pmed.0020274.txt
./technical/plos/pmed.0020275.txt
./technical/plos/pmed.0020278.txt
./technical/plos/pmed.0020281.txt
```
(All files size is larger than 1KB)

* Example 2 (Directories):

```$ find ./technical -type d -size -100k```

* Output:

```
./technical
./technical/911report
./technical/biomed
./technical/government
./technical/government/About_LSC
./technical/government/Alcohol_Problems
./technical/government/Env_Prot_Agen
./technical/government/Gen_Account_Office
./technical/government/Media
./technical/government/Post_Rate_Comm
./technical/plos
```
(All Directories size is smaller than 100 KB)

Source: I learned about the -size option from the tutorial "Linux Find Files By Size" on nixCraft: https://www.cyberciti.biz/faq/how-do-i-find-the-largest-filesdirectories-on-a-linuxunixbsd-filesystem/


### Option: -mtime
This option allows you to search for files based on their modification time.

* Example 1 (Files):

```$ find ./technical -type f -mtime -7```

* Output:

```
.
.
.
./technical/plos/pmed.0020258.txt
./technical/plos/pmed.0020268.txt
./technical/plos/pmed.0020272.txt
./technical/plos/pmed.0020273.txt
./technical/plos/pmed.0020274.txt
./technical/plos/pmed.0020275.txt
./technical/plos/pmed.0020278.txt
./technical/plos/pmed.0020281.txt
```
(All files that is modified in the last 7 days)

* Example 2 (Directories):

```$ find ./technical -type d -mtime -1```

* Output:

```
./technical
./technical/911report
./technical/biomed
./technical/government
./technical/government/About_LSC
./technical/government/Alcohol_Problems
./technical/government/Env_Prot_Agen
./technical/government/Gen_Account_Office
./technical/government/Media
./technical/government/Post_Rate_Comm
./technical/plos
```
(All Directories that is modified in the previous day)

Source: I discovered the -mtime option from the article "Find Files in Linux, Using the Command Line" on Linode Library: https://www.linode.com/docs/guides/find-files-in-linux-using-the-command-line/

### Option: -exec
This option allows you to execute a command on each found file.

* Example 1 (Files):

```$ find ./technical -type f -name "*.txt" -exec cat {} \;```

* Output:

```
        ...Author JŠ participated in the design of the study and
        carried out tissue culture and flow cytometry experiments.
        Author KH participated in flow cytometry experiments and in
        the design of the study. Author JGV participated in the
        design of the study and in its coordination...
```
(A whole lot of text in txt files that get the command ```cat``` and printed out)

* Example 2 (Directories):

```$ find ./technical -type d -name "plos" -exec ls -l {} \;```

* Output:

(This output shows all the detailed file information for the Directory by the command ```ls -l``` that is used on the directories)

Source: The -exec option is a widely used feature of the find command. I learned about it from various online resources and documentation, including the find command manual page.
