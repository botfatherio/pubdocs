First you need to `download a bot Script` you want to run. You can either:

1. Visit our [Scripts page](/scripts/) and download a Script
2. Visit our [Documentation](/docs/) to learn how to write your own Script
3. Search the web, github, bitbucket, gitlab or online boards for Scripts

Scripts contain the bots logic and algorithms. Some scripts have options on their top. Use a code editor like Notepad++, Sublime Text or Visual Studio Code to `edit script settings` if necesarry. To run the script you need to `download and install` botfather.

1. **Download** the botfather installer from our [download page](/downloads/)
2. **Run the installer** and follow the wizards instructions
3. **Start botfather** and run your Script by clicking the Play button

Depending on what kind of Script you want to run (Android, Browser, Desktop) you may want to `touch botfather settings`.

### Run Android Scripts

---------

To run an Android Script you must **select what Device or Emulator to control** using the Android dialog. Both real Android devices and common Android Emulators can be controled.

Botfather uses the Android Debug Bridge (ADB) in the background to control Android. We don't ship ADB with botfather thus you have to download and **install it manualy**. 

ADB is part of the [Android SDK Platform Tools](https://developer.android.com/studio/releases/platform-tools) which you can get from the Android website.

### Run Browser Scripts

---------

To run websites with Flash content you need to **activate the Adobe Flash Player** using the botfather settings dialog. To do so [Adobe Flash Player for Opera and Chromium (PPAPI)](https://get.adobe.com/de/flashplayer/otherversions/) must be installed on your computer.

On **Windows** you just need to run the Flash installer. Then activate the _Use system wide Flash installation_ option in the botfather settings.

On **Linux** you need to download _.tar.gz_ version of the Flash Player and extract it. Then select the contained _libpepflashplayer.so_ and _manifest.json_ file in the botfather settings.

To apply the Adobe Flash Player settings **restart botfather**.

##### Warning:
Flash might work in your favorite Browser like Google Chrome, Edge or Firefox. But that does not mean you already have the correct Flash version installed. Google Chrome for instance ships with its own Flash version. Thus you still have to **install Adobe Flash Player PPAPI** manualy!

### Run Desktop Scripts

---------

Running an Desktop Script that controls your mouse you might want to **configure a Hotkey** to start/stop the bot. 
