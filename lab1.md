# CSE 15L Lab Report 1

## Installing VScode

In order to install VS code, go to this website [Link](https://code.visualstudio.com/), it will show this following page:

![image](https://user-images.githubusercontent.com/98847913/230797124-d390eab2-7fea-4460-b5f8-32685dcc8d63.png)

Click download, it should lead you to a page that has all the different version of downloads. Choose the correct download that matches your computer. 

After installed, you should open the VS code with this page (color may look different but is't ok):

![image](https://user-images.githubusercontent.com/98847913/230797345-b9cecb37-8265-4cd8-9913-9d5e46429e60.png)

## Remotely Connecting

The first thing should do for Windows user. 
Install git. Go to this link: [Link](https://gitforwindows.org/)

You will to in this page:
![image](https://user-images.githubusercontent.com/98847913/230797506-894ceda6-75ee-4bbf-bb16-e83b2f96b2d9.png)
Click Download button. Follow the instuction that the software provides. And install. 

After installed, follow the steps:
Go to VS code, use (Ctrl + `) to open new terminal or just choose terminal  on top of the contral bar, and click new terminal.
It should pop a terminal window on the bottom like this:

![image](https://user-images.githubusercontent.com/98847913/230797727-b1fa5486-3cc5-46b8-8be2-5ce501137eaa.png)

**If you want to use the Git Bash** (If not, go down where it says Next)

Open the command paltte using Ctrl + Shift + P
It will be like this:

![image](https://user-images.githubusercontent.com/98847913/230797778-828e0734-bf2e-47f9-86f6-e7d4bce14e4a.png)

Type the following command in the space: Select Default Profile
Select Git Bash from the options.
Click on the + icon in the terminal window:

![image](https://user-images.githubusercontent.com/98847913/230797935-d2cf6312-ee99-47a2-b00a-f77d55c638a9.png)

It will create a new terminal that is using Git Bash:

![image](https://user-images.githubusercontent.com/98847913/230797997-7eef37bf-b201-4a4e-bdc7-dfb4a9c2d48e.png)

Next, we use ssh. Open a terminal in VScode
Type in the following command

```
$ ssh cs15lsp23--@ieng6.ucsd.edu
```

The -- part should be the characters that you have on your account that's different with the command above. 
You don't have to type in $. Just a way to write command. 

Then it shoud go to this message:
```
The authenticity of host 'ieng6.ucsd.edu (128.54.70.238)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.     
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
```

Type: yes and press enter. 
It will ask for your password, type it in and press enter.
Then it will have something like this:

```
Last login: Tue Mar 14 14:33:46 2023 from 100.83.51.76
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/hourly.2023-04-02_2001: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/hourly.2023-04-04_2001: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/hourly.2023-04-04_1601: Stale file handle
Hello cs15lsp23bz, you are currently logged into ieng6-201.ucsd.edu

You are using 0% CPU on this system

Cluster Status 
Hostname     Time    #Users  Load  Averages  
ieng6-201   14:55:01   9   1.39,  1.11,  1.09
ieng6-202   14:55:01   6   4.27,  4.19,  4.19
ieng6-203   14:55:01   10  1.13,  1.20,  1.22

 
Sun Apr 09, 2023  2:55pm - Prepping cs15lsp23
[cs15lsp23bz@ieng6-201]:~:13$ 
```

Your terminal is connected to CSE basement's computer. 

## Trying Some Commands

Now try to run some commands in your terminal. Do it both on your computer and the remote computer. 
You can try the following:
* ```cd ~```
* ```cd```
* ```ls -lat```
* ```ls -a```
* ```ls -f```
* ```ls <directory> ```
 put <directory> as ```/home/linux/ieng6/cs15lsp23/cs15lsp23abc``` where abc is another group members' username. 
* ```cp /home/linux/ieng6/cs15lsp23/public/hello.txt ~/```
* ```cat /home/linux/ieng6/cs15lsp23/public/hello.txt```
* You can also use ```ls --help``` to find more ```ls``` commands.

You should see something similar to this in your terminal while running on remote computer:
 
For example, this is a ```ls -a``` command, it will show all the entries staring from . to your current directory 
 ![image](https://user-images.githubusercontent.com/98847913/230798791-2d7cc5c8-029b-4a14-ad1a-db7ffce5ac3b.png)

Here's another example of doing ```ls -f```, you will list all the commands in directory order. 
 ![image](https://user-images.githubusercontent.com/98847913/233855966-7a95f0fb-fadb-410e-93df-0cb3d7808af8.png)

In order to log out of the remote server in your terminal, type ```Ctrl-D``` or run the command ```exit```
