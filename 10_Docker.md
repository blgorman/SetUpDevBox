# Get Docker

In this task you'll get Docker installed on your machine.

>**Note:** If you are not working for a large organization you can use Docker Desktop.  If you are working for a large organization, you should avoid using Docker Desktop unless your organization is paying for licensing.  

Because of licensing issues, this tutorial will utilize Docker directly within WSL without Docker Desktop.

If you can use Docker Desktop, you should just install the solution from their website and docker will then be working for your from that point on in both WSL and Windows.

## Docker Desktop

If you are working for a large organization, you should avoid using Docker Desktop unless your organization is paying for licensing. If you are on your own, you can use Docker Desktop.

>**Note:** The videos will not cover installing docker desktop.  If you install and use Docker Desktop, you are going to be done with this walkthrough.

## Docker without Docker Desktop

Make sure your machine can handle docker. 

### Virtualization

I am creating these videos on a virtual machine with 4 cores.  In order for the platform to allow the containerization to work, I have to have a couple of Windows Features enabled.  If you are running on your own machine, you likely do not need to do this.  I do not believe it would hurt if you do enable these features, but you may not need to.

1. Windows Features On or Off

    Open the Windows Features On or Off dialog and ensure that the following features are enabled:

    - Hyper-V
    - Virtual Machine Platform
    - Windows Hypervisor Platform

    >**Note:** Do not enable `Containers`.  I know this is anti-intuitive, but you are not running Windows Server or Windows containers on this machine so it will be useless to turn this feature on. 

1. Restart your machine
1. Open a PowerShell terminal as an administrator
1. Log in to WSL
    
        ```PowerShell
        wsl
        ```  

1. Follow this excellent tutorial to get Docker installed and working on your machine

    ["Brian Hogan's Docker Tutorial at Digital Ocean"](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04)  

1. Make sure to enable the ability to run docker without `sudo` (it's in the tutorial)

1. Make sure to run the hello world container.

## Additional Updates

### Docker Desktop

I decided to recorde a quick video of Docker Desktop running on another machine.  I did this because I wanted to show you what it looks like when you run Docker Desktop.  I also wanted to show you how much easier it can be without having to run commands from the command line.

### Docker without Docker Desktop

I then also decided to run the same tutorial as above.  As long as I've never started Docker Desktop, I can use the local instance of Docker on the machine without Docker Desktop.  One caveat is the command start the docker service on the WSL instance is different than the tutorial.  I have included the command below.

```bash
sudo service docker start
```  

I noticed, however, that as soon as I start Docker Desktop, the command is overtaken by Docker Desktop and I can no longer use the local instance of Docker.  I have to restart the machine to get the local instance of Docker to work again.  Even stopping Docker Desktop does not allow me to use the local instance of Docker, as the docker instance is stopped but starting it does not work after having run Docker Desktop.

## Conclusion

You are now able to use WSL2 with Ubuntu to run docker containers on your machine.  You can use this to run docker and do modern cloud-native development on your machine.  You also know that you do not need to use Docker Desktop, which could be very valuable when it comes to working for a large organization that does not want to pay for licensing for Docker Desktop.
