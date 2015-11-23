# ionic-progreanmer
Project Demo for Hybrid platform from VSM

#Install Step by Step
Tools for develop
  - Python 3.5.0
  - Nodejs 5
  - Java sdk7
  - Apache ant
  - Android sdk
  - Git for Windows 

#First Step
Depending on the platforms you wish to develop for, you’ll need to install platform-specific tools. Follow the Cordova platform guides for Android and iOS to make sure you have everything needed for development on those platforms. Luckily, you’ll only need to do this once.

#Windows users developing for Android: You'll want to make sure you have the following installed and set up.

NOTE: Whenever you make changes to the PATH, or any other environment variable, you'll need to restart or open a new tab in your shell program for the PATH change to take effect.

#Java JDK

Install the most recent Java JDK (NOT just the JRE).

Next, create an environment variable for JAVA_HOME pointing to the root folder where the Java JDK was installed. So, if you installed the JDK into C:\Program Files\Java\jdk7, set JAVA_HOME to be this path. After that, add the JDK's bin directory to the PATH variable as well. Following the previous assumption, this should be either %JAVA_HOME%\bin or the full path C:\Program Files\Java\jdk7\bin

#Apache Ant

To install Ant, download a zip from here, extract it, move the first folder in the zip to a safe place, and update your PATH to include the bin folder in that folder. For example, if you moved the Ant folder to c:/, you'd want to add this to your PATH: C:\apache-ant-1.9.2\bin.

#Android SDK

Installing the Android SDK is also necessary. The Android SDK provides you the API libraries and developer tools necessary to build, test, and debug apps for Android.

Cordova requires the ANDROID_HOME environment variable to be set. This should point to the [ANDROID_SDK_DIR]\android-sdk directory (for example c:\android\android-sdk).

Next, update your PATH to include the tools/ and platform-tools/ folder in that folder. So, using ANDROID_HOME, you would add both %ANDROID_HOME%\tools and %ANDROID_HOME%\platform-tools.

#Second Step
we will go and install the most recent version of Apache Cordova, which will take our app and bundle it into a native wrapper to turn it into a traditional native app.

To install Cordova, make sure you have Node.js installed, then run
```bash
$ npm install -g cordova
```

#Third Step
Install Ionic
Ionic comes with a convenient command line utility to start, build, and package Ionic apps.

To install it, simply run:
```bash
$ npm install -g ionic
```
# Fourth Step
Create the project
Now, we need to create a new Cordova project somewhere on the computer for the code for our app:
```bash
$ ionic start <project name> blank
```
That will create a folder called todo in the directory the command was run. Next, we will go into that directory and list the contents. Here is what the outer structure of your Ionic project will look like:
```bash
$ cd <project name>  && ls

├── bower.json     // bower dependencies
├── config.xml     // cordova configuration
├── gulpfile.js    // gulp tasks
├── hooks          // custom cordova hooks to execute on specific commands
├── ionic.project  // ionic configuration
├── package.json   // node dependencies
├── platforms      // iOS/Android specific builds will reside here
├── plugins        // where your cordova/ionic plugins will be installed
├── scss           // scss code, which will output to www/css/
└── www            // application - JS code and libs, CSS, images, etc.

```

 * Setup this project to use Sass:
 ```bash 
$ ionic setup sass
```
 

 * Develop in the browser with live reload:
 ```bash 
$ ionic serve
```

 * Add a platform (ios or Android): 
 ```bash 
$ ionic platform add ios [android]
```
   Note: iOS development requires OS X currently
   See the Android Platform Guide for full Android installation instructions:
   https://cordova.apache.org/docs/en/edge/guide_platforms_android_index.md.html

 * Build your app: 
 ```bash
$ ionic build <PLATFORM> 
  ```

 * Simulate your app: 
```bash
$ ionic emulate <PLATFORM>
```
 * Run your app on a device: 
```bash 
$ ionic run <PLATFORM>
```
#Android
First step is to enable Developer Options on your Android phone. By default the Developer Options are turned off. Once you turn them on, enable USB debugging.

To turn Android Developer options:

Go to your phone’s settings > About device > find a Build Version.

Tap the Build Version 7 times.

Tap the Developer Option. Scroll down to find USB Debugging and tick the box.

Go back to the terminal and type the command below to run for Android.
```bash 
$ ionic run android --device
```


 * Package an app using Ionic package service: 

```bash 
$ ionic package <MODE> <PLATFORM>
```
