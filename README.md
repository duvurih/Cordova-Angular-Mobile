# Cordova-Angular Mobile/Desktop App

# Mobile App:

![alt text](https://github.com/duvurih/Cordova-Angular-Mobile-Desktop/blob/master/Context.png)

# Pre-Requisites
  - Windows 10 SDK to deploy cordova application as Wndows 10 desktop Application
  - Android Studio
  - Android SDK
  - Java SDK
  - Node.js
  - Cordova
  
# Technology & Features
  - Angular v7
  - Cordova
  - Fingerprint Authentication Integration
  - Camera Integration for Profile Picture
  - GeoLocation Statistics
  - Weather API Integration (OpenWatherAPI)
  - Flickr API Integration (FlickrAPI)
  - Forex API Integration (ForexPI)
  - Push Notifications
    - OneSignal.com and Google Cloud Messaging for Android
    - Firebase Cordova Plugin 

# Application  Structure
  - Angular App Folder
    - Angular Source and Depedencies
    - Cordova App Folder "AngularMobile"
      - Cordova App Source
      - www - Angular Output Folder and Cordova output folder
  - Creating Application
    - ng new "AngularCordovaApp"
    - move to "AngularCordovaApp"
    - cordova create AngularMobile
    - move to "AngularMobile"
    - Add following platforms
      - cordova platform add android
      - cordova platform add ios
      - cordova platform add browser
      - cordova platform add cordova-windows
    - Add following plugins
      - cordova plugin add cordova-plugin-device
      - cordova plugin add cordova-plugin-network-information
      - cordova plugin add cordova-plugin-camera
      - cordova plugin add cordova-plugin-geolocation
      - cordova plugin add cordova-plugin-fingerprint-aio
      - cordova plugin add cordova-plugin-android-fingerprint-auth

# Build and Deployment Process
  - Angular Application Build Process
    - ng build --prod --base-href ./ --output-path .\AngularMobile\www
  - Cordova Application Build Process 
    - cordova run android //run on emulator
    - cordova build android // only build the apk file
    - cordova run browser // run on browser
    - cordova run android --device //deploy and run on android mobile
    - cordova run windows // make-sure you have administrator previlages on windows 10 and developer mode enabled
    - cordova run windows -- --win //explicitly specify windows as target. Ensure Windows 10 SDK is installed
# Testing and Debugging Process
  - How to know connected devices
    - adb kill-server
    - adb devices
    - cordova run android --device
  - Chrome Debugging Tools
    - chrome://inspect/#devices
    - select the device name to open in browser and debug
  - Fingerprint Authentication Test on Android Emulator
    - Fingerprint Authentication works only on Marshmallow or greater versions
    - Open Emulator settings
    - Configure the pattern under the Security Settings
    - Add fingerprint authentication
    - execute the following command to register the fingerprint command
      - adb -e emu finger touch <finger_id>
      - adb -e emu finger touch 123abc
    - Now build and run the application on emulator
      - cordova run android
      - Now app will ask for fingerprint authentication. To authenticate execute the below command
      - adb -e emu finger touch 123abc
  
# Deployment
  - Android
  - iOS
  - Windows 10
