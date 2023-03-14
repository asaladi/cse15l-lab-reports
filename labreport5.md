# Lab Report 5
## Researching Commands: Find command options and uses 

### Option #1: -size
Filters found files based on file size

Example #1:
```
find written_2/ -size 1M
```
Output:
![image](https://user-images.githubusercontent.com/122575267/224876864-dcbf78ca-70dd-4162-86c8-d437b180a1b4.png)


This is an example of how a size maximum can be set on the files to filter the files, in this case filtering for files that are 1MB.

Example #2:
```
find written_2/ -size 1G
```
Output:
![image](https://user-images.githubusercontent.com/122575267/224877691-eaad3433-0744-460f-a669-3dddc3d5d0dc.png)


This shows the same thing as in the first example, but the size parameter can be used in terms of gigabytes rather than megabytes.

The -size option would be useful when trying to filter files of a certain size, if you wanted to know the size of the files you want to manipulate.

Source: [[https://phoenixnap.com/kb/less-command-in-linux](https://www.tecmint.com/35-practical-examples-of-linux-find-command/)]([https://phoenixnap.com/kb/less-command-in-linux](https://www.tecmint.com/35-practical-examples-of-linux-find-command/))

---

### Option #2: -perm
Filters found files based on permisions of file  

Example #1:
```
find written_2/ -type f -perm /u=r
```

Output:
![image](https://user-images.githubusercontent.com/122575267/224879877-686768fa-d194-4c82-b239-d0a0c573fe6d.png)

This is an example of filtering for file permisions based on whether it is read only.

Example #2: 
```
find written_2/ -type f -perm /u=r
```

Output:
![image](https://user-images.githubusercontent.com/122575267/224880358-14e3074a-2c46-4706-b2fe-e0146e9cc527.png)

This is an example of filtering for file permisions based on whether it is executable.

The -perm option would be useful as a way of filtering the permissions of the file and help look at which files for permissions could be useful.

Source: [[https://phoenixnap.com/kb/less-command-in-linux](https://www.tecmint.com/35-practical-examples-of-linux-find-command/)]([https://phoenixnap.com/kb/less-command-in-linux](https://www.tecmint.com/35-practical-examples-of-linux-find-command/))

---

### Option #3: -iname
Filtering finder without case sensitivity 

Example #1:
```
find written_2/ -iname "*ch*"
```

Output:
![image](https://user-images.githubusercontent.com/122575267/224881933-cafe1353-1621-41fa-ab16-4a5ee348ceba.png)

This is an example of how case sensitivity is removed when searching for file names with "ch" in them.

Example #2:
```
find written_2/ -iname "*to*"
```

Output:
![image](https://user-images.githubusercontent.com/122575267/224882388-9d5dfc11-e429-4f79-9d40-17bed00188cf.png)

This example is like the first one, but it for "to". This shows that the command includes when the pattern is seen inside words, and not as a seperate word.
(Example WhereToGo.txt counts and History.txt counts)

The -iname option would be useful so that case sensitivity would not have to be worried about when looking for files

Source: [[https://phoenixnap.com/kb/less-command-in-linux](https://geekflare.com/linux-find-commands/)]([https://phoenixnap.com/kb/less-command-in-linux](https://geekflare.com/linux-find-commands/))

---

### Option #4: Removing found files with -exec rm
Removes files that are being searched for

Example #1:
```
find written_2/ -type f -name "Cuba-History.txt" -print -exec rm -f {} \;
```

Output:
![image](https://user-images.githubusercontent.com/122575267/224883844-0a6bfcbb-8235-4d26-af92-19eb1cdd1583.png)

The image shows that the file Cuba-History.txt was found and printed, then proves is was removed when the file was searched for again and is not found.

Example #2:
```
find written_2/ -type f -name "*.txt" -print -exec rm -f {} \;
```

Output:
![image](https://user-images.githubusercontent.com/122575267/224884841-cbe2f15b-c509-4c30-a83d-8f777fb33139.png)

The image shows that multiple files can be deleted, based on whatever pattern is searched for in the files. In this case it deletes all txt files.

The -exec rm command would be useful for completing two actions in one, finding a file and removing it.

Source: [[https://phoenixnap.com/kb/less-command-in-linux](https://www.tecmint.com/35-practical-examples-of-linux-find-command/)]([https://phoenixnap.com/kb/less-command-in-linux](https://www.tecmint.com/35-practical-examples-of-linux-find-command/))
