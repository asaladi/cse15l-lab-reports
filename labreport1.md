# Tutorial for remote server logging (sshing)

## Step 1: Getting access to your remote account

Follow this [Link](https://sdacs.ucsd.edu/~icc/index.php) to get your account username. Reset your password using the site with the same password or a different one to set up the credentials on your account. This process takes aroung 15 minutes to complete, so the account should be set after 15 minutes.

## Step 2: Download Visual Studio Code
We will be using the terminal in Visual Studio Code, which you should download from their [site](https://code.visualstudio.com/). Download the appropriate version according to your computer's operating system. The application can be customized to your own styles, but it should look like this...
![image](https://user-images.githubusercontent.com/122575267/215636753-96dd993a-c8b5-4e58-b85e-a11eb052aeb8.png)

 - My screen may look different because it has a file open, on the home screen, there is an option to open files from your computer

##Step 3: Downlading Git and opening the terminal
Download git for your computer for the operating system you are using with the [link:](https://git-scm.com/download/win). Once it is downloaded, open the terminal in Visual Studio Code. In the command pallette of VSC, type Select Default Profile and click on it. From the options your are given, select Git Bash. In the terminal window, press the "+" button and wait a few seconds for the bash terminal to load. 

## Step 4: Connecting to the Remote server
Use the ssh command to log into your personal resmote server. The username you use should be in the format of cs15lwi23zz@ieng6.ucsd.edu, with the "zz" replaced by the characters provided in your own username. The password is the same as the one you reset it to. Once you are logged in, your screen should look something like this...
![image](https://user-images.githubusercontent.com/122575267/215636676-58cc517e-b52b-40d4-8b7f-a8cfdc1230f7.png)

## Step 5: Try Running Commands
Now that you are in your remote account, you can explore the files in your directory using different different commands. Some of these include:
- `cd` which opens a directory
- `cd ~` which takes you to the home directory
- `ls` which lists all the things in the current directory
- `ls -a` which lists all files, even hidden ones
- `cat` to view the contents of files
 
To go out of the terminal, run exit or ctrl-D

Here is an example of what running various commands looks like:
![image](https://user-images.githubusercontent.com/122575267/215637904-e17e0558-3b31-485a-875b-f33188bfbec5.png)

That is all!

