# Install Chocolatey

In this task you'll get Chocolatey installed on your machine.

`Chocolatey` is used to do package installations on Windows machines.  It is similar to `apt-get` on Linux or `brew` on Mac.

## Task 1 - Install via PowerShell

To get Chocolatey installed on your machine, you'll want to run commands from PowerShell as an administrator.

1. First, find the installation instructions on the Chocolatey website

    [Chocolatey Installation Instructions](https://chocolatey.org/install)

1. Open Terminal and start a PowerShell session as an administrator

    ```powershell
    Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
    ```  

1. Restart your terminal

    >**Note:** You will need to restart your terminal for the changes to take effect.  

1. Search for packages at Chocolatey.org

    [Chocolatey Packages](https://chocolatey.org/packages)  

1. Install Python3 (entirely optional)

    In the terminal, type:

    ```powershell
    choco install python3
    ```

## Task 2 - Validate Installation

You now have Chocolatey installed on your machine. You can use it going forward to install common packages on your machine.  

>**Note:** Chocolately is incredibly useful for getting docker to work on a Windows box when you can't use Docker Desktop.  You can use it to install `docker` on your machine to work with WSL.  This will happen in a later walkthrough.

1. Open the terminal again

1. Type the following command:

    ```powershell
    python --version
    ```

    You should see the latest version of Python installed on your machine.

## Conclusion

You have now installed Chocolatey on your machine.  You can use it to install packages on your machine going forward.  You can also use it to install `docker` on your machine to work with WSL.  This will happen in a later walkthrough.  
