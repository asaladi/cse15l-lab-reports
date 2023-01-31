# **Part 1**

## Code:
![image](https://user-images.githubusercontent.com/122575267/215546809-dcfa3058-e05a-4bd8-b422-8a9dca43e8d1.png)
The code used here is mostly recylcled from the NumberServer web server from lab week 2. The Server class is a nested class used in this program to start running the web server in the StringServer class, then the url logic is taken care of be the Handler class. The handler class is one of the parameters used to run the Server and contains the code for what website should be doing.

## Running the program:
![image](https://user-images.githubusercontent.com/122575267/215547321-6d10ab6d-4882-4b90-9471-0a563ea44884.png)

Running from the terminal

## Test #1:

![image](https://user-images.githubusercontent.com/122575267/215549217-c87e74c2-64b5-419a-a111-aee76c023b1b.png)

When first running this program, the URIHandler class sets up the web server to be running functionally, then the logic within the Server class makes the command for adding a string to the text on the screen. The main method takes the port number as an argument, and the handle request method takes in the url as an argument, where it breaks it down to seperate the text that need to be added, and adds it to the Server class instance variables. If the request is run successfully, the text varible is updated with the new text from the request. 

## Test #2:

![image](https://user-images.githubusercontent.com/122575267/215550245-1b425232-203b-40e8-b2df-68c75233c953.png)

This request is no different from the previous, where the handle request method is called with the url adress inputted, and the text that needs to be added isolated so that it can be added to the text variable on a new line and displayed to the screen again.

# **Part 2**
One bug we looked at during week 3 was the bugs in the reverseInPlace() method
Here is the code for this method, whos intended purpose was to reverse an array in place:
![image](https://user-images.githubusercontent.com/122575267/215623220-b7cf8252-abf2-446b-93f9-931e327595a0.png)

Failure inducing input: {2, 4, 6}

```
int[] input1 = {2, 4, 6};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{6, 4, 2}, input1);
```

Output:

![image](https://user-images.githubusercontent.com/122575267/215631384-0fa38f57-2531-47de-ac7b-82af7b0f3e9e.png)

({6, 4, 2} does not equal {6, 2, 6} test failed)

Working input: {3}

```
int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
```

Output:

![image](https://user-images.githubusercontent.com/122575267/215632252-a7737b83-76aa-4e97-951b-466d2fc23902.png)

(green checkmark means test case worked)

Symptom: 
Method gets value of changed array for the next index, so halfway it will become palindromic instead of getting the actual indices that come afterwards

Fixed Code:
Make a temporary int to store current value, then swap index element and element that it needs to be replaced with, make the for loop half of the length

Before:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
}
```

After:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int tempInt = arr[i];
      arr[i] = arr[arr.length-i-1];
      arr[i] = arr[arr.length - i - 1];
    }
}
```

# **Part 3**

In week 2, we learned how to clone programs using github and use them to run web servers on our machines. We experimented with the code for the web server and tested various inputs by changing the url of the link to make the website perform different methods. In week 3, we learned more about debugging and error case handling through junit. Something I did not know before was how to run the files from git hub to work in actual web servers that you can run from your local computer. I also did not know that the webpages could be seen by other people when using remote logins.
