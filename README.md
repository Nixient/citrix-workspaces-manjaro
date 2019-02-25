# Manjaro: Getting Citrix Workspace App working

I've recently started a project at work where I have to use Citrix to access an environment. Initially I spun a Windows VM, but didn't want to use Windows becuase there's a Linux application avialable from Citrix!

## Pre-Reqs

1. Install required libraries using Pacman and Pamac

    ```bash
    # Install required packages available from Package Manager
    sudo pacman -S libidn.so.11
    
    # Install required packages that are available from AUR (Be CAREFUL!)
    pamac build webkitgtk
    ```
    

## Setup

1. Download the latest version of [Citrix Workspace for Linux](https://www.citrix.com/downloads/workspace-app/linux/workspace-app-for-linux-latest.html).
2. Move it to a temporary directory and extract it.

    ```bash
    [user@host ~]$ mktemp -d
    /tmp/tmp.8ie08cOq8A
    [user@host ~]$ cd /tmp/tmp.8ie08cOq8A
    [user@host tmp.8ie08cOq8A]$ cp ~/Downloads/linuxx64-19.1.0.9.tar.gz .
    [user@host tmp.8ie08cOq8A]$ tar xvf linuxx64-19.1.0.9.tar.gz 
    ```

3. Run Installer as Root and select option 1.

    ```bash
    [user@host tmp.8ie08cOq8A]$ sudo ./setupwfc 
    ```
    
4. Follow the installer.
    - I did not install the USB Support
    
