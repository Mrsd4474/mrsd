## Getting Started
1. Open this link and download the correct tools for your Windows, Mac or Linux machine.
   * [Android Platform Tools with adb (android debug bridge, utility)](https://developer.android.com/studio/releases/platform-tools)
2. Unzip the downloaded folder.
3. Search the unzip folder for the folder that contains the **adb** compiled program utility adb.exe or adb
4. Find the debuggable version of Simple Last.fm Scrobbler you would like to use in [releases](https://github.com/simple-last-fm-scrobbler/sls/releases)
5. Install the .apk file on your Android device

## For people with more than one phone connected
```console
.\adb devices -l
```
View your devices and notice the transport ID, usually a single digit integer (unless you have 10+ devices connected)
Example 
transport_id:1
transport_id:2
Remember this you will need to add the flag later.

## Logging data
 ### For users who have one device connected.
```console
.\adb logcat -d com.adam.aslfms:V > log.txt
```
  ### For users who have multiple devices connected.

.\adb logcat -d com.adam.aslfms:V -t INSERT_TRANSPORT_ID
```console
.\adb logcat -d com.adam.aslfms:V -t 2 > log.txt
```

## Sharing logs
If you are new and you are sharing debugging information please copy or upload the log.txt file directly to GitHub or somewhere online we can read it.

[https://hastebin.com](https://hastebin.com) is great place to paste the log.txt file and share the link where you need to.
You could also create an issue or add to an existing issue using the [SLS GitHub Issues List](https://github.com/simple-last-fm-scrobbler/sls/issues)
