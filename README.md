# yawk: Yet Another Weather app for Kobo

Based on [Kevin Short's app](https://www.mobileread.com/forums/showthread.php?t=194376)

Running on Python's distribution from [NiLuJe](https://www.mobileread.com/forums/showthread.php?t=254214)

Using the excellent library [FBInk from NiLuJe](https://github.com/NiLuJe/py-fbink)

Uses [Open Weather Maps](https://openweathermap.org/) as forecast and current conditions provider

Everything was tested on a [Kobo Glo](https://en.wikipedia.org/wiki/Kobo_Glo) using the firmware 4.13.12638

# Disclaimer

The procedure I'm suggesting here will most likely void the warranty.

Follow the guidelines at your own risk, I'm not responsible for any problems that might arise from this app's usage.

# Installation 

1. I suggest you Reset your device to factory defaults:
	1. Turn it off
	1. Holding the Light Switch, slide the power button for ~1 sec
	1. Hold the Light switch until the "Restoring" screen appears
	1. Follow directions on the screen (you'll need the [Kobo Setup app](https://www.kobosetup.com) and an account, I used from RakutenKobo itself)
	1. Update everything, connect to your WiFi network
1. Provide [telnet access](https://wiki.mobileread.com/wiki/Kobo_WiFi_Hacking#Enabling_Telnet_.26_FTP) - you can skip this step if you're able to find out the IP address of the device using some other method.
	1. Check the file .kobo/ip.txt for the IP address
1. Install [NiLuJe's Stuff](https://www.mobileread.com/forums/showthread.php?t=254214) - tested with Version 1.5.N @ r15719 on 2019-Apr-06 @ 07:25
1. Using the preferred FTP client (ie: [WinSCP](https://winscp.net/eng/download.php)), copy the repository's content to the folder /mnt/onboard/.apps/yawk
1. Create an account in [Open Weather Maps](https://openweathermap.org/):
    1. Take note of your API key
    1. Find out the ID your city (use the website to check the weather in your city, copy the ID from the URL) 
1. Open a SSH (or telnet) connection (user: root, password blank), navigate to /mnt/onboard/.apps/yawk/ and run install.sh
    1. if it says "-sh ./install.sh: not found", you have to convert the line endings to unix style:
    ```sed -i 's/^M$//' install.sh```
    1. Answer the questions correctly
    

# Doubts, suggestions

brunolalb@gmail.com