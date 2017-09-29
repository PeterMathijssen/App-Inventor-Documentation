# Live Testing / Development

AppyBuilder provides you drag-and-drop interface for designing and building your Android mobile apps. During development, you can connect your Android device for Live Testing. For example, when you drag a Button to the Viewer, you can immediately view the result on your device. Also, when you make something to happen \(e.g. pressing a Button\), you can directly press the button on your phone.  This kind of feedback is enormously useful, because it lets you develop and test your apps _incrementally_, defining each bit of new behavior and testing as you go along. Inexperienced programmers often make the mistake of building a large amount of stuff before they test any of it. Then, when they run into bugs, they're faced with a huge tangle to sort out, where they don't know which pieces are working and which are not. So try to work incrementally. You'll still surely encounter bugs, but incremental development will let you isolate bugs more quickly and fix them more easily.

To perform Live Testing / Development, you'll require AppyBuilder companion app. The companion app can be found in Google Play Store. Follow link [HERE ](https://help.appybuilder.com/release-notes.html)which includes the version of the companion app.

Once you install AppyBuilder companion app, you'll need to connect it to your computer.

**NOTE: **If you have already run the App Inventor companion app, you have to KILL the companion app and / or from your Windows Task Manager, kill adb.exe

Currently, there are 2 approaches for Live Testing / Development:

##### 1. Connection through WiFi

You'll need to connect both your computer and your device to the SAME WiFi Network.

* Start your companion app
* Goto [http://Gold.AppyBuilder.com](http://Gold.AppyBuilder.com)
* Either open existing app or start a new one
* From menu select Connect, then Live Testing: 

![](/assets/connectWiFi1.png)

* AppyBuilder will provide you a QR code. You can use the companion app to scan or manually enter the 6-digit code:

![](/assets/connectWiFi2.png)

![](/assets/ConnectWiFi3.png)

##### 2. Connection using USB

Currently, the USB option only works for Windows OS. Download AppyBuilder-Starter-app from [**HERE**](http://appybuilder.com/companion/AppyBuilderStarterSetup.msi). This is an installer package that includes the files required connect your device, through USB to your Windows computer. Run the setup. The setup will install the files onto  

