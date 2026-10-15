# Night Yap apps for Umbrel

A community app store for umbrelOS with two apps. Neither holds secrets.

- **Night Yap Video** (`nightyap-moment-video`): the renderer behind the Night Yap app's "Download
  video". Image `ghcr.io/gauravnvidia/night-yap-moment-video`.
- **Paad Tak Stream** (`nightyap-paadtak-stream`; umbrelOS requires community app ids to start with the store id): streams https://paadtak.com/?stream live to YouTube, at
  low priority. Image `ghcr.io/gauravnvidia/paadtak-streamer`. The YouTube stream key is entered
  only in the app's settings on the Umbrel (Advanced, Environment variables), never here.

Add this repository's URL in umbrelOS: App Store, the three dots, Community App Stores.
