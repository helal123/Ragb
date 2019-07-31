## Background context
Android Q introduces security improvements that change how apps are required to handle files. You can read more about these changes [here](https://developer.android.com/preview/privacy/scoped-storage). TL;DR, we can no longer be granted blanket access to user's SD cards. This is generally a good thing in terms of your security, but it means that getting files into and out of UserLAnd has become a slightly more involved process. 

### AN IMPORTANT NOTE ABOUT USERLAND FILES
Scoped storage is deleted when the app is uninstalled. To keep any files after uninstalling, make sure to copy them somewhere outside scoped storage before you uninstall.

There are potentially two areas of scoped storage available on your device.
- **Emulated external storage**
  This is available on every device. It is referenced as `INTERNAL` because it is a partition of your main storage 
  device which emulates an sdcard.
- **Actual external storage on an sdcard**
  _If_ you have a physical sdcard inserted in your phone, you will also have access to scoped storage on that
  storage device. We reference this as `SDCARD`.

## Sharing files using `/storage` bindings in a UserLAnd session
- Copy any file(s) to `/storage/<internal or sdcard>` in a UserLAnd session to make them available in an Android file browser.
![Copying files in a UserLAnd session](https://i.imgur.com/UeBQQwU.png)


## Accessing files through an Android file browser.

### Method 1
Files can be accessed using our custom document provider if it is available on your device. You can also copy files into this directory to make them accessible at `/storage/<internal or sdcard>` while in a UserLAnd session. You can access this document provider by accessing the dropdown menu in the top left of your file browser. _UserLAnd SDCARD will only be enabled **if you have a physical sdcard inserted in your device**_.

![](https://imgur.com/Zord3Xf.png)

This document provider will lead directly to the directory that is bound to `/storage/<internal or sdcard>` while in a UserLAnd session.

![](https://i.imgur.com/O8dyXY4.png)

### Method 2
Navigate manually to scoped storage directory. This is usually under `<internal or sdcard root>/Android/data/tech.ula/files/storage`.
You can freely copy files into and out of this directory. Files in this directory will appear at `/storage` while in a UserLAnd session. You can see a typical directory structure below.


![](https://i.imgur.com/SUX7c5M.png)