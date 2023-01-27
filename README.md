# My Pset (Windows OS and Persistence)

## Pset 1. Execute Windows Program At Startup Using Registry Editor

### Below is my detailed process of how I was able to execute my calculator application (calc.exe) at startup of my windows OS. The process I'll show you below includes mistakes I made before I finally suceeded at my assigned problem set.

The Windows registry editor contains various informations and settings of the PC. It reflects and stores all changes made on the PC. For example, if changes were made to a file's control settings, or if a seperate user on the PC makes changes to their screensaver, all these changes are stored in the registry editor and used for future reference and execution. 

The registry editor is also responsible for executing startup processes at default and its possible to instruct the registry editor to execute any application of your choice at the startup of the PC.

Below are steps I used to execute "calc.exe" at the startup of my Windows 10 OS

### I searched for Registry Editor in Windows search bar and clicked on the Registry Editor application and was shown the page below 

![Registry Editor](https://github.com/xst0rmy/ProblemSet-1/blob/main/1%20copy.png)


 I selected "HKEY_CURRENT-USER" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/2%20copy.png)

### I clicked on "Software" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/3%20copy.png)

### I clicked on "Microsoft" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/4%20copy.png)

### I scrolled down and clicked on "Windows" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/5%20copy.png)

### I clicked on "CurrentVersion" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/6%20copy.png)

### I clicked on "Run" and right clicked to show the option "New" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/7%20copy.png)

##### I selected the option "New" and was presented with more options and I selected "String Value" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/8%20copy.png)

##### I got to find out there was another way to create a new startup process. Click the "Edit" option on the top left section of your screen and click on "New" and click on "String Value" as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/7b.png)

##### You'll be presented with an option to input "Value Name" and "Value Data". Value name describes whatever you want the process to be called, input something memorable, in this example, I used "Execute Cal". Now I think I should have used "Calculator" instead.

##### The Value data describes the path to the executable application you want to execute at startup.

In the image below, I inputed the wrong "Value Data" by mistake

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/7bc.png)


I couldn't understand why the application didn't startup after restarting my PC, then I made changes to the Value Data and the Calculator application as before didn't startup after rebooting. I wanted to fix it what was wrong and I knew it's got to be the Value Data 

The image below shows one of the many times I was about to restart my PC

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/10%20copy.png)

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/11%20copy.png)

Then I made further changes to the "Value Data" as shown in the image below. I felt fairly certain I had figured it out at last (The value data seems more reasonable, or so I thought)

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/12%20copy.png)

As you can already imagine, I was disappointed once again but I was also more determined to make it work. Just then an idea struck me, and I thought, "how about I confirm where the application is stored on the terminal?"

### I opened the Command Prompt and inputed this command on the Terminal:

```

where calc.exe

```

### The image below gives a better description

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/13%20copy.png)


I realised I was using the wrong file path and I made changes as shown in the image below

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/14%20copy.png)

### In the image below, I was restarting my PC

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/15%20copy.png)

## Voila! It worked 

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/16%20copy.png)



# Pset 2. Execute "notepad.exe" every 2 hours using Task Schedular

## Below is a detailed explanation of how I used Task Scheduler to automate the periodic running of notepad.exe.

Task scheduler is an application on windows that is used to automate tasks periodically and it can also be used to automatically startup apps at boot.

There are numerous options available for you to tweak to your needs when scheduling an application in Task scheduler. Below are the steps I followed to achieve my assigned task of getting task scheduler to execute "notepad.exe" every 2 hours.

### In the first image below, I searched for Task Scheduler in windows search bar and clicked on the application.

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/1.png)

### I was presented with the Task scheduler's home page

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/2.png)

### I right-clicked on Task Scheduler Library and clicked on "New Folder"

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/3.png)

### I named the folder 

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/4.png)

### I clicked on the ">" beside the Task Scheduler Library

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/5.png)

### I clicked on my newly created folder

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/6.png)

### I clicked the "Action" tab at the top left side of the screen and clicked on "Create Task" 

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/7.png)

### I gave it a task name. The Description is optional and I choose other settings as I saw important 

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/9.png)

### I clicked on "Triggers" and clicked on "New"

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/8.png)

### I clicked on "Daily" and chose other suitable options in the "Advanced" Section

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/10.png)

### I clicked on "Action" tab and clicked on "New"

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/11.png)

### I chose "Start a program" and clicked on "Browse"  

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/12.png)

### I typed "notepad" in the "File name" menu and clicked on the file name extension that was suggested and I clicked on "Open"

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/13.png)

### The "Program/script" option automatically displays the file path. I clicked on "Ok"

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/14.png)

### I clicked on "Conditions" and set the suitable options and clicked on "Ok"

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/16.png)

### I clicked on "Settings" and again chose suitable options and clicked on "Ok"

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/17.png)

### Now our new task is ready to run. Click the "Run" option on the "Selected Task" at the lower right side of thge screen

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/18.png)

### I closed the task scheduler app and "Notepad" application is already launched on my PC

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/19.png)

### I closed the Notepad application and 2 hours later, the Task Scheduler relaunched the app (Time stamp differs)

![](https://github.com/xst0rmy/ProblemSet-1/blob/main/20.png)

#### That is the comprehensive process I used to execute an application every 2 hours using Task Scheduler.


























