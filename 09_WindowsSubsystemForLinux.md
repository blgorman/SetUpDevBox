# Get the Windows Subsystem for Linux and Ubuntu installed on your machine

You can now run a side-by-side distribution of Linux on your Windows machine.  This is a great way to get access to Linux tools and utilities without having to run a VM.

This is especially useful for doing containerized (modern/cloud-native) development on your machine.

## Task 1 - Install WSL2

For the first task, you'll get WSL2 working on your machine.  It is assumed you currently do not have WSL at all.  You can run WSL2 side-by-side with WSL1 if you need to. For almost everyone, you should just use WSL2 at this point.

1. WSL from the windows store

    You may be able to just get Ubuntu from the windows store and have this just work. In the past, however, it has been necessary from my experience to install WSL2 first.  If you have issues, try installing WSL2 first.

    >**Note:** if you're watching the videos for these walkthroughs you'll see me install Ubuntu and get the error that WSL2 is not installed.  This was what I expected but I wanted to try to see if it would work.  It didn't.  

1. Open a PowerShell terminal as an administrator
1. Type the following command:

    ```PowerShell  
    wsl --install  
    ```  

1. Ensure WSL2 is default

    ```PowerShell  
    wsl --set-default-version 2  
    ```  

1. Reboot the machine

## Task 2 - Install Ubuntu

The installation for Ubuntu should continue based on the WSL installation.  If it doesn't, you can install Ubuntu from the Windows Store.

1. Complete the installation
1. Add a username/password combo for your linux distribution
1. Open any terminal and type `wsl` to get into the linux distribution

    ```PowerShell
    wsl
    ```  

1. Check your distribution version

    ```bash  
    lsb_release -a  
    ```  

1. Run linux commands

    ```bash  
    ls
    sudo apt-get update  
    #etc
    ``` 

## Complete

You now have a windows machine with WSL2 running Ubuntu.  You can use this to run linux commands and utilities on your machine.  You can also use this to run docker containers on your machine.  This will be covered in the next walkthrough.
