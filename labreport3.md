# Lab Report 3
## Researching Commands: Less command options 

### Option #1: -N
Shows line numbers when viewing file with less

Example #1:
```
less -N written_2/*/*/HandRIbiza.txt
```
Output:
![image](https://user-images.githubusercontent.com/122575267/218634152-53a38639-5ff6-477f-b625-41500c646cfe.png)

This is an example of how the line numbers appear when viewing the HandRIbiza.txt file with the less command. THe numbers are not actually part of the file, they are added by the "-N" option. We can see that the file is 20 lines total.

Example #2:
```
less -N written_2/*/*/Bahamas-History.txt
```
Output:
![image](https://user-images.githubusercontent.com/122575267/218642253-3e226986-65a8-47f7-89d1-e54ef900f089.png)

This shows the same thing as in the first example, but we see that for some display lines they are not enough to fit a full line from the text, so there will be multiple line 6s, or 10s, or 11s.

The -N option would be useful when opening a file and wanting to know which line you are on in the file, if you want to use it as refernece for then or later.

Source: https://phoenixnap.com/kb/less-command-in-linux

---

### Option #2: Finding words in the less viewer
The finder option in the less viewer  

Example #1:
```
less written_2/*/*/Bahamas-History.txt
```
And in the viewer...
```
/Lucayans
```

Output:
![image](https://user-images.githubusercontent.com/122575267/218636014-474209a2-5cf4-4a4b-ae94-378024b963f0.png)

While the less viewer is open, we can type a forward slash then the word we are looking for, in this case "Lucayans" to confirm that "Lucayans" is found in both places in the Bahamas-History.txt file.

Example #2:
```
less written_2/*/*/HandRIbiza.txt
```
And in the viewer...
```
/The
```

Output:
![image](https://user-images.githubusercontent.com/122575267/218640665-4afb5185-e579-4d42-9ea8-7e0c06ca06ca.png)

This repeats the same thing done in the first example, but it shows that the finder is case sensitive (only highlights captial The but not lowercase the). To make it not case sensitive, you have to use the "-i" option in the first command.

The finder option would be useful when trying to look for specific key words in a text  file you are looking through. It acts like a ctrl-f but in file readers.

Source: https://phoenixnap.com/kb/less-command-in-linux

---

### Option #3: Open multiple files with less
Viewing more than one file at a time  

Example #1:
```
less written_2/*/*/Bahamas-History.txt
```
and in the viewer to see the next file...
```
:n
```

Output:

first file:
![image](https://user-images.githubusercontent.com/122575267/218639979-2b408f4e-072b-46d6-b370-332df20583db.png)

second file:
![image](https://user-images.githubusercontent.com/122575267/218640304-34a66910-db22-4977-83fd-6b3bd105a80d.png)



By typing in the two files you want to see, you can open both of them and view them one at a time. To switch between files you are viewing, type ":n" in the viewer to view the next file and type ":p" to see the previous file.

Example #2:
```
less written_2/non-fiction/OUP/Kauffman/*.txt
```

Output:
![image](https://user-images.githubusercontent.com/122575267/218638340-9eaa9560-da09-4bd5-b4ea-d2245161ee98.png)

With this command, we can see all 9 txt files in the Kauffman directory, without having to type out every name of the file in the directory. We know this because it says so in the bottom left corner where it says "(file 1 out of 9)".

The option to view multiple files at a time would be useful when you need two files opened atthe same time to compare them or use the infromation from both articles in a way.

Source: https://phoenixnap.com/kb/less-command-in-linux

---

### Option #4: Create bookmarks in the file
Marks down places you want to return to while viewing your file, even after closing it.  

Example #1:
```
less -N written_2/*/*/Bahamas-History.txt
```

In the viewer, select all of line 50 and...
```
m
a //answer to prompt for bookmark name
```
This creates a bookmarks named "a". To return to it...
```
'a
```

Output:
![image](https://user-images.githubusercontent.com/122575267/218641951-e89f585b-1331-43b6-a792-d8a870b93dca.png)

Even after scrolling further down the file, or closing out of it, using the " 'a " command takes us back to line 50 in the txt file Bahamas-History.txt. This suggests that the m feature makes bookmarks in the text with whatever character to assign it to.

Example #2:
```
less -N written_2/non-fiction/OUP/Kauffman/ch1.txt
```
In the viewer, select all of line 50 and...
```
m
a //answer to prompt for bookmark name
```
Then select all of line 20 through 21 and...
```
m
b //answer to prompt for bookmark name
```
This creates a bookmark named "a" for line 50 and "b" for line 20 and 21. To return to it...
```
'a //for bookmark a
'b //for bookmark b
```

Output:
bookmark a:
![image](https://user-images.githubusercontent.com/122575267/218649237-dea08aeb-2523-49f4-8c99-db5b0a6e86cd.png)

bookmark b:
![image](https://user-images.githubusercontent.com/122575267/218649282-e587f218-b198-4a49-a6ab-783a645618ed.png)

This shows that multiple bookmarks can be made with different names.

Source: https://phoenixnap.com/kb/less-command-in-linux
