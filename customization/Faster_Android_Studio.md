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
 
 ## Tweak your studio.vmoptions file
 tl;dr: in Android Studio head to “Help > Edit Custom VM Options…“ and change it to the below:
 
 #-Xms256m
#-Xmx2048m
-XX:ReservedCodeCacheSize=240m
-XX:+UseCompressedOops
-Dfile.encoding=UTF-8
-XX:+UseConcMarkSweepGC
-XX:SoftRefLRUPolicyMSPerMB=50
-Dsun.io.useCanonCaches=false
-Djava.net.preferIPv4Stack=true
-Djdk.http.auth.tunneling.disabledSchemes=""
-Djna.nosys=true
-Djna.boot.library.path=

-da
-Xverify:none

-XX:ErrorFile=$USER_HOME/java_error_in_studio_%p.log
-XX:HeapDumpPath=$USER_HOME/java_error_in_studio.hprof

# ###############################################
# custom settings from https://github.com/artem-zinnatullin/AndroidStudio-VM-Options/blob/master/studio.vmoptions
# ###############################################

# Runs JVM in Server mode with more optimizations and resources usage
# It may slow down the startup, but if you usually keep IDE running for few hours/days
# JVM may profile and optimize IDE better. Feel free to remove this flag.
-server

# Sets the initial size of the heap, default value is 256m
-Xms1G

# Max size of the memory allocation pool, default value is 1280m
-Xmx2G

# Sets the size of the allocated class metadata space that will trigger a GC the first time it is exceeded, default max value is 350m
-XX:MetaspaceSize=512m
