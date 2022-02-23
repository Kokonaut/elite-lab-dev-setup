# Installing Python and VSCode on Windows

HEADS UP: You need Windows 10 to install WSL. This was in the pre-req for this course. If you have an earlier version of windows, please notify me.

We will be setting up the Windows Subsystem for Linux for your dev environments.

The purpose of this is to standardize the environments between Windows users and Mac users. Also Linux is the preferred OS for web servers and backend development, I highly recommend getting familiar with it early.

## Quick Overview
With Windows 10, Microsoft gave us the ability to run a subsystem OS inside of Windows. This means that you are running an OS inside of an OS! Since we are using Linux, this feature is called WSL or Windows Subsytem for Linux.

What happens: Windows will install a feature inside of your computer that will allow a separate OS to be run inside of its own program. We will then install Ubuntu (which is a free OS) and use it as our basis of development.

Just a disclaimer: You can totally still develop using Windows. However, I don't recommend it's use when dealing with the basics of Web App development and Web servers. Feel free to explore Windows development on your own time, but for this course's sake, we will be using Linux (in the form of Ubuntu)

## Before You Start
Make sure your Windows version is up to date! Make sure you don't have any pending updates, and if you do, feel free to update and restart your computer. The Zoom link will still be the same.

## Installing WSL
https://docs.microsoft.com/en-us/windows/wsl/install-win10

Please use the official Microsoft documentation to guide the install process for WSL. Microsoft may customize this page based on your OS version, so once again, make sure you are up-to-date.

You only need to follow the instructions to install. This may or may not require you to restart your computer. By default, it should install Ubuntu for you, but if not, then proceed to the next section where you change the default version to Ubuntu.

**Make sure you install Ubuntu.**

Version doesn't matter, just any of the higher ones. For reference, my Windows computer uses Ubuntu 20.04.1 if you want to match my version.

Please make sure that you REMEMBER the username and password you provide (You may also leave a blank password if you wish).

## Installing VSCode
After you have Ubuntu installed, proceed to follow the official Microsoft documentation for setting up VSCode and Python.

https://docs.microsoft.com/en-us/windows/python/web-frameworks#set-up-visual-studio-code

Stop at `Run a simple Python program`

## Setting up Flask

Follow these steps to set up Flask.

https://docs.microsoft.com/en-us/windows/python/web-frameworks#hello-world-tutorial-for-flask

At the very end, you are done when you can open a browser window with the Hello World message.


## Extra

If you finish early, then go read up on Command Line basics. This will be invaluable for anytime you work with the terminal.

https://ubuntu.com/tutorials/command-line-for-beginners#1-overview

https://www.guru99.com/linux-commands-cheat-sheet.html
