## Background context
Android Q introduces security improvements that change how apps are required to handle files. You can read more about these changes [here](https://developer.android.com/preview/privacy/scoped-storage). TL;DR, we can no longer be granted blanket access to user's SD cards. This is generally a good thing in terms of your security, but it means that getting files into and out of UserLAnd has become a slightly more involved process. 

** AN IMPORTANT NOTE ABOUT USERLAND FILES **
Scoped storage is deleted when the app is uninstalled. To keep any files after uninstalling, make sure to copy them somewhere outside scoped storage before you uninstall.

## Sharing files using `/storage` in a UserLAnd session
- Copy any file(s) to `/storage` in a UserLAnd session to make them available in an Android file browser.
![/storage in UserLAnd session](https://i.imgur.com/Iex1ES0.png)

## Accessing files through an Android file browser.

### Method 1
Files can be accessed using our custom document provider if it is available on your device. You can also copy files into this directory to make them accessible at `/storage` while in a UserLAnd session. You can access this document provider by swiping left in your file browser.

![](https://i.imgur.com/u5Ac6pt.png)

This document provider will lead directly to the directory that is bound to `/storage` while in a UserLAnd session.

![](https://i.imgur.com/O8dyXY4.png)

### Method 2
Navigate manually to scoped storage directory. This is usually under `Android/data/tech.ula/files/storage`.
You can freely copy files into and out of this directory. Files in this directory will appear at `/storage` while in a UserLAnd session. You can see a typical directory structure below.


![](https://i.imgur.com/SUX7c5M.png)