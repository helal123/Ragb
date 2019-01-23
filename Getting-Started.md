## How to get started using UserLAnd:

There are two ways to use UserLAnd: single-click apps and user-defined custom sessions.

### Using single-click apps:
1. Click an app.
2. Fill out the required information.
3. You're good to go!

### Using user-defined custom sessions:
1. Define a session - This describes what filesystem you are going to use, and what kind of service you want to use when connecting to it (ssh or vnc).
2. Define a filesystem - This describes what distribution of Linux you want to install.
3. Once defined, just tap on the session to start up. This will download necessary assets, setup the filesystem, start the server, and connect to it.  This will take several minutes for the first start up, but will be quicker afterwards.

### Managing Packages 

**Debian, Ubuntu, And Kali**:

-> Update: `sudo apt-get update && sudo apt-get dist-upgrade`

-> Install Packages: `sudo apt-get install <package name>`

-> Remove Packages: `sudo apt-get remove <package name>`

**Archlinux**:

-> Update: `sudo pacman -Syu`

-> Install Packages: `sudo pacman -S <package name>`

-> Remove Packages: `sudo pacman -R <package name>`

### Installing A Desktop

**Debian, Ubuntu, And Kali**:

-> Install Lxde: `sudo apt-get install lxde` (default desktop)

-> Install X Server Client: [Download on the Play store](https://play.google.com/store/apps/details?id=x.org.server&hl=en)

-> Launch XSDL

-> In UserLAnd Type: `export DISPLAY=:0 PULSE_SERVER=tcp:127.0.0.1:<PORT NUMBER>`

-> Then Type: `startlxde`

-> Then Go Back To XSDL And The Desktop Will Show Up

**ArchLinux**:

-> Install Lxde: `sudo pacman -S lxde`

-> Install X Server Client: [Download on the Play store](https://play.google.com/store/apps/details?id=x.org.server&hl=en)

-> Launch XSDL

-> In UserLAnd Type: export `DISPLAY=:0 PULSE_SERVER=tcp:127.0.0.1:<PORT NUMBER>`

-> Then Type: `startlxde`

-> Then Go Back To XSDL And The Desktop Will Show Up

<br/>
<br/>
But you can do so much more than that. Your phone isn't just a play thing any more!