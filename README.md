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
Create a file named  `gradle.properties`  in whatever directory applies:

-   `/home/<username>/.gradle/`  (Linux)
-   `/Users/<username>/.gradle/`  (Mac)
-   `C:\Users\<username>\.gradle`  (Windows)

> // Enable Gradle Daemon  
org.gradle.daemon=true
// Enable Configure on demand  
org.gradle.configureondemand=true
//Enable parallel builds  
org.gradle.parallel=true
// Enable Build Cache  
android.enableBuildCache=true
//Enable simple gradle caching  
org.gradle.caching=true
// Increase memory allocated to JVM
org.gradle.jvmargs=-Xmx2048m -XX:MaxPermSize=512m -XX:+HeapDumpOnOutOfMemoryError -Dfile.encoding=UTF-8


I set jvmargs to 2048m (2gb) in my computer with 8gb ram. You can increase it if you have more ram.
