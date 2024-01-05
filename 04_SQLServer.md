# SQL Server (SQL) and SQL Server Management Studio (SSMS)

In this walkthrough you'll get SQL Server and SQL Server Management Studio installed on your machine.

>**Note:** If you are using a Mac or Linux trying to do this set up, you can't do SQL Server from your machine. In order to make SQL Server work on your mac or linux machine you'll need to set up SQL server to run in a container.

## Other Database Options

If you are not doing .NET development and are doing typical LAMP development, you can use MySQL or MariaDB.  If you are doing Java development, you can alternatively use MySQL, MariaDB, or Oracle (or you can use SQL if you want).  If you are doing Python development, you can use MySQL, MariaDB, or PostgreSQL.  

This walkthrough will not cover installing those tools, but you can find instructions on how to install them on their respective websites.  Additionally, you can skip SQL Server and SSMS if you are not doing .NET development or Java/Azure development.

## Download and Install SQL Server

The first task it get SQL Server Developer edition on your machine.

### Task 1 - Download SQL Server

In this task you'll get SQL Server installed

1. Open a browser
1. Search for `SQL Server Downloads`
1. Click on the `SQL Server Downloads` link

    [SQL Server Downloads](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)  

1. Find the `Developer` edition by scrolling down the page
1. Click the button that says `Download now` under the `Developer` icon

    [Download SQL Server Developer Edition](https://go.microsoft.com/fwlink/p/?linkid=2215158&clcid=0x409&culture=en-us&country=us)  

### Task 2 - Install SQL Server

Install the SQL Server instance on your machine.

1. Run the installer to start the installation process
1. Select `Basic` installation
1. Click `Accept` on the license terms
1. Leave the defaults and Click `Install`
1. Wait for the installation to complete (maybe 8-10 minutes, grab a coffee and take a break).

## Download and Install SQL Server Management Studio

The second task is to get SQL Server Management Studio installed on your machine.

### Task 1 - Download and Install SSMS

Get SSMS downloaded and installed on your machine.

1. Search for `SSMS Download` (or click on the `Install SSMS` link on the SQL Server Downloads dialog if you still have that open`)  
1. Click on the link to `Download SQL Server Management Studio (SSMS)`
1. Click on the link to `Download SSMS`

    [Download SQL Server Management Studio (SSMS)](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16#download-ssms)

1. Click on the link for the `Free Download for SQL Server Management Studio (SSMS) XX.X`

    ["Free download for SQL Server Management Studio (SSMS)](https://aka.ms/ssmsfullsetup)  

1. Run the installer to complete the process

## Ensure you can connect to SQL Server

The third task is to ensure you can connect to SQL Server from SQL Server Management Studio.

### Task 1 - Connect to SQL Server

Make sure that you can connect to SQL Server from SSMS.

1. Open SSMS
1. Connect to the `localhost` instance using your windows credentials

You are now ready to work with SQL Server and SSMS on your machine.

## Get AdventureWorks Database

In this last part (optional), you can get a sample database, restore it, and ensure your machine is ready to work with SQL Server.

### Task 1 - Download AdventureWorks and Restore

In this task you'll get the download.  You can choose the full or the LT version, depending on what makes sense for your needs.

1. Open a browser
1. Search for `AdventureWorks Download`

    [AdventureWorks Download](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms)

1. Click on the appropriate `AdventureWorks Download` link [it doesn't matter which one you choose, unless you have a reason to get an older version - 2017 will run on 2022, etc as these are not specific to a database version]
1. Use SSMS to `Restore` the database (under Database-> Restore Database)
1. Find the folder for where the backup should be stored
1. Move the backup file to that folder
1. Restore the database

### Task 2 - Query AdventureWorks

In this task you'll just query the table to show that the database is installed and working and the machine is handling SQL Server as expected.

1. Open SSMS
1. Connect to the `localhost` instance using your windows credentials
1. Expand the `AdventureWorks` database
1. Expand the `Tables` folder
1. Right click on the `Person.Person` table and select `Select Top 1000 Rows`
    - can also do the `Script Table as` -> `Select to` -> `New Query Window` option  
        - hit f5 to run the query
1. You should see the data from the table

## Conclusion

You have now installed SQL Server and SSMS and restored a database to prove that you have a fully working and enabled SQL Server instance on your machine with SSMS to query the data at will.
