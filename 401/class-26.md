# Android Fundamentals

## **Application Fundamentals:**

Android apps can be written using Kotlin, Java, and C++ languages. The Android SDK tools compile your code along with any data and resource files into an APK or an Android App Bundle.

Each Android app lives in its own security sandbox, protected by the following Android security features:

+ The Android operating system is a multi-user Linux system in which each app is a different user.
+ By default, the system assigns each app a unique Linux user ID (the ID is used only by the system and is unknown to the app). The system sets permissions for all the files in an app so that only the user ID assigned to that app can access them.
+ Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps.
+ By default, every app runs in its own Linux process. The Android system starts the process when any of the app's components need to be executed, and then shuts down the process when it's no longer needed or when the system must recover memory for other apps.


### **App components:**
There are four different types of app components:

+ Activities
+ Services
+ Broadcast receivers
+ Content providers


### **Activating components:**
Three of the four component types—activities, services, and broadcast receivers—are activated by an asynchronous message called an intent. Intents bind individual components to each other at runtime. You can think of them as the messengers that request an action from other components, whether the component belongs to your app or another.

An intent is created with an Intent object, which defines a message to activate either a specific component (explicit intent) or a specific type of component (implicit intent).


### **The manifest file:**

The manifest does a number of things in addition to declaring the app's components, such as the following:

+ Identifies any user permissions the app requires, such as Internet access or read-access to the user's contacts.
+ Declares the minimum API Level required by the app, based on which APIs the app uses.
+ Declares hardware and software features used or required by the app, such as a camera, bluetooth services, or a multitouch screen.
+ Declares API libraries the app needs to be linked against (other than the Android framework APIs), such as the Google Maps library.




**resources:** 

*[https://developer.android.com/guide/components/fundamentals](https://developer.android.com/guide/components/fundamentals)*
