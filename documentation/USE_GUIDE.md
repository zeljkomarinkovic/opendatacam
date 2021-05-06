## Documentation for using ODC on Jetson development boards

To install image on SD card follow official documentation on Nvidia website.
To install OpenDataCam follow ODC documentation

### PuTTY installation

To get PuTTY working requires a small amount of configuration. First, if you have not done so already, you will want to download PuTTY.
You'll need too choose the appropriate \*.msi installation file for your system while doing so. If you are unsure of whether you are running a 32-bit or 64-bit system, you can check by right-clicking on the Windows Start menu and choosing “System”. You will be provided all the necessary information. If you are still unsure, you can always choose the 32-bit version; it should run without trouble on either system.
Once you have downloaded the appropriate file, double-click on the installation icon, and run the Windows installer. After it has finished being installed, start up PuTTY.

Connect to a VPS with PuTTy via Password
After opening PuTTY, you should see a screen that looks something like this:

![putty_hostname](https://user-images.githubusercontent.com/23746207/117303561-1f0ca700-ae7d-11eb-8983-3a5758a555fd.png)

In the field labeled Host Name (or IP address), enter the IP address or hostname of your PuTTy compatible VPS, like so:

- In case of NGROK
  - 0.tcp.ngrok.io Port: 1234
- Or in local network
  - 172.20.57.72 Port: 22

![putty_ssh](https://user-images.githubusercontent.com/23746207/117304094-a823de00-ae7d-11eb-89b4-150101fea4aa.png)

Verify that PuTTy SSH has been chosen. You'll also want to verify your SSH settings, so on the left menu, under “Connection,” click on “SSH” and you will see this screen:

![putty_protocol](https://user-images.githubusercontent.com/23746207/117304217-ca1d6080-ae7d-11eb-9214-45ee37241764.png)

Under “Preferred SSH protocol version” make sure you check “2” (“1” is an older and less secure version of SSH).
At this point, you can open your SSH window, by clicking “Open.”
You will be shown a terminal window. Enter your login name, and password.

### Changing settings in ODC

In putty terminal type `nano opendatacam/config.json`

There you can change settings to your likings, when done press `CTRL+o` for save and `CTRL+X` for exit from nano

To apply settings simply type `pm2 restart opendatacam`

It will take some time to restart process and settings will be applied
