If you want to add a distribution that is not currently supported, here is how you go about that:

0. A distribution is a special type of app.  Please read [this](https://github.com/CypherpunkArmory/UserLAnd/wiki/Adding-an-App) first.
1. Tell us that you want to help us out by doing the work to add a new distribution.  You can do this by filing an issue [here](https://github.com/CypherpunkArmory/UserLAnd/issues/new/choose).
2. We will create a new repo.  It will be empty, but named `UserLAnd-Assets-DISTNAME`. 
3. You fork that new repo to do your work.
4. That repo needs to contain things like you see in [this one](https://github.com/CypherpunkArmory/UserLAnd-Assets-Debian).
5. The anatomy of that repository is as follows:
   * The [scripts](https://github.com/CypherpunkArmory/UserLAnd-Assets-Debian/tree/master/scripts) subdirectory contains scripts that help bootstrap the distribution and tar it up, such that it can be used as a `chroot` on a device.
   * The [assets](https://github.com/CypherpunkArmory/UserLAnd-Assets-Debian/tree/master/scripts) subdirectory is where files that need to be copied to the device live.  This includes the tar files, but also includes other useful assets that you need to modify for your purpose.
