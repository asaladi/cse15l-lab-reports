# Lab Report 4
## Step 1: Log into ieng6
Type (or copy) the command below, then press enter:

The <user> portion (do not include angle brackets) should replaced with the acount username for your remote server account(press the left arrow key as many times as needed to go back in the command to move your cursor to the <user> area, press the delete button to delete the <user> portion, then type you own username to replace) 
```
ssh <user>@ieng6.ucsd.edu
<enter>
```
If you are prompted for a password, type it, then press enter:
```
<enter password>
<enter>
```

The result should look like this:
![image](https://user-images.githubusercontent.com/122575267/221536515-fc345d67-6277-4f63-8164-e3c79bbd2bca.png)
![image](https://user-images.githubusercontent.com/122575267/221536596-7983d172-d910-4947-962d-9609113d0e9a.png)

## Step 2: Clone your fork of the repository from your Github account
Type (or copy) the command below, then press enter:
The <user> portion (do not include angle brackets) should replaced with the acount username for your remote server account(press the left arrow key as many times as needed to go back in the command to move your cursor to the <user> area, press the delete button to delete the <user> portion, then type you own username to replace) 
```
git clone https://github.com/<user>/lab7
<enter>
```

The result should look like this:
![image](https://user-images.githubusercontent.com/122575267/221540567-03a005a2-9f99-4be0-9958-eaac42e532f3.png)

## Step 3: Run the tests, demonstrating that they fail
Copy the commands below, then press enter after every line:
```
cd lab7
<enter>
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
<enter>
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```
  
The result should look like this:
![image](https://user-images.githubusercontent.com/122575267/221659811-b4587fe7-7a6f-41f4-9f95-e296c595e2d9.png)

## Step 4: Edit the code file to fix the failing test
Copy the command below:

This takes you to the code editor in the terminal.
Press the down arrow key until you reach the ```index1 += 1;``` in the while loop below:

```
while(index2 < list2.size()) {
      result.add(list2.get(index2));
      index1 += 1; //put cursor at begining of this line
    }
```



The result should look like this:
![image](https://user-images.githubusercontent.com/122575267/221661158-83f9b1ae-7d29-4f7f-971b-c9a2d56dee95.png)

Editing the code
```



Step 5: Run the tests, demonstrating that they now succeed

The javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java command was 4 up in the search history, so I used up arrow to access it. Then the java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore command was 4 up in the history, so I accessed and ran it in the same way.


Step 6: Commit and push the resulting change to your Github account
