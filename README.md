# Custom_notification_code
Step by Step Notification Code

## Android Push Notifications using Firebase Cloud Messaging FCM
Integrating Firebase Cloud Messaging

 Now we’ll create a simple app that receives firebase messages from both firebase console and from the PHP code.

1)First thing you need to do is go to
[Firebase console](https://firebase.google.com)
and make an account to gain access to their console

2)A fter you gain access to the console you can start by creating your first project.

3) Give the package name of your project.and press Button.Add Firebase to your Android App.

4) Now Need of SHA1 key

by pressing Right side of Android Studio and Click Gradle and Select the app from Gradle projects tray,
double click on android-signingReport
you will see the SHA1 key on Console
SHA1: 62:14:3F:05:F4:1E:E8:9F:43:3A:56:81:0B:32:14:DB:5A:BE:A2:5C

5) Here the google-services.json file will be downloaded when you press add app button.
This step is very important as your project won’t build without this file.


## Add Firebase SDK
 The Google services plugin for Gradle loads the google-services.json file you just downloaded. Modify your build.gradle files to use the plugin.
## Project-level build.gradle (build.gradle):
  // Add this line
    classpath 'com.google.gms:google-services:4.0.0'
Sync the Project.

## App-level build.gradle (build.gradle):
dependencies {
  // Add this line
  compile 'com.google.firebase:firebase-core:16.0.0'
}
...
// Add to the bottom of the file
 
apply plugin: 'com.google.gms.google-services'

## Retrieve the current registration token:
 access the token's value by creating a new class which extends FirebaseInstanceIdService In that class, call getToken within onTokenRefresh.
 Also add the service to your manifest file.
 
 ## Get Custom Notification
 click on cloude Messaging,now open the Message tray,Fill up the data 
 Now Press Done button.You will get the Notification in Mobile Device.
 
 
 
 
 
 
