## Notification Listener Privacy Concerns Explained

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