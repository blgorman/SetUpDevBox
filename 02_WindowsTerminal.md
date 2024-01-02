## Windows Terminal and PowerShell 7

In this walkthrough you'll get Windows Terminal and PowerShell 7 installed/configured on your machine

## Download and Install Windows Terminal

The first part of this walkthrough is to get Windows Terminal installed on your machine.

### Task 1 - Download Windows Terminal

Begin by downloading Windows Terminal from the Microsoft Store

1. Open the Microsoft Store
1. Search for Windows Terminal
1. Click on the Windows Terminal icon
1. Click on the Install button  

### Task 2 - Configure Windows Terminal

Make sure to pin Windows Terminal to your taskbar

1. Search for Windows Terminal in the start menu
1. Right-click and pin to your taskbar

## Task 2 - Install and Configure for PowerShell 7

Now you need to configure Windows Terminal to use PowerShell 7 as well as PowerShell 5.

### Task 1 - Review PowerShell instances

Open Windows Terminal and review the PowerShell instances that are available.

1. Open a PowerShell tab
1. Get the current version

    ```powershell  
    $PSVersionTable.PSVersion
    ```  

### Task 2 - Download and Install PowerShell 7

In this task you'll download and install PowerShell 7

1. Open a browser
1. Search for PowerShell 7
1. Click on the `Installing PowerShell on Windows` link
1. Navigate to the `MSI` Installer
1. Download the `PowerShell 7.x.x-win-x64.msi` file (if you are on 32-bit windows then you'd have to get the x86 version).  
1. Install it
    - Select options for Add `Open Here` context menu option and Add `Run with PowerShell 7` context menu option
1. Complete the installation
1. Review version by opening `PowerShell 7` from the start menu as an administrator.

    ```powershell  
    $PSVersionTable.PSVersion
    ```
1. Pin to TaskBar
1. Open Windows Terminal
1. Review the new PowerShell 7 instance
1. Make sure you can do both PowerShell 5 and PowerShell 7 in the Windows Terminal.








