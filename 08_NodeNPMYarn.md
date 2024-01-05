# Node, NPM, and YARN

If you are going to be developing with Angular or React or any other Javascript framework, you'll need to have Node and NPM installed on your machine.  YARN is also a tool that has historically performed better than NPM to get packages (although this may no longer be the case).  I would still recommend installing YARN until I hear reasons not to.

## Get Node

Start by Getting Node LTS installed on your machine.

1. Open a browser
1. Search for `Node LTS download`
1. Click on the `Node LTS download` link

    [Node LTS Download](https://nodejs.org/en/download/)  

1. Download the LTS version for your machine (i.e. 64-bit Windows .msi installer)
1. Run the installer to install Node

>**Note:** My installation seemed to hang because of some visual studio issues.  I decided to kill the installer but node and npm were already installed.

## Validate Node and NPM are installed

1. Open a terminal
1. Type the following commands:

    ```bash
    node --version
    npm --version
    ```

    You should see the latest version of Node and NPM installed on your machine.

## Get YARN

Next get YARN installed on your machine.

>**Note:** When I first did this, I installed the old version by accident (it's the same version in chocolatey).  I had to then run the additional tools to get the installation correctly installed.

1. Latest version (4)
1. Open a terminal
1. Run the commands found here:

    [YARN Installation](https://yarnpkg.com/getting-started/install)  

    ```PowerShell
    corepack enable
    yarn init -2
    yarn set version stable
    yarn install
    ```

## Validate YARN is installed

1. Open a terminal
1. Type the following command:

    ```bash
    yarn --version
    ```

    You should see the latest version of YARN installed on your machine.

## Create an angular project

To validate everything is working, create a simple Angular project

1. Follow the tutorial here:

    [Geeks for Geeks Angular Tutorial](https://www.geeksforgeeks.org/angular-cli-angular-project-setup/)  

1. Open a terminal
1. Type the following command:

    ```bash
    cd C:/code
    mkdir angularprojects
    cd angularprojects
    npm install -g @angular/cli
    ng new myAngularApp
    cd myAngularApp
    yarn
    ng serve -o --poll=2000 
    ```  

1. Validate the site

    Ensure you can validate the site is working at

    [http://localhost:4200](http://localhost:4200)

## Conclusion

You now have Node, NPM, and Yarn working and optionally created a working angular project.

