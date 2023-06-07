# Lab Report 4
### Log into ieng6
![image](https://github.com/ex188/cse15l-lab-reports/assets/98847913/7e7ff67b-e6f3-4492-a5c2-7134254876e3)

Command: ```ssh cs15lsp23bz@ieng6.ucsd.edu <enter>```

Then type in your password and press ```<enter>```

(If you already saved your password through lab instructions, you can skip the password type in part.)

### Clone your fork of the repository from your Github account
![image](https://github.com/ex188/cse15l-lab-reports/assets/98847913/209d92f4-8f83-43a4-a639-a1e57d0547d8)

Command: ```git clone https://github.com/ex188/lab7 <enter>```

The command will clone the lab7 files from github

### Run the tests, demonstrating that they fail
![image](https://github.com/ex188/cse15l-lab-reports/assets/98847913/c9943964-631b-41be-a688-f70cdc08bcf8)

Command: ```cd lab7 <enter> javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter> java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExampleTestes <enter>```

These commands will go into lab7 files, compile and run the terter for lab7.

### Edit the code file ListExamples.java to fix the failing test:

type ```vim ListExamples.java``` and ```<enter>```

![image](https://github.com/ex188/cse15l-lab-reports/assets/98847913/e7bd8efc-8dfd-429a-a11d-dfe70e74f723)
 
type "/index2" then ```<enter>```   (```/``` is the word searching in vim, type in what ever word you need to search after it)

follow by ```<shift> n```           (use ```shift+n``` to move to the next word that is the same)

press ```<l>``` six times,          (```<l>``` is to move the cursor to the left)

use ```<i>```                       (```<i>``` to enter insert mode)
  
```<backspace>```                   (delete a character in insert mode)
  
type ```<2>```
  
```<esc>```                         (exit insert mode)
  
type ```":wq!"```                         (save and exit the file)
  
lastly press
 ```<enter>```          


### Run the tests, demonstrating that they now succeed

After that use 
```<up><up><enter>```
to run the test again. (```<up>``` is to run the last command)
  
![image](https://github.com/ex188/cse15l-lab-reports/assets/98847913/f369f933-5947-4143-bd1f-d82e016dd38b)


### Commit and push the resulting change to your Github account

type ```git add ListExamples.java``` and ```<enter>```

type ```git commit``` and ```<enter>```
 
It will show up this page

![image](https://github.com/ex188/cse15l-lab-reports/assets/98847913/9f97f604-dce6-41ca-8f1d-daf7dae8513c)

Press ```<i>``` to enter insert mode to comment when commiting

![image](https://github.com/ex188/cse15l-lab-reports/assets/98847913/9becf03a-080a-4aa2-953e-1c49a473a536)

```<esc>``` to exit insert mode and type ```":wq"``` to save the exit the file

![image](https://github.com/ex188/cse15l-lab-reports/assets/98847913/755876f7-2051-4bd2-a3db-21775b39140e)

Now type in ```git push <enter>```

![image](https://github.com/ex188/cse15l-lab-reports/assets/98847913/1f4be4e6-39ea-4ae9-941d-8d94e276f955)

enter your account name and press ```<enter>```

enter your password and press ```<enter>```

![image](https://github.com/ex188/cse15l-lab-reports/assets/98847913/bda5d580-0a33-4ed7-ada0-0d8632b0b8d1)

Push successfully!!
