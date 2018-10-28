# Cordova-Angular-Mobile

# Technology & Features
  - Angular v6
  - Cordova
  - Android SDK
  - Fingerprint Authentication Integration
  - Camera Integration for Profile Picture
  - GeoLocation Statistics
  - Weather API Integration
  - Push Notifications

# Application  Structure
  - Angular App Folder
    - Angular Source and Depedencies
    - Cordova App Folder "AngularMobile"
      - Cordova App Source
      - www - Angular Output Folder and Cordova output folder

# Build Process
  - Angular Application Build Process
    - ng build --prod --base-href ./ --output-path .\AngularMobile\www
  - Cordova Application Build Process 
    - cordova run android //run on emulator
    - cordova build android // only build the apk file
    - cordova run browser // run on browser
    - cordodva run android --device //deploy and run on android mobile

# Debugging Process
  - To know the devices connected
    - adb kill-server
    - adb devices
    - cordova run android --device
  - Chrome Debugging Tools
    - chrome://inspect/#devices
    - select the device name to open in browser and debug
  - Fingerprint Authentication Test on Emulator
    - Open Emulator settings
    - Configure the pattern under the Security Settings
    - Add fingerprint authentication
    - execute the following command to recognize the fingerprint command
      - adb -e emu finger touch <finger_id>
      - adb -e emu finger touch 11aa11
    - Now build and run the application on emulator
      - cordova run android
      - Now app will ask for fingerprint authentication. To authenticate execute the below command
      - adb -e emu finger touch 11aa11
  
# Deployment
  - Android
  - iOS
