# Night Yap apps for Umbrel

A community app store for umbrelOS with five apps. None holds secrets.

- **Night Yap Video** (`nightyap-moment-video`): the renderer behind the Night Yap app's "Download
  video". Image `ghcr.io/gauravnvidia/night-yap-moment-video`.
- **Paad Tak Stream** (`nightyap-paadtak-stream`; umbrelOS requires community app ids to start with the store id): streams https://paadtak.com/?stream live to YouTube, at
  low priority. Image `ghcr.io/gauravnvidia/paadtak-streamer`. The YouTube stream key is entered
  only in the app's settings on the Umbrel (Advanced, Environment variables), never here.

- **Firefox** (`nightyap-firefox`) and **Chromium** (`nightyap-chromium`): the linuxserver browsers,
  used from any browser on the network, downloading straight to Files, Downloads. The current images
  only work over HTTPS (why Umbrel's own Firefox and Chromium apps were disabled in July 2025), so the
  app icon opens a small page that forwards to https://<umbrel>:3453 (Firefox) or :3454 (Chromium),
  with the Umbrel's self-signed certificate. Sign in with `umbrel` and the password Umbrel generates
  for the app (shown in its info).

- **Wi-Fi Driver** (`nightyap-wifi-driver`): loads the TP-Link Archer T2U Plus driver (RTL8821AU, built from
  morrownr/8821au-20210708 in /home/umbrel/8821au-20210708) at every boot, because umbrelOS resets
  /lib/modules at boot. Privileged, host PID namespace; it uses the host's own modprobe and insmod.

Add this repository's URL in umbrelOS: App Store, the three dots, Community App Stores.
