## Background context
Android Q introduces security improvements that change how apps are required to handle files. You can read more about these changes [here](https://developer.android.com/preview/privacy/scoped-storage). TL;DR, we can no longer be granted blanket access to user's SD cards. This is generally a good thing in terms of your security, but it means that getting files into and out of UserLAnd has become a slightly more involved process. 

## Accessing files in your file manager

### Method 1
Access scoped storage using our custom document provider if it is available on your device. Files in this directory will appear at `/sdcard` while in a UserLAnd session. You can access this document provider by swiping left in your file browser if your device supports it.


![](https://i.imgur.com/dD4bUAi.jpg)

### Method 2
Navigate to scoped storage. This is usually under `Android/data/tech.ula/files/home`.
You can freely copy files into and out of this directory. Files in this directory will appear at `/sdcard` while in a UserLAnd session. You can see a typical directory structure below.


![](https://i.imgur.com/s4Rx5nH.png)

## Accessing files in a UserLAnd session
Files will be accessible at `/sdcard`.
![](https://i.imgur.com/LYURQkU.png)