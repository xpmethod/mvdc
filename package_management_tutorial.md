#Package Management

##The Basics

###What is Package Management, And Why Should I Care?

Computer users spend the majority of their time operating with two types of things stored on a computer: files and applications. Files include that essay you saved last night, the pdf you downloaded from your email, and your vacation pictures. Applications, on the other hand, *do things*. One of the simplest applications on your computer is the calculator, but applications also include Microsoft Word, your web browser, and any games you might play. You've probably heard the word "app" before; it's short for application.

Put simply, you can think of files as essays and applications as things that let you write them.

Deleting and making files is pretty straightforward. All you have to do is find where it's stored (usually in your Documents folder, if you're a PC user) and click delete. Maybe you even empty your recycle bin every once in a while.

For applications, though, it can get very complex very fast. Installing an application usually means installing the hundreds or thousands of files that it needs to run. If, say, you decide that you're tired of playing that computer game, finding all the places where its files are stored can be almost impossible. And what if you end up deleting something that another one of your applications needs?

Not only that, but let's say you run across a really cool-looking program online, and you want to download it even though it's from sketchy-site.nz.de.exe? How do you know it's safe? (For the record, that website is definitely not safe. But I digress.)

###The Solution: Package Management

The *nix family (basically anything that ends in -nix, like Unix, Linux, etc.) has an elegant solution for this problem. For each "distribution" (your particular variety of -nix), there is an online repository which contains useful programs. Not only is the repository itself secure, but all of the software in it has been subjected to rigorous checks to make sure that a) it won't harm your computer; and b) it actually works.

This by itself wouldn't solve the problem of having all those application files floating around. So the solution involves something else: command line tools which allow you to easily install and uninstall applications in the repository. Put simply, the system helps us to "manage" applications. And since installing an application downloads a "package" of files onto your computer, you can see where "package management" comes from.

###A Brief Package Management Tutorial (for Ubuntu)

Since each distribution of *nix has it's own particular way of doing things, I'm just going to show the way that Ubuntu does things. The general idea in most package managers is the same, though. And the basics aren't very complex.

On Ubuntu, the syntax is fairly simple. First, open your command line.

To install a program, type  
```  
	apt-get install name-of-program
```

If the application isn't in the repository, you'll be informed. Otherwise, you can start using the application once installation completes.

To uninstall something, type   
``` 
	apt-get remove name-of-program
```

That takes care of removing all the files for you! Pretty easy, huh?

If you ever need help for apt-get, I suggest you type    
```
	apt-get -h
```  

And if you ever get strange error messages, I recommend updating apt-get:  
```
	apt-get update
```

or just visit the manpage located here: <http://manpages.ubuntu.com/manpages/saucy/man8/apt-get.8.html>

You'll also probably have to run apt-get commands by putting sudo in front of them, which might also make you enter your computer password to authorize them.

This is getting off topic a little, but sudo is basically a way to tell the computer that you want to run the command as an administrator--which is often a requirement to install things. When using apt-get, sudo is generally safe (for all the reasons discussed above). **But don't try to use sudo to force your computer to do anything without a clear understanding of exactly what you're doing**.

###I've Heard Mac is based on Unix. Do I Have a Package Manager on my Mac Too?!?

The short answer is no. At least, not automatically.

But of course, the helpful people of the internet are already aware of this problem and have been working hard to fix it. While there's no *official* package manager for Mac, there is an unofficial one that is widely regarded as safe and reputable. It's called "Brew", and you can find out more about it here: <http://brew.sh/>

###I Use Windows. Am I Hopeless?

Of course not! I too use Windows (cue horrified gasps from certain readers).

If you're on a Windows machine, your options are fairly limited. Windows handles "package management" in an entirely different way (with "dll files") that incorporate a lot of redundancy and overhead.

If you really want to explore package management--and who doesn't--you can download a ready-to-use shell which supports a package manager. Here are step-by-step directions on how to do that (with the apt-cyg parts relying heavily on the apt-cyg project at <https://github.com/transcode-open/apt-cyg> and their old site at <https://code.google.com/p/apt-cyg/>):

 - Install the shell. (We won't cover this part here. I suggest Babun: <http://babun.github.io/>.)

 - Now we'll install **apt-cyg**. apt-cyg is a package manager that works much like apt-get. Note that the instructions on apt-cyg's github page don't seem to work, so I'm using the ones on their old site. In babun, type:  
```
	svn --force export http://apt-cyg.googlecode.com/svn/trunk/ /bin/
```  
```
	chmod +x /bin/apt-cyg
```

 - Now you're ready to use apt-cyg! Though it's a little less functional than apt-get, the basic commands (install, remove) are the same.
 - Just for fun, we'll try to install bash-completion, which auto-completes things you type in bash. (You might already have bash-completion, but if you try to install it anyway you won't break your computer.)  
```
	apt-cyg install bash-completion
```

If you decide bash-completion is not for you, type  
```
	apt-cyg remove bash-completion
```

For full documentation, visit the apt-cyg site above. You might have to run babun as an administrator either to install apt-cyg or when using apt-cyg to install packages. If that's the case, simply locate the icon for babun on your desktop, right click it, and select "Run as Administrator." If your first "apt-cyg install" doesn't work, I'd recommend doing that.

###Other Types of Repository and Package Management Systems

Different languages have their own repositories, like Ruby (gem) and Python (pep)--and you can use these repositories regardless of what machine you're on as long as you have the language installed. They tend to be repositories to language-specific files, though, and don't tend to host general-purpose things like the *nix repositories.

