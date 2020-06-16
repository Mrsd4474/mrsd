# Privacy Concerns

## Notice
1. This app is licensed Free Open Source Software FOSS.
2. We do not keep, store, or steal any of your private information.
3. Required information is extracted via the [Media Session API](https://developer.android.com/guide/topics/media-apps/working-with-a-media-session) that requires Notification Listener permissions.
4. Hence, only track metadata will be extracted & sent to Last.fm, Libre.fm, ListenBrainz or your custom service.

## Concerning Code
 * [ControllerReceiverService.java](https://github.com/simple-last-fm-scrobbler/sls/blob/master/app/src/main/java/com/adam/aslfms/service/ControllerReceiverService.java#L50-L145)
 * [ControllerReceiverCallback.java](https://github.com/simple-last-fm-scrobbler/sls/blob/master/app/src/main/java/com/adam/aslfms/service/ControllerReceiverCallback.java)

## Explanation
 * 'NotificationListenerService' is used in the [ControllerReceiverService](https://github.com/simple-last-fm-scrobbler/sls/blob/master/app/src/main/java/com/adam/aslfms/service/ControllerReceiverService.java) to create a media session and pull meta data and play updates from the music app you have active via callback function inside [ControllerReceiverCallback](https://github.com/simple-last-fm-scrobbler/sls/blob/master/app/src/main/java/com/adam/aslfms/service/ControllerReceiverCallback.java).
 * Battery Optimization is in case you choose to not use the Permanent Notification setting, so scrobbles are submitted no matter the circumstance.
 * Storage access is in case you'd like to export your database.

## In Summary
[IDFWU I got a million other things, that I much rather do](https://www.youtube.com/watch?v=-d0Xms2jcu4)