---
title: Installing XCode, Haskell, and Pandoc on older versions of Mac OSX  
author: Cole Sayer  
date: December 6, 2014  
---

# Objective

This tutorial is for those of you who have outdated versions of Mac OSX. The biggest hurdle for me has been successfully installing add-ons like XCode and Pandoc as the newest releases are in general only compatible with the latest operating system. I am currently working on an older MacBook Pro with OSX 10.7.3, but the following guide should work for 10.6 and later. 

The following tutorial should be followed sequentially. To install Haskell you will need XCode, and to install Pandoc you will need Haskell. All terminal commands will be in **bold**.  

# XCode Command Line Tools

First you will need Xcode. Or more specifically, you will need the Command Line Tools which are a part of Xcode. You can’t find previous versions of Xcode at the App Store. Instead you have to go to Apple’s IOS Developer site.  

1. Go to <https://developer.apple.com/downloads/index.action> to access the downloads page for older versions of Xcode.  
2. Log in using your Apple ID or you may have to first create a developer ID and then log in.  
3. Locate the link for Command Line Tools that corresponds to your version of OSX.  
4. Download, double click the package icon, and follow the instructions to install.   

# Haskell Platform 

Now that you have the Command Line Tools, you will be able to download and install the Haskell Platform. The Haskell platform is a collection of software packages, tools, and libraries that resolve many of the compatibility issues between machines. 

1. Go to <https://www.haskell.org/platform/mac.html> to access the downloads page for Haskell Platform.  
2. Click the download link, double click the package icon, and follow the instructions to install. (The Haskell platform takes up a lot of space 1.16gb)  
3. Once Haskell is installed, open your terminal. 
4. Type: **ghci** press enter. 
5. You will see a few lines of text ending with the word prelude. This will confirm Haskell is installed.
6. hold: **ctrl d** to exit from Haskell.

# Pandoc

Now that Haskell is installed, we can download and install Pandoc directly from the terminal.

1. Still in terminal, type: **cabal update**  
2. Then type: **cabal install pandoc**  
3. This will run for quite a while. It took my computer nearly an hour.  
4. Next, type the following line: **export PATH="$HOME/Library/Haskell/bin:$PATH"**  
5. Finally, type: **pandoc --version** to confirm that pandoc is installed.  

