# MatterTracker mobile shell

Capacitor wrapper around the published MatterTracker web app
(https://matter-track-pro.base44.app) with native push notifications via
OneSignal (FCM for Android, APNs for iOS once the Apple Developer account
exists).

- `capacitor.config.json` — loads the published Base44 app via server.url
- OneSignal Cordova plugin v5 provides native push; the web app detects the
  native bridge and registers the device under the logged-in user's email
  (the same external id the Railway scraper targets)
- CI builds a debug APK on every push (Actions artifact `mattertracker-debug-apk`)
