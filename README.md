![Gazee](/public/images/logo.png)

Gazee is a comic viewer for the web browser.  This is a re-factor of the
original, made with the main author's blessings.  I tore some stuff out.  It
was easier to start a new repo.

Works great with [Mylar](https://github.com/evilhero/mylar) comic book management, but not needed.

Check out [the Wiki](https://github.com/hubbcaps/gazee/wiki) for detailed instructions on setup if you need them.

Questions can also be asked in the #gazee channel on Freenode

## Features

Index - Nice big cover thumbs
![screen01](https://32images.com/i/eaisme33.jpg)

Index - Smaller cover thumbs
![screen02](https://32images.com/i/sea3aeag.jpg)

The reader has views and whatnot.
![screen03](https://32images.com/i/gag3ssg2.jpg)

HTTPS Support

Bookmarks remember where you left off as you read.

Multiple Users and Admins

Much more to come!

## Requirements
* Python 3.6
* CherryPy
* Mako
* Pillow
* rarfile
* GitPython

Requirements can be installed easily in the setup section below.

#### Unrar Downloads

Unrar needs to be installed and visible in the path of the user Gazee is running under to be able to properly extract all CBRs.

Double check this on Windows, different systems have different requirements for making sure you have unrar visbile in your users path.

[Unrar for Windows](http://www.rarlab.com/rar_add.htm), windows also needs command line accessible Git installed, gone over in the [install guide on the wiki](https://github.com/hubbcaps/gazee/wiki/Windows-Install-Guide)

[Centos](https://www.rpmfind.net/linux/rpm2html/search.php?query=unrar) needs Unrar from RPMFusion, not Offical/EPEL unar application. unar is out of date and will fail with certain types of cbrs and other rar archives.

[Debian](https://packages.debian.org/jessie/unrar)

## Setup

**Step 1: Clone the repository and install python dependencies**

    cd <directory you want to install to>
    git clone https://github.com/hubbcaps/gazee.git
    cd gazee
    sudo python3 setup.py install
    
During the installation, look for a line like:

    Installing Gazee script to /usr/lib/python3.6/bin/

That if that directory isn't in your path, you can always do something like:

    cd /usr/local/bin
    ln -s /usr/lib/python3.6/bin/Gazee

...and start Gazee:

    Gazee

**Step 2: Logon to Gazee's Web UI**)

  Go to **http://localhost:4242**
  
  Default username and password for the web interface:

It will prompt you for a username / pw if you start the program without an
admin user created.  Default accounts are generallya a bad idea.
  
  Proceed to the settings page and change your admin pass, and enter the path to your comic library   and optionally your Mylar DB for better comic info extraction.

### Daemonize (Linux & OSX only)

You can easily run the program in Daemon mode by using the -d flag

    python Gazee.py -d

### QOL Features on the Roadmap

These are features that will make Gazee better and more up to par in what should be expected of a modern comic reader, but aren't needed for actual usability.

