<h1>Minimally Viable Tutorial</h1>

<h2>Github for Dummies</h2>

<h3>Marjana Chowdhury</h3>

##Creating a Free Github Account
* Go to https://github.com/
* Create a personal account on the homepage
* Choose the free plan ($0/month) on the Choose your plan page then click “Finish Sign up”
* Click “Let’s Get Started!” and read the information provided. If you don't really understand the information, don't fret! This tutorial is a simple step-by-step guide to Github.

##Creating a Repository
* At your main page, click the plus drop down menu <img src="file:///Users/Ratia/Desktop/Screen%20Shot%202014-12-19%20at%209.58.30%20PM.png" style="width: 25px;"/> <br>
* Click "New Repository"
* Creat a name for this repository. For the purpose of this tutorial, let's call it "Code".
* Add a description (optional)
* Make it public (this is free)
* Click "Create Repository"

##Generating Your SSH Public Key
* Go into your terminal account. On Mac, this program can be found in the Utilities folder in Applications.
* You may already have a public key.<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To check if you do, type:

	$ cd ~/.ssh //This will take you into your ssh directory if you have one
	$ ls //This will show you the contents of the directory.
* If you do have a ssh key, ls will return results that may have files named something similar to id_dsa or id_rsa and a matching file with a pub extension. You will most likely not have a key and so the ssh directory will not exist.
* Now you must create a key <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Type:

	$ ssh-keygen
* Confirm where you want to save the key
* It will prompt you for a passphrase. You may leave this blank if you wish to have no passphrase.
* Confirm your passphrase when prompted to do so.

##Depositing Files into Your Repository
* Save your Markdown file/directory that you wish to deposit into your repository wherever you want in your computer. For the purpose of this tutorial, let's conclude we have a folder called "Notebook" saved to our Desktop. This folder "Notebook" includes several markdown files that we wish to deposite into our "Code" repository. If you do not have markdown, you can download it [here].
	
##The First Way
Type into terminal:

	$ cd Desktop //Takes you into your Desktop directory
	$ ls //Shows all of the folders on your Desktop including the "Notebook" folder
	$ cd Notebook/ //Takes you into your Notebook folder
	$ git init //Initializes the local directory as a Git repository
	$ git add . //Adds the files to the local repository
	$ git commit -m 'Any description you want to write'
* Go into you Github account and into your "Code" repository.
* Copy the remote repository url
* Now go back to terminal <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Type into terminal:

	$ git remote add origin [paste the URL. Should be something like git@github.com:username/Code.git]
	$ git remote -v
	$ git push origin master

##The Second Way
Type into terminal:

	$ cd Desktop //Takes you into your Desktop directory
	$ ls //Shows all of the folders on your Desktop including the "Notebook" folder
	$ cd Notebook/ //Takes you into your Notebook folder
	$ ls //Shows all of your files in the Notebook folder
	$ cd .. //Will take you out of your Notebook folder

* Go into you Github account and into your "Code" repository.
* Copy the SSH clone URL
* Now go back to terminal <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Type into terminal:

	$ git clone [paste the SSH clone URL. Should be something like git@github.com:username/Code.git]
* Terminal will prompt for your passphrase.
<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Type:

	$ cd Notebook/
	$ git add *
	$ git commit -m 'Any description you want to write'
	$ git push origin master
* Check back in your Github repository if all your files are now there.

###END

[here]: http://daringfireball.net/projects/markdown/
	
