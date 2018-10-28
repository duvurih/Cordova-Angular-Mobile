# Cordova-Angular-Mobile Technology & Features
  - Angular v6
  - Cordova
  - Fingerprint Authentication Integration
  - Camera Integration for Profile Picture
  - GeoLocation Statistics
  - Weather API Integration
  - Push Notifications

# Application  Structure
  -- Angular App Folder
    -- Angular Source and Depedencies
    -- Cordova App Folder "AngularMobile"
      -- Cordova App Source
      -- www - Angular Output Folder and Cordova output folder

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
    - cordova run android --devicce
  - Chrome Debugging Tools
    - chrome://inspect/#devices
    - select the device name to open in browser and debug
  
# Deployment
  - Android
  - iOS
