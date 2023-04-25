# Lab Report 2 - Servers and Bugs (Week 3)

## Part 1
Code for StringServer:
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    String output="";

    public String handleRequest(URI url) {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().equals("/")) {
                return String.format("");
            }
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    output += (String)(parameters[1])+"\n";
                    return String.format(output);
                }
            }
            return "404 Not Found!";
        }
    }


public class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

When doing ```/add-message?s=Hello``` command:

![image](https://user-images.githubusercontent.com/98847913/234123301-ca418b6a-9906-419d-9393-67469ac1d3a5.png)

It will call the handleRequest method. 
The the relevant arguments will be ```/``` + ```add-message``` + ```s``` + ```=``` + ```Hello``` five parts. These will be catch while using handleRequest method. 
Every values will cause the change. The handleRequest will catch all the different parts of the argument before ```Hello``` in order to process throught the add message function. If any of the parts is missing, the go through process will fail. ```Hello``` which is the last argument that will effect on output.

![image](https://user-images.githubusercontent.com/98847913/234123427-7db36b1c-f627-4d2b-85a9-c90e047b62d9.png)

It will also call on the handleRequest method
The the relevant arguments will be ```/``` + ```add-message``` + ```s``` + ```=``` + ```https://github.com/ex188/cse15l-lab-reports/edit/main/lab2.md``` five parts. These will be catch while using handleRequest method. 
Every values will cause the change. The handleRequest will catch all the different parts of the argument before ```https://github.com/ex188/cse15l-lab-reports/edit/main/lab2.md``` in order to process throught the add message function. If any of the parts is missing, the go through process will fail. Even though the last argument is a link of another website, but by the method, everything after ```=``` will become a String value that will be add to the website's display.


## Part 2

A failure-inducing input for the buggy program, as a JUnit test and any associated code:

```
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```

An input that doesn’t induce a failure, as a JUnit test and any associated code:

```
  @Test
  public void testReversedShortArray() {
    int[] input1 = {1,2,3 };
    assertArrayEquals(new int[]{3,2,1 }, ArrayExamples.reversed(input1));
  }
```

The symptom, as the output of running the tests :

![image](https://user-images.githubusercontent.com/98847913/234126813-c19f4d05-9aba-4d3f-915b-dc5a7ce76c7b.png)

The bug, as the before-and-after code change required to fix it:

```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
  ```
    
  ```
    static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[arr.length - i - 1]=arr[i];

    }
    return newArray;
  }
  ```
The bug is that in the reversed method, it tries to assign values from the new empty array to the existing array. Which is completely opposite. It also returns the original array instead of the new array. In order to run the method correctly, assign value from original array to the new array. Then return the newArray value. 

## Part 3
Things that learned:

* We can start a server by import a URI java class with build method.
* ```curl``` can be used in command line to access web parges. 
* Even though I already knew about the Junit testing and debugging methods, it is still a really useful technique to help coding people get rid of the mistakes. Watch symptom - read error message from tester - debug - test again. Going through this process can help us clearly figure out the problems and save us a lot of time from debuging randomly. 
