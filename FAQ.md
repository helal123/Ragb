
# 1. How do I connect from a device on the same network?

   For ssh, we use port 2022.  So, you can use an ssh client from another device on the same network by connecting to your_phones_ip:2022 .

   For vnc, we use display :51.  So, you can use a vnc client from another device on the same network by connecting you your_phones_ip and specifying the display is :51 or the port is 5951 (depending on what your client needs).

# 2. How do I get Firefox working?

   # Installing Firefox on Debian
   For Debian, you can just click the Firefox icon on the apps page.  Or you can do the following manually:
   ```
   sudo apt update
   sudo apt install firefox-esr
   firefox-esr &
   ```

   # Installing Firefox on Ubuntu
   For Ubuntu you can do the following (sorry it is a little more involved):
   ```
   sudo apt update
   sudo apt install software-properties-common
   sudo add-apt-repository ppa:mozillateam/ppa
   sudo apt-get update
   sudo apt install firefox-esr
   firefox-esr &
   ```
   
   For other distros, please look online, possibly specifically on the Firefox website for how to install firefox-esr from packages (not snap).

# 3. How do I install a desktop environment?

   # The easy way
   For Debian, you can just click the `xfce` or `lxde` app icons and it will be setup for you.

   # The hard way
   For Debian or otherwise, `xfce` or `lxde` should install and work properly.  Ideally, this would be really easy, like `sudo apt update && sudo apt install xfce4` (for Ubuntu), but sometimes issues pop up that require more work on your behalf.  In the future we will make this easy for all distros we support.  For now, if you are getting an error about `udisks2` please see this issue:  https://github.com/CypherpunkArmory/UserLAnd/issues/1072