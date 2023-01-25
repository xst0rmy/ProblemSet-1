# My Pset1 (Windows OS and Persistence)

## 1. Execute Windows Program At Startup Using Registry Editor

### Below is my detailed process of how I was able to execute my calculator application (calc.exe) at startup of my windows OS. The process I'll show you below includes mistakes I made before I finally suceeded at my assigned problem set.

The Windows registry editor contains various informations and settings of the PC. It reflects and stores all changes made on the PC. For example, if changes were made to a file's control settings, or if a seperate user on the PC makes changes to their screensaver, all these changes are stored in the registry editor and used for future reference and execution. 

The registry editor is also responsible for executing startup processes at default and its possible to instruct the registry editor to execute any application of your choice at the startup of the PC.

Below are steps I used to execute "calc.exe" at the startup of my Windows 10 OS

### I searched for Registry Editor in Windows search bar and clicked on the Registry Editor application and was shown the page below 

![Registry Editor](https://github.com/xst0rmy/ProblemSet-1/blob/main/1.png)


### I selected "HKEY_CURRENT-USER" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/2.png)

### I clicked on "Software" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/3.png)

### I clicked on "Microsoft" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/4.png)

### I scrolled down and clicked on "Windows" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/5.png)

### I clicked on "CurrentVersion" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/6.png)

### I clicked on "Run" and right clicked to show the option "New" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/7.png)

### I selected the option "New" and was presented with more options and I selected "String Value" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/8.png)

## I got to find out there was another way to create a new startup process. Click the "Edit" option on the top left section of your screen and click on "New" and click on "String Value" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/7b.png)

#### You'll be presented with an option to input "Value Name" and "Value Data". Value name describes whatever you want the process to be called, input something memorable, in this example, I used "Execute Cal". Now I think I should have used "Calculator" instead.

#### The Value data describes the path to the executable application you want to execute at startup.

In the image below, I inputed the wrong "Value Data" by mistake

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/7bc.png)


I couldn't understand why the application didn't startup after restarting my PC, then I made changes to the Value Data and the Calculator application as before didn't startup after rebooting. I wanted to fix it what was wrong and I knew it's got to be the Value Data 

The image below shows one of the many times I was about to restart my PC

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/10.png)

Then I made further changes to the "Value Data" as shown in the image below. I felt fairly certain I had figured it out at last (The value data seems more reasonable, or so I thought)

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/12.png)

As you can already imagine, I was disappointed once again but I was also more determined to make it work. Just then an idea struck me, and I thought, "how about I confirm where the application is stored on the terminal?"

### I opened the Command Prompt and inputed this command on the Terminal:

```

where calc.exe

```

### The image below gives a better description

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/13.png)

I realised I was using the wrong file path and I made changes as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/14.png)

### In the image below, I was restarting my PC

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/15.png)

## Voila! It worked 

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/16.png)


#2. Execute "notepad.exe" every 3 hours using Task Schedular





