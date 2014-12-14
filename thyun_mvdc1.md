#Simple & Helpful Terminal Commands for Mac Users

This tutorial will show you the basics of how to view your command history, retrieve information from the Internet, and use **-i** to safeguard against commands made in error.

##What and where is the Terminal?
Think of the terminal as a stripped down, bare version of your computer, without the fancy 3D icons and user-friendy interface. With the right language, the Terminal allows you to do everything and more that you can do on your computer. On a Mac, type in "Terminal" into the Spotlight search bar (the magnifying glass on the upper right corner of your screen). Click on "Terminal" and the window will appear.

##History
If you ever forget a specific command you used in the Terminal, simply type in **history** in your Terminal command line, and your history of commands will appear.

You can also use your **up/down arrow keys** (on your keyboard) in the command line to browse through the individual commands you used previously, instead of retyping commands you have already used.


##wget
This command is used to retrieve a file from the Internet into a specific folder in your computer. The steps below outline the *basic* capability of this command: grabbing information written in plaintext from the Web to your computer.

###For Mac Users: Install Brew

Although Mac is based on the UNIX system, it does not automatically use the exact same language of UNIX to run its operating system (iOS). The solution, then, is to install **Brew**. Brew is an online repository, or a kind of central library that offers UNIX tools for download and use. Brew (and other repositories conducive to other systems) manages the packaging of command tools so that your system can run on these commands elegantly and eliminate the blundering that may arise from downloading a hodgepodge of tools seperately without fully understanding how your system works.

To install **Brew**, copy and paste the following command in your Terminal and hit enter:

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Once you have installed **Brew** on your Mac machine, you can now install **wget** (as well as sed, grep, and gawk) by running the following commands in your Terminal *one at a time*:

``` 
brew tap homebrew/dupes
brew install coreutils
brew install findutils --default-names
brew install gnu-indent --default-names
brew install gnu-sed --default-names
brew install gnutls --default-names
brew install grep --default-names
brew install gnu-tar --default-names
brew install gawk
brew install wget
```

**Using wget**
Now that you have installed wget from Brew, now you can try it this command:

1. To begin, go to the folder in which you would like to retrieve a file, using the **cd** (change directory) command. (This step is not crucial because you can use the **mv** command to move your retrieved file to another folder at a later time.) 
	- Remember that the Terminal works in **plaintext**. To be able to view a file or information in the Terminal, you must retrieve a information from the Internet written in plaintext (no encryption). Plaintext files are usually named with the extension **.txt**.
2. Type in `wget [URL path]`
	- Example: `wget http://www.gutenberg.org/cache/epub/2701/pg2701.txt`
3. The file will now be in the folder in which you are currently working in the Terminal, named as the title indicated in the URL. In the example above, the file will be saved as "pg2701.txt"
4. To view the plaintext file in the Terminal, use the **cat** command: `cat [name of file]`
5. To rename the file, you can use the **mv** command:
`mv [original name of file] [new name of file]`
	- *Note:* **mv** means "move," and can also be used to move a file to another folder, which means it has the ability to overwrite other files. If you use this commadn to rename a file, *make sure you are renaming the file to a unique name to avoid overwriting.*

*More powerful iterations of wget will allow you to install programs from the Web onto your computer.*


##The all important -i

For new (or all) users of the Terminal, the -i flag should be used in combination with riskier commands such as mv (move), rm (remove), or cp (copy), all of which have the capability to overwrite other files.

1. In any command, **-i** can be placed after the primary command
	- Example: rm -i file.txt
2. The Terminal (on a Mac) will ask you to confirm the command: `remove [filename].txt?` 
3. To complete the command, simply type in "y" for yes, or "n" for no and hit enter.

*Note: the -i flag can be used in combination with other flags.*

