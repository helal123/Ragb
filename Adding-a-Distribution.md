If you want to add a distribution that is not currently supported, here is how you go about that:

1. A distribution is a special type of app.  Please read [this](https://github.com/CypherpunkArmory/UserLAnd/wiki/Adding-an-App) first.
2. Tell us that you want to help us out by doing the work to add a new distribution.  You can do this by filing an issue [here](https://github.com/CypherpunkArmory/UserLAnd/issues/new/choose).
3. We will create a new repo.  It will be empty, but named `UserLAnd-Assets-DISTNAME`. 
4. You fork that new repo to do your work.
5. That repo needs to contain things like you see in [this one](https://github.com/CypherpunkArmory/UserLAnd-Assets-Debian).
6. The anatomy of that repository is as follows:
   * The [assets](https://github.com/CypherpunkArmory/UserLAnd-Assets-Debian/tree/master/scripts) subdirectory is where files that need to be copied to the device live.  Some interesting assets are:
      * `tar.gz` files (per architecture type supported) that represent the initial `chroot` image.  These are `split` to avoid going over GitHub's rule about no files over 100MB without paying.
      * `start*.sh` scripts that are used to startup and SSH or VNC server, so we can connect to them from client side apps.
      * `userland_profile.sh` which sets up, or clears, needed environment variables on each login.
      * `assets.txt` files (per assets subdirectory) that list out all the asset files in that subdirectory and their last modified timestamps.  We use the timestamps to know when to update the files (this will become more robust later).
   * The [scripts](https://github.com/CypherpunkArmory/UserLAnd-Assets-Debian/tree/master/scripts) subdirectory contains scripts that help create the assets.  Some interesting scripts are:
      * [buildArch.sh](https://github.com/CypherpunkArmory/UserLAnd-Assets-Debian/blob/master/scripts/buildArch.sh) builds the architecture dependent files needed, including the `tar.gz` files that are used to create the initial `chroot`.
      * [installArch.sh](https://github.com/CypherpunkArmory/UserLAnd-Assets-Debian/blob/master/scripts/installArch.sh) copies those built files into the assets subdirectory.
7. When finished, make a pull request with your changes.
