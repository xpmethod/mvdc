#Terminal Basics  

##Introduction to the terminal  
Finding the terminal in a modern day computer requires a bit of digging, either with a Spotlight search or looking through the Accessories list. Historically, the terminal played a much more central role. Instead of having individual terminals in each machine, computer users would schedule time with a central terminal to log into their own computer, sharing their computing environment with other users. In modern day machines, the terminal emulates this interface. Computers now are more complex and more personal, but at some low level in the operating system remains this incredibly stable way of interacting with your machine, a method that remains readable by humans and programs alike. As a result, any commands written in the terminal work similarly across all machines.  

This tutorial will explore the basics of the terminal: folder structure and file nagivation.  

##The terminal in practice  
###Folder Structure  
1. Open the terminal
2. There are a few symbols that will appear immediately:   
 - The first phrase is your machine name.  
 - The ~ symbol indicates that you are in your home directory, your default location for your machine. If you change your location to another folder, then this symbol will be replaced by the name of that folder. We'll practice this change soon.
 - The name/phrase following that symbol is the user. This name will remain throughout your work in the terminal as the beginning of your command line.  
3. **pwd**  
 - The pwd command stands for "path to working directory," and shows which folder you are in within your machine (e.g. Users/Name means that you're in the "Name" folder within the "Users" folder). For the rest of the tutorial, directory = folder.  
 - These names stand for real folders in your machine. If you were to launch Finder or My Computer, the equivalent would be clicking on the "Users" folder and then clicking on the "Name" folder to get inside it. The / you see in the terminal shows the root of this navigation.   
4. **ls**  
 - The ls command stands for "list," and it also shows you where you are in your machine by listing the folders and files in your current location.  
 - The difference between pwd and ls is that pwd shows you how you arrived at your location, and ls shows you what is available at your location.  
5. **cd** 
 - The cd command stands for "change directory," and it lets you move in and out of folders. cd Test/ moves to the Test directory.  
 - Once you change to a new directory, the name of the folder will appear before your username in the command line.    
 - There are a couple of tricks to cd:  
		- Once you start typing the name of the folder, hitting "tab" will autocomplete your command. (*Get in the habit of tabbing--it will save you from making mistakes when you are working in the terminal.*)  
		- If you want to get back to your home directory, enter cd ~ 
		- If you want to move up one folder, enter cd ..  
		- The folders you can list after cd are limited to those in your current directory.  
6. File structure also includes creating directories. To do this, navigate back to your home directory to avoid making changes to existing folders (pwd and ls to check). 
7. **mkdir**   
 - mkdir newfolder/ creates that folder.
 - You can enter whatever you would like as "newfolder," but be sure to add / to indicate the end of a root.  
 - mkdir stands for "make a directory."  
 - mkdir creates a directory but does not move you into it. In order to navigate into this new folder, use cd newfolder/ (and don't forget to tab).  

###File Navigation  
Up to this point, this tutorial has focused on the structure of your system. We will now turn to the files that this system organizes.  

1. Navigate to your new directory.  
2. **touch**  
 - touch file.txt creates a new plain text file.  
 - The .txt extension means that the file you are "touching" or creating, is a plaintext file, readable by a computer without a specific program.  
 - Like "newfolder," you can enter whatever name as "file." However, without the extension, your computer will be unsure about what kind of file you are creating.  
3. **nano**  
 - nano file.txt allows you to edit file.txt.  
 - nano is a text edit program that runs in the terminal. If you choose, there are other more advanced systems, but nano is the simplest for the purposes of this tutorial.   
 - To exit nano, type control+x, and be sure to select y to save your work. Hit enter to exit the program.    
4. **cat**  
 - cat file.txt lets you read this file in the terminal.  
 - Using cat depends on the type of file; cat is unable to open and read encrypted files that are not plaintext.
5. **cp** (a dangerous command)  
 - cp stands for "copy."
 - cp file.txt file2.txt copies the contents of file.txt into the new file2.txt  
 - cp can also override complete files accidentally, so be especially careful when using it.  
6. **mv** (a dangerous command)  
 - mv stands for "move."
 - mv file.txt file3.txt renames "file" to "file3."  
 - mv file.txt ~/Documents will move the file to the Documents folder in your home directory. You can change the destination of this file by changing the path in the command line.  
 - After you move a file, you are still in the original location, so use cd to change your directory if desired.  
 - mv is also a dangerous command because of its ability to override files.  
7. **rm** (a dangerous command)  
 - rm stands for "remove."  
 - rm file.txt removes the file permanently, which is why this command is dangerous.  
 - To remove a file safely, mkdir trash/ and move the file to this trash folder  
 - rm can also be used with directories. rm -r deletes a directory and its contents recursively. Because this command is especially dangerous at a directory scale, rm -i provides a built-in check before deleting any files or folders.  
