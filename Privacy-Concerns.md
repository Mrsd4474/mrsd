## Notification Listener Privacy Concerns Explained

Note
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


## In Summary

  * Big Sean - I Don't F*** With You
