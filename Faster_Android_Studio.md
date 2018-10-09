# Faster Android Studio

This guide will help you to achieve faster build and make Android Studio more responsive. Consist of two parts, first disabling unneeded plugins and second add global gradle.properties for Android Studio.

## Remove Unneeded Plugins

Go to preferences > plugins > and disable everything you don't need.
 - Android APK Support 
 - Android Games
 - Android NDK
 - App Links Assistant
 - CVS
 - EditorConfig
 - Firebase product (all of them)
 - GitHub
 - Google product (all of them)
 - Mercurial Integration
 - Settings repository
 - Subversion integration
 - Task management
 - Test recorder
 - TestNG-j
 - YAML

## Add "gradle.properties"
Copy `gradle.properties` in this repo to whatever directory applies:

-   `/home/<username>/.gradle/`  (Linux)
-   `/Users/<username>/.gradle/`  (Mac)
-   `C:\Users\<username>\.gradle`  (Windows)
