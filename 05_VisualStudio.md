# Installing Visual Studio

In this task, you'll get Visual Studio with the .NET tools for Desktop, Web, and Azure development installed on your machine.

## Other IDE Options  

If you are not doing .NET Development or you are on a Mac, you will likely not want/need Visual Studio.  You can skip this walkthrough in that case.  You may also consider the following alternatives:

1. Eclipse (Java Development)
1. IntelliJ (Java Development)
1. Jetbrains Rider (.NET Development on a Mac - requires a subscription)

## Task 1 - Download Visual Studio

In this task you'll get Visual Studio installed on your machine.

1. Open a browser
1. Search for `Visual Studio Downloads`
1. Click on the `Visual Studio Downloads` link

    [Visual Studio Downloads](https://visualstudio.microsoft.com/downloads/)  

1. Unless you have a license for Visual Studio, you'll want to download the `Community` edition  

>**Note:** If you have a professional or enterprise license, you can download the appropriate version instead.

    - Click on the `Free download` under the `Community` section.

## Install Visual Studio

1. Run the installer to start the installation process

### Select Workloads

During the installation you will select the workloads you want to install.  The following workloads should be selected at minimum (you can select others if you want):

1. ASP.NET and web development
1. .NET desktop development
1. Data storage and processing

Optional

1. Azure development
1. .NET Multi-platform development (MAUI)
1. Game development with Unity

### Select Individual Components

Along with workloads, you can select additional components.  The additional components allow you to add additional functionality to Visual Studio.  The following components should be selected at minimum (you can select others if you want):

1. Get the two previous versions of .NET Core still in support (.NET 7 goes out of support by June 2024).  

- .NET 6 (EOS - November 2024)
- .NET 7 (EOS - June 2024)

1. .NET 8 should already be selected, ensure that it is.
1. .NET Framework 4.8 SDK/4.72 should be included
    - don't do others unless you have specific needs (i.e. you have a .NET Framework 4.51 project that you are supporting)

### Select Language Packs  

If you need additional languages, you can select them here.  Otherwise, you can skip this step.

### Select Installation Locations

1. Complete the installation in the default location

1. Select `Install while downloading` to speed up the installation process.

## Validate Visual Studio is installed

After Visual Studio Community (or other edition) is installed, you will need to reboot your machine at some point.

You can reboot now, or you can wait until the end of this validation step.

### Get started

When getting started you will need to eventually sign in with a Microsoft account.  You can skip this step for now, but plan on using an outlook or hotmail or other personal email to get signed in.

>**Note:** If you are using a version on a work subscription, of course you need to use that email.  For VSCommunity, I recommend using a personal email.

1. Open Visual Studio
1. Log in or skip the login for up to 30 days

### Create a new project (optional)

In this step you'll create a new web project to validate your installation and database.

1. Click on `Create a new project`
1. Select `ASP.NET Core MVC Model-View-Controller project`
1. Create the project with
    - Individual Accounts (ensures database is required and wired up)
1. Modify the connection string to use
    - server: localhost
    - database: projectnamedb
    - TrustServerCertificate: true
1. Run the project
1. Click on `Register` and create a new user
1. Stop the project after seeing the error
1. Modify the connection string in appsettings.json
    - Add `TrustServerCertificate=True;` to the connection string
1. Open the Package Manager Console
1. Run the following command to create the database
    - `Update-Database`
1. Run the project again
1. Click on `Register` and create a new user
1. Confirm the user
1. Log in with the user
1. Open SSMS and connect to the database
1. Confirm the user is in the database

### Reboot the machine

It's a good time to reboot the machine now.

### Run Windows Updates

1. Open Windows Updates
1. Check/Run Windows Updates
1. Reboot the machine if necessary
1. Complete any pending updates and repeat until no more updates are available.

## Complete

This completes the walkthrough for getting Visual Studio installed on your machine.  
