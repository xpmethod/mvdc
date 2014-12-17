#How to Upload a File to Github  
##by Ryan Thompson  

###Background  
If you want to share files, texts, or collaborate with peers on a group project then Github is the perfect place to operate. You can create your own file, and then use your terminal to push it to the remote server, Github. The public can view your file, and with certain privileges your colleagues can edit your file, allowing for a friendly work space. Github optimizes versioning, preventing too many versions from being made. Now let's go through the steps to uploading your file to Github.  

###Procedure  
1. On Github, create a new repository and give it a name of your choice.  
2. In your terminal, create a new directory using the **mkdir (your new directory name)** command and move the file to be shared into the new directory using the **mv (your file name)** command.  
3. Initialize the Github server by entering the command **gitinit**  
4. Use the following command to link your new directory to the repository created on Github:  **git remote add origin (copy and paste your repository URL here)**  
5. Now you must add your file to the que where it gets packaged before being pushed to the server by typing **git add (your file name)** into your terminal.  
6. It is good practice to check the status of your files after you perform any of the **git add, git commit, or git push** commands. Use the command **git status** to do this. You should see a list of files you've added to be committed.   
7. Now that you've added your file to be packaged, commit it to the package with the command **git commit -m "(write yourself a note here to describe the changes made)"**. Once again use the **git status** command after to ensure everything went smoothly.  
8. Once your file is committed, push it to Github with the command **git push -u origin master**. After you perform your first push, you will only need to type **git push** for future files. Once again check the status.  
9. Now refresh your Github page and check your repository to ensure that the file was successfully uploaded to the server. If it has, CONGRATULATIONS! If not, follow the steps again, carefully from start to finish.  

###Closing  

Hopefully you will find Github of some service to you! Follow these simple steps and you should be able to quickly upload and share files with friends and colleagues. Good Luck!
