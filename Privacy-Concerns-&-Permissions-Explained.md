# Privacy Concerns Explained

## Notification Listener (required for Android 8.0+ Oreo)

### **Why?**
#### Old Broadcast Receiver Scrobbling is Broken on Devices using Android Oreo and above.

 * Old Simple (Last.fm) Scrobbler relied heavily on track information Broadcasts aka implicit broadcasts.
 * [Implicit Broadcast ban on Android Oreo](https://commonsware.com/blog/2017/04/11/android-o-implicit-broadcast-ban.html)
 * Google does not allow us to [Target SDK 25 or lower anymore](https://android-developers.googleblog.com/2017/12/improving-app-security-and-performance.html)
 * Hence for devices using (sdk 26) Android 8.0+ Oreo and above we can no longer use implicit broadcasts.

### **FACTS**
 * We are an open source app.
 * We do not collect private information and we store your private information in your phone.
 * Your music metadata will be sent to your chosen music metadata service(s). 
 * We only share necessary information for Scrobbles or Listens.

**Code Privacy Concerns**

_[ControllerReceiverService.java](https://github.com/simple-last-fm-scrobbler/sls/blob/master/app/src/main/java/com/adam/aslfms/service/ControllerReceiverService.java)_

 * Uses the Notification Listener Service Library
 * Connects the app to the Media Session Manager Google Java Library
 * Listens only for music data changes

_[ControllerReceiverSession.java](https://github.com/simple-last-fm-scrobbler/sls/blob/master/app/src/main/java/com/adam/aslfms/service/ControllerReceiverSession.java)_

 * contains static functions for media session management
 * contains simple functions

_[ControllerReceiverCallback.java](https://github.com/simple-last-fm-scrobbler/sls/blob/master/app/src/main/java/com/adam/aslfms/service/ControllerReceiverCallback.java)_

 * Manages the incoming data form your music apps
 * Manages play-state and metadata changes.

### Your Music MetaData

 1. [Last.fm Terms of Use](https://www.last.fm/legal/terms)
 2. [Libre.fm Privacy Policy Contact Information](https://gnu.io/contact/)
 3. [ListenBrainz Privacy Policy](https://metabrainz.org/privacy)

## Storage Permissions Explained (Optional)

 * Since Android KitKat [External Storage is required](https://developer.android.com/about/versions/android-4.4#BehaviorStorage) to read music metadata directly from devices before Android Oreo

**Code Privacy Concerns**

_[BuiltInMusicAppReceiver.java](https://github.com/simple-last-fm-scrobbler/sls/blob/master/app/src/main/java/com/adam/aslfms/receiver/BuiltInMusicAppReceiver.java#L220-L272)_

_[ScrobbleDroidMusicReceiver.java](https://github.com/simple-last-fm-scrobbler/sls/blob/master/app/src/main/java/com/adam/aslfms/receiver/ScrobbleDroidMusicReceiver.java#L118-L171)_

 * Both files pull music information directly from the storage device

_[Util.java](https://github.com/simple-last-fm-scrobbler/sls/blob/master/app/src/main/java/com/adam/aslfms/util/Util.java#L521-L544)_

 * Developer tool that exports the database to the file system.

## Battery Optimizations (Optional)

 * Disables service and app auto closing, especially important for users who disable "Active App Notification"

**Code Privacy Concerns**

 * There are no code privacy concerns

## In Summary

  * Big Sean - I Don't F*** With You (first few verses)
