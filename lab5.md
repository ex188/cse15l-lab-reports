# Part 1 – Debugging Scenario
## Original Post
#### What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?

  * Computer: MSI
  * System: Win 10 x64
  * Terminal: Bash

#### Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.


![image](https://github.com/ex188/cse15l-lab-reports/assets/98847913/b8f3ac3c-95db-4988-90e2-76b3b6772a93)

  NullPointerException was throw in the terminal. The expect value should be 0 since there's nothing inside the String.

#### Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.

  * Command Running: 
    javac NullPointerBug.java
    java NullPointerBug
  * No test case or command-line arguments
  * Working directory:
    ~/Desktop/CSE 15L/lab report 5

## TA Response

Thank you for your information

From here, we can see that you have initial a variable called message and you want to see the length of the message.
Since you set message to null, the String won't exist, which means the length will be undefined.
If you want a empty string that length is zero, you will ne to initial the variable as "". 

## Student Trying

![image](https://github.com/ex188/cse15l-lab-reports/assets/98847913/f00fb8bd-b5fe-4735-9c96-8bc6e0e25e55)

Bug Explanation:
In the code before, I have a variable message initialized to null. The subsequent line attempts to invoke the length() method on the message object. However, since message is null, a NullPointerException is thrown at runtime.

## SetUp Info
  * Files:
    NullPointerBug.java
    NullPointerBug.class
  * Directory: 
    ~/Desktop/CSE 15L/lab report 5
  * Content of file before fix:
  ```
      public class NullPointerBug {
        public static void main(String[] args) {
          String message = null;
          int length = message.length(); // Causes NullPointerException
          System.out.println("Length: " + length);
          }
      }
  ```
  
  * Content of file After fix:
  ```
      public class NullPointerBug {
        public static void main(String[] args) {
          String message = "";
          int length = message.length(); // Causes NullPointerException
          System.out.println("Length: " + length);
          }
      }
  ```
  * Command line to trigger the bug:
    javac NullPointerBug.java
    java NullPointerBug
    
  * Fix:
      To fix this bug, you need to ensure that the object is properly initialized before using it. In this case, you can assign an empty string to the message variable instead of null.
      By initializing message with an empty string, the length() method can be safely invoked without causing a NullPointerException.
     
## Part 2 – Reflection   
  One of the biggest thing that I've learn in the second half of the quarter is the new programing language Bash. We use bash to test out codes. It is a pretty wired programing language and 9how for people who just learn java or python to use. But it seems helpful when we building testers. And I believe for TA's who need to grade student's homeeworks. This skill must be helpful.
  Then the vim, text editor. It is pretty straight foward. A build in language in vscode. Including lessons of how to use it. Once we get used to this editor, it will be really efficiency aand speed/ There's a lot of short cuts that can help us edit files quicker. Over all, I've learned a lot throught the second half of the quarter. It is one of the useful class that I've ever take. 
