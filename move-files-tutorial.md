#Tutorial: Moving Files into a Different Directory from the Terminal

###What this means/why it matters:
Often when we save files we don't put much thought into where we store them on our computer. Consequently, the lack of organization can make these files difficult to find later on. In order to take control over the way files are organized on our computers, we will likely have to make changes to the way they're automatically arranged when we save them. Through a single, simple command line in the terminal, we can easily move a file from the directory it was originally saved in to the directory we want it to be saved in. 
###How to move a file from one directory to another:
- The basic command line for this maneuver is: ` mv -i yourfilename.txt destination-directory ` 
- In order to ensure that the file you want moved is in your current directory, enter in command line ` ls`. This will list the contents of the directory and show that the desired file is actually located here. 
- Then, you will want to change to the destination directory (where you want to move the file). To do this you will use the ` cd ` command, which means change directory.
	- For example, if you start out in the downloads folder of your home directory, which in this example will be ` ~/downloads `, and you want to change to your documents folder in the root directory, which for this tutorial will be `/My Documents `, you would enter into the command line ` cd /My\ Documents `. 
	- If you do not know where exactly your destination directory/folder is located, you can use the ` cd .. ` command, which will take change to the previously directory. After entering this command, use ` ls ` to determine if this if your target, and if it isn't then repeat this command. 
- Once you reach the destination directory, use the command `pwd` to find out the root of the directory. Take note of it, as this will be necessary later on. 
	- In my example, when I enter `pwd` I receive the output `/My\ Documents`.
- Next, change back to the original directory (where the file you want to move is located) using the command `cd originaldirectorynamehere`.
	- For example, for me this would be `cd ~/downloads`.
- Finally, you will use the command line included at the top of the tutorial: `mv -i yourfilename.txt destination-directory `.
	- In this example, the command would be `mv -i download1.txt /My\ Documents `. `download1.txt`, in this case, is the file I want to move into my document folder. 
	- `mv` means move.
	- `-i` makes the maneuver interactive and asks for permission to replace the same file if it already exists in the destination directory/folder. 
