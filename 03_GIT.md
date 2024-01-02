# Installing GIT

In this walkthrough you'll get GIT installed on your machine

## Download and Install GIT

In this first part you'll install GIT on your machine.

### Task 1 - Download GIT

First you need to download and install GIT

1. Download GIT

    In any browser, type 

    ```
    git download
    ```  

    This should help you navigate to the page where you can download GIT.  If not, you can use this link:  

    [https://git-scm.com/downloads](https://git-scm.com/downloads)  


### Task 2 - Install GIT

Now you need to install GIT.  Make sure to apply recommended settings as shown in the video and listed here:

1. Run the installer

    Run the installer you downloaded in the previous step.  

1. Select Components
    
    > Windows Explorer Integration:  

    - Open GIT Bash Here (checked)
         This will allow you to right click on a folder in Windows Explorer and open GIT Bash in that folder.
    - Open GIT GUI Here (not checked) 
        This will allow you to right click on a folder in Windows Explorer and open GIT GUI in that folder.  It is almost 100% likely you would use any other GUI tool than this one, so this will just get in the way.  Other GUI options include:
        - GitKraken
        - SourceTree
        - Visual Studio Code
        - Visual Studio
        - etc

    > GIT LFS (Large File Support): (checked)  

    > Associate .git* configuration files with the default text editor? (checked)  

    > Associate .sh files to be run with Bash? (checked)  

    > Check daily for GIT for Windows updates? (checked)  

    > (NEW!) Add a Git Bash Profile to Windows Terminal? (checked - but doesn't work at this time)  

    > (NEW!) Scalar (Git add-on to manage large-scale repositories) (checked - optional)

1. Choosing the default editor used by GIT

    > Use Visual Studio Code as Git's default editor? (selected)  

        Do not use the insider build.

1. Adjusting the name of the initial branch in new repositories

    > Override the default branch name for new repositories? (selected)
        
        This setting makes the name of the default branch `main` in new repositories.  

1. Adjusting the PATH environment

    > Git from the command line and also from 3rd-party software? (selected)  

        This will add the GIT installation to your PATH environment variable.  This will allow you to run GIT from the command line.  

1. Choosing the SSH executable

    > Use bundled OpenSSH (selected)  

        This will use the ssh.exe client that is installed with Git.  This is the preferred option.  
    
1. Choosing the HTTPS transport backend

    > Use the OpenSSL library (selected)  

        Server certificates will be validated using the ca-bundle.crt file.  This is the preferred option.

1. Configuring the line ending conversions

    > Checkout Windows-style, commit Unix-style line endings (selected)  

        This will convert line endings to Windows-style when you checkout files.  This is the preferred option.
    
    > Checkout as-is, commit Unix-style line endings (not selected)  

        This will not convert line endings when you checkout files.  This is not the preferred option for a windows machine because line-endings for *.nix (mac/linux) use a different format for cr/lf than Windows and you will get a ton of notifications about line endings being different for developers.

    > Checkout as-is, commit as-is (not selected)

        This is a very bad option because you will check the files out, convert the line endings then check them in with a non-shared line ending.  This will cause a ton of issues for developers in a shared environment.  If you are the only developer you wouldn't notice any problems.

1. Configuring the terminal emulator to use with GIT Bash

    > Use MinTTY (the default terminal of MSYS2) (selected)  

        This is the preferred option.  MinTTY is a terminal emulator that is part of the MSYS2 project.  It is a very good terminal emulator and is the default for GIT Bash.

1. Choose the default behavior of `git pull`

    > Default (Fast-forward or merge) (selected)  

        This is the preferred option.  This will do a fast-forward merge if possible.  If not, it will do a merge commit.

    > Rebase (not selected)

        Use this option if you are always rebasing your branches.  This is not the preferred option.  You could have some issues if you are not aware of how to work with rebasing.

    > Only ever fast-forward (not selected)

        This is not the preferred option.  This will only do a fast-forward merge.  If a fast-forward merge is not possible, it will fail to pull changes.

1. Choose a credential helper

    > Git Credential Manager (selected)  

        This is the preferred option.  This will use the Windows Credential Manager to store your credentials.  This is the best option for Windows.  This allows you to log in only one time to your GitHub/BitBucket/GitLab/ADO account and uses the credentials from the Windows Credential Manager to authenticate you to the remote repository for every additional operation when required.

1. Configure extra options

    > Enable file system caching (selected)  

        This is the preferred option.  This will cache file system operations to speed up GIT operations.  This is a good option for Windows.

    > Enable symbolic links (not selected)  

        You can turn this on if you want to, but typically you won't need this option on windows. 
        
        From the documentation [https://learn.microsoft.com/en-us/windows/security/threat-protection/security-policy-settings/create-symbolic-links](https://learn.microsoft.com/en-us/windows/security/threat-protection/security-policy-settings/create-symbolic-links): 
        
        This privilege should only be given to trusted users. Symbolic links can expose security vulnerabilities in applications that aren't designed to handle them.
    
1. Configuring Experimental Options

    > Enable experimental support for pseudo consoles (not selected)  

    > Enable experimental built-in file-system monitor (not selected)

1. Completing the installation

    Complete the installation 

## Validate GIT is installed

In this next step you'll validate that GIT is installed and working correctly.

### Task 1 - Validate GIT is installed by Version


### Task 2 - Create a repository and commit a file



## Updating Terminal to Show GIT Bash as an option

In this final step you'll set your Windows Terminal to show GIT Bash as an option.

1. Open Windows Terminal
1. Click on the down arrow next to the plus sign
1. Click on Settings

    When the settings.json file opens, you'll see a list of profiles.  Each profile is a different terminal option.  You can add as many as you want.  You can also change the order of the profiles to change the order they appear in the drop down menu.
1. Open a PowerShell tab to create a GUID

    Run the following command to create a GUID

    ```powershell
    New-Guid
    ```  

    Copy the GUID that is returned.  It will look something like this:

    ```text
    ad15e7fa-85c1-4a3c-828c-c75396b7d22b
    ```   

1. Add the following profile to the list of profiles

    Use the GUID generated above and put it in the `guid` section of this text.  Also, make sure the `commandline` and `icon` sections match the location of your GIT Bash installation (which they should if you installed it in the default location).  
    
    - `%PROGRAMFILES%` is a variable that will resolve to `C:\Program Files` 
    - `%USERPROFILE%` is a variable that will resolve to `C:\Users\<your username>`.

    ```json
    {
        "guid": "{ad15e7fa-85c1-4a3c-828c-c75396b7d22b}",
        "name": "GIT Bash",
        "commandline": "%PROGRAMFILES%/Git/usr/bin/bash.exe -i -l",
        "icon": "%PROGRAMFILES%/Git/mingw64/share/git/git-for-windows.ico",
        "startingDirectory": "%USERPROFILE%",
        "hidden": false
    }
    ```  
